---
name: funis
description: Lista, lê, atualiza e publica funis e páginas da UpFunnels, e consulta os domínios.
---

# Funis e páginas

Use só estas ferramentas: `list_funnels`, `get_funnel`, `update_funnel`, `publish_funnel`, `list_funnel_pages`, `get_page`, `update_page`, `publish_page`, `list_domains`.

- `list_funnels` lista os funis. Não devolve o grafo.
- `get_funnel` lê um funil: nome e como os nós se ligam. Não devolve o grafo cru.
- `update_funnel` atualiza nome, descrição, categoria ou objetivo. Não publica e não mexe no grafo.
- `list_funnel_pages` lista as páginas de um funil, sem o HTML.
- `get_page` lê o metadado de uma página. O conteúdo só vem recortado, se pedido.
- `update_page` atualiza nome, descrição ou caminho. O editor da UpFunnels continua dono do HTML.
- `list_domains` lista os domínios. O id serve para publicar página.

Antes de `publish_funnel` ou `publish_page`, peça confirmação ao usuário. `publish_funnel` publica o funil. `publish_page` publica a página num domínio que já existe.
