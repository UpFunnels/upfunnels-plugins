# UpFunnels plugins

Dois roots, de propósito. Claude e Cursor não compartilham o manifesto do MCP.

- [`claude/`](claude/) — Claude Code e Cowork (`.mcp.json`)
- [`cursor/`](cursor/) — Cursor (`mcp.json`)

Servidor de produção: `https://mcp.upfunnels.com/mcp`

A fonte das skills é [`content/skills/`](content/skills/). `scripts/copy-skills.sh` copia esse texto para `claude/skills` e `cursor/skills`.

Submeter aos diretórios é passo humano. O marketplace do Cursor é curado.

Não há client id, secret nem header neste repositório.
