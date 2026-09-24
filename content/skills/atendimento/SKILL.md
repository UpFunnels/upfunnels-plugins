---
name: atendimento
description: Lista conversas, lê o histórico e envia texto numa conversa que já existe na UpFunnels.
---

# Atendimento

Use só estas ferramentas: `list_conversations`, `get_conversation`, `get_conversation_messages`, `send_conversation_message`.

- `list_conversations` lista conversas, sem o histórico e sem as mensagens. A prévia e a contagem bastam para achar o id.
- `get_conversation` lê canal, status e responsável. Sem as mensagens.
- `get_conversation_messages` lê o histórico, paginado.

Antes de `send_conversation_message`, peça confirmação ao usuário. Ela envia texto numa conversa que já existe, só pelo id. Não aceita telefone nem e-mail como destino.
