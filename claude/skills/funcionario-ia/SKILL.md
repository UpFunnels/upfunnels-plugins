---
name: funcionario-ia
description: Lista, cria, lê, atualiza e apaga funcionários de IA e bases de conhecimento da UpFunnels, vincula uma base que já existe e adiciona fonte por URL ou texto.
---

# Funcionário de IA

Use só estas ferramentas: `list_assistants`, `get_assistant`, `create_assistant`, `delete_assistant`, `list_cerebros`, `get_cerebro`, `create_cerebro`, `delete_cerebro`, `force_delete_cerebro`, `link_assistant_cerebro`, `unlink_assistant_cerebro`, `update_assistant`, `update_cerebro`, `list_cerebro_sources`, `add_cerebro_source`, `delete_cerebro_source`.

Não grave o documento cru. `add_cerebro_source` aceita URL ou texto. Não envia arquivo.

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

Antes de `delete_assistant`, `delete_cerebro`, `force_delete_cerebro` ou `delete_cerebro_source`, peça confirmação ao usuário. `delete_assistant` apaga o funcionário. `delete_cerebro` apaga a base e recusa se ainda houver funcionário vinculado. `force_delete_cerebro` desvincula os funcionários e apaga a base. `delete_cerebro_source` apaga a fonte.
