---
name: funis
description: Lista, cria, lê, atualiza, publica e apaga funis, páginas e colunas da UpFunnels, e consulta os domínios.
---

# Funis e páginas

Use só estas ferramentas: `list_funnels`, `get_funnel`, `update_funnel`, `publish_funnel`, `create_funnel`, `delete_funnel`, `list_funnel_pages`, `get_page`, `update_page`, `publish_page`, `create_page`, `unpublish_page`, `delete_page`, `list_domains`, `list_funnel_columns`, `create_funnel_column`, `update_funnel_column`, `reorder_funnel_columns`, `update_funnel_column_config`, `delete_funnel_column`.

Não grave flowData, html nem grapesData. O editor da UpFunnels continua dono do grafo e do HTML.

- `list_funnels` lista os funis. Não devolve o grafo.
- `get_funnel` lê um funil: nome e como os nós se ligam. Não devolve o grafo cru.
- `update_funnel` atualiza nome, descrição, categoria ou objetivo. Não publica e não mexe no grafo.
- `create_funnel` cria um funil. Não grava flowData, html nem grapesData.
- `list_funnel_pages` lista as páginas de um funil, sem o HTML.
- `get_page` lê o metadado de uma página. O conteúdo só vem recortado, se pedido.
- `update_page` atualiza nome, descrição ou caminho. O editor da UpFunnels continua dono do HTML.
- `create_page` cria uma página. Não grava flowData, html nem grapesData.
- `list_domains` lista os domínios. O id serve para publicar página.
- `list_funnel_columns` lista as colunas de um funil.
- `create_funnel_column` cria uma coluna no funil.
- `update_funnel_column` atualiza nome ou responsável da coluna.
- `reorder_funnel_columns` reordena as colunas do funil.
- `update_funnel_column_config` atualiza a configuração da coluna. Não mexe no grafo.

Antes de `publish_funnel`, `publish_page`, `delete_funnel`, `unpublish_page`, `delete_page` ou `delete_funnel_column`, peça confirmação ao usuário. `publish_funnel` publica o funil. `publish_page` publica a página num domínio que já existe. `unpublish_page` despublica a página. `delete_funnel` apaga o funil. `delete_page` apaga a página. `delete_funnel_column` apaga a coluna.
