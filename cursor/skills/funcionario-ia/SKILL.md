---
name: funcionario-ia
description: Lista, cria, lê, atualiza e apaga funcionários de IA e bases de conhecimento da UpFunnels, vincula uma base que já existe, adiciona fonte por URL ou texto, envia arquivo ou áudio em base64, diagnostica os funcionários, define quem atende cada canal conectado e consulta, marca e desmarca compromissos na agenda do funcionário.
---

# Funcionário de IA

Use só estas ferramentas: `list_assistants`, `get_assistant`, `create_assistant`, `delete_assistant`, `list_cerebros`, `get_cerebro`, `create_cerebro`, `delete_cerebro`, `force_delete_cerebro`, `link_assistant_cerebro`, `unlink_assistant_cerebro`, `update_assistant`, `update_cerebro`, `list_cerebro_sources`, `add_cerebro_source`, `delete_cerebro_source`, `add_cerebro_file`, `replace_cerebro_file`, `remove_cerebro_file`, `add_cerebro_audio`, `get_assistants_health`, `list_channel_connections`, `set_channel_assistant`, `get_assistant_calendar`, `list_assistant_calendar_events`, `create_assistant_calendar_event`, `delete_assistant_calendar_event`.

Não grave o documento cru. `add_cerebro_source` aceita URL ou texto. Não envia arquivo. `add_cerebro_file`, `replace_cerebro_file` e `add_cerebro_audio` enviam arquivo em base64, teto de 1 MB. Acima disso recusa.

- `list_assistants` lista os funcionários de IA, sem o prompt interno.
- `get_assistant` lê um funcionário: perfil, instruções e cérebros vinculados.
- `create_assistant` cria um funcionário de IA.
- `list_cerebros` lista as bases de conhecimento, sem embedding.
- `get_cerebro` lê uma base: documentos, fontes e funcionários vinculados. Sem segredo.
- `create_cerebro` cria uma base de conhecimento.
- `link_assistant_cerebro` vincula uma base que já existe a um funcionário.
- `unlink_assistant_cerebro` desvincula. Não apaga a base.
- `update_assistant` lê o documento, mescla e grava o modalData. Campo omitido permanece; null apaga. Não é PUT cru do documento.
- `update_cerebro` manda só o patch. A API já mescla. Campo omitido permanece.
- `list_cerebro_sources` lista as fontes da base, sem segredo.
- `add_cerebro_source` adiciona fonte por URL ou texto. Não envia arquivo.
- `add_cerebro_file` adiciona arquivo em base64, teto de 1 MB. Acima disso recusa.
- `replace_cerebro_file` substitui arquivo em base64, teto de 1 MB. Acima disso recusa.
- `add_cerebro_audio` adiciona áudio em base64, teto de 1 MB. Acima disso recusa.
- `get_assistants_health` diagnostica todos os funcionários: o que falta configurar e quem converte abaixo da média, com onde se corrige. Use em "o que melhorar?" e "quem precisa de atenção?".

## Passar a conversa, links e Telegram

Em `create_assistant` e `update_assistant`:

- `notifyHuman.attendants` passa a conversa para uma pessoa. Mande a lista completa: quem já existe vai com o mesmo nome; pessoa nova precisa do WhatsApp com DDI e DDD, só números. `when` diz quando chamar a pessoa.
- `notifyAssistant.rules` passa para outro funcionário de IA: `[{ assistantId, when }]`, lista completa.
- `rules.allowedLinks` são os links que o funcionário pode mandar, lista completa.
- `telegramLearning` liga o aviso no Telegram quando o funcionário não souber responder.

## Canais

- `list_channel_connections` mostra os canais conectados (WhatsApp, Instagram, Messenger) e qual funcionário atende cada um.
- `set_channel_assistant` troca quem atende um canal já conectado; `assistantId` null tira o atendente. Com mais de uma conexão no canal, mande o `connectionId`. Não conecta canal novo: isso é na tela de Integrações.

## Agenda

A agenda do funcionário é a Google Agenda conectada a ele. Conectar ou desconectar é só na tela.

- `get_assistant_calendar` diz se há agenda conectada e com qual conta.
- `list_assistant_calendar_events` lista só os horários ocupados (id, início e fim), sem título nem convidados.
- `create_assistant_calendar_event` marca um compromisso: `title`, `startISO` e `endISO` em ISO-8601 (horário de Brasília quando sem fuso), no futuro.
- `delete_assistant_calendar_event` desmarca pelo id que `list_assistant_calendar_events` devolve. Não tem desfazer.

Antes de `delete_assistant`, `delete_cerebro`, `force_delete_cerebro`, `delete_cerebro_source`, `remove_cerebro_file`, `delete_assistant_calendar_event` ou `set_channel_assistant`, peça confirmação ao usuário. `set_channel_assistant` muda quem responde os clientes daquele canal na hora. `delete_assistant` apaga o funcionário. `delete_cerebro` apaga a base e recusa se ainda houver funcionário vinculado. `force_delete_cerebro` desvincula os funcionários e apaga a base. `delete_cerebro_source` apaga a fonte. `remove_cerebro_file` apaga o arquivo da base.
