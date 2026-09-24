---
name: funis
description: Lista, cria, lê, atualiza, publica e apaga funis, páginas, colunas e domínios da UpFunnels, e substitui o conteúdo da página ou o fluxo do funil.
---

# Funis e páginas

Use só estas ferramentas: `list_funnels`, `get_funnel`, `update_funnel`, `set_funnel_flow`, `publish_funnel`, `create_funnel`, `delete_funnel`, `list_funnel_pages`, `get_page`, `update_page`, `set_page_content`, `publish_page`, `create_page`, `unpublish_page`, `delete_page`, `list_domains`, `create_domain`, `get_domain_dns_records`, `check_domain_dns`, `retry_domain`, `verify_domain_cloudfront`, `delete_domain`, `list_funnel_columns`, `create_funnel_column`, `update_funnel_column`, `reorder_funnel_columns`, `update_funnel_column_config`, `delete_funnel_column`.

`create_funnel`, `update_funnel`, `create_page` e `update_page` não gravam flowData, html nem grapesData. `set_funnel_flow` e `set_page_content` substituem o campo inteiro. Acima de 200 mil caracteres a ferramenta recusa e não recorta.

- `list_funnels` lista os funis. Não devolve o grafo.
- `get_funnel` lê um funil: nome e como os nós se ligam. Não devolve o grafo cru.
- `update_funnel` atualiza nome, descrição, categoria ou objetivo. Não publica e não mexe no grafo.
- `set_funnel_flow` substitui o campo inteiro do fluxo. Acima de 200 mil caracteres a ferramenta recusa e não recorta.
- `create_funnel` cria um funil. Não grava flowData, html nem grapesData.
- `list_funnel_pages` lista as páginas de um funil, sem o HTML.
- `get_page` lê o metadado de uma página. O conteúdo só vem recortado, se pedido.
- `update_page` atualiza nome, descrição ou caminho. O editor da UpFunnels continua dono do HTML.
- `set_page_content` substitui o campo inteiro do conteúdo. Acima de 200 mil caracteres a ferramenta recusa e não recorta.
- `create_page` cria uma página. Não grava flowData, html nem grapesData.
- `list_domains` lista os domínios. O id serve para publicar página.
- `create_domain` cria um domínio: subdomínio ou domínio personalizado.
- `get_domain_dns_records` lê os registros DNS de validação do certificado.
- `check_domain_dns` confere se o DNS do domínio já propagou.
- `retry_domain` repete a validação de um domínio em erro.
- `verify_domain_cloudfront` confere se o DNS aponta para o CloudFront.
- `list_funnel_columns` lista as colunas de um funil.
- `create_funnel_column` cria uma coluna no funil.
- `update_funnel_column` atualiza nome ou responsável da coluna.
- `reorder_funnel_columns` reordena as colunas do funil.
- `update_funnel_column_config` atualiza a configuração da coluna. Não mexe no grafo.

Antes de `set_funnel_flow`, `publish_funnel`, `set_page_content`, `publish_page`, `create_domain`, `delete_domain`, `delete_funnel`, `unpublish_page`, `delete_page` ou `delete_funnel_column`, peça confirmação ao usuário. `set_funnel_flow` substitui o campo inteiro do fluxo. `publish_funnel` publica o funil. `set_page_content` substitui o campo inteiro do conteúdo. `publish_page` publica a página num domínio que já existe. `create_domain` cria um domínio. `delete_domain` apaga o domínio. `unpublish_page` despublica a página. `delete_funnel` apaga o funil. `delete_page` apaga a página. `delete_funnel_column` apaga a coluna. Acima de 200 mil caracteres a ferramenta recusa e não recorta.
