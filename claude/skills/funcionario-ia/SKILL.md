---
name: funcionario-ia
description: Lista funcionários de IA e bases de conhecimento da UpFunnels e vincula uma base que já existe.
---

# Funcionário de IA

Use só estas ferramentas: `list_assistants`, `get_assistant`, `list_cerebros`, `get_cerebro`, `link_assistant_cerebro`, `unlink_assistant_cerebro`.

Não existe ferramenta para criar ou reescrever funcionário nem base. Não tente escrever assistente nem cérebro.

- `list_assistants` lista os funcionários de IA, sem o prompt interno.
- `get_assistant` lê um funcionário: perfil, instruções e cérebros vinculados.
- `list_cerebros` lista as bases de conhecimento, sem embedding.
- `get_cerebro` lê uma base: documentos, fontes e funcionários vinculados. Sem segredo.
- `link_assistant_cerebro` vincula uma base que já existe a um funcionário.
- `unlink_assistant_cerebro` desvincula. Não apaga a base.
