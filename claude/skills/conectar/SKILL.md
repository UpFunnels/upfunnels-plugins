---
name: conectar
description: Liga o Claude, o Cursor ou o ChatGPT ao MCP da UpFunnels pelo endereço do servidor, sem client id.
---

# Conectar a UpFunnels

Use o endereço do servidor que está em Configurações → MCP na UpFunnels. Não peça client id.

## Claude

No Claude Code, rode o comando com a URL do servidor no lugar de `<url>`:

```
claude mcp add --transport http upfunnels <url>
```

Ou, no Claude: Configurações → Conectores → Adicionar, e preencha o nome do MCP e a URL.

## Cursor

Em Configurações → Customize → MCP, execute a autenticação com o mesmo endereço.

## ChatGPT

Em Configurações → Plug-ins → MCPs, adicione a URL e execute a autenticação.

## Organização

A organização é a do consentimento. Quem autoriza escolhe a organização naquela tela.

## Dá para fazer?

Para saber se uma tarefa é possível pelo MCP ou se o token tem a permissão, use `discover`. Ele aponta as ferramentas e a ordem, ou diz não com o motivo para avisar o usuário. Escrita segue o cargo de quem autorizou: cargo sem a área (por exemplo, Vendas em domínios) não escreve nela.
