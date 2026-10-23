# Schema da planilha Controle de Compras e Preços

## Compras

id_compra, data, supermercado, unidade, total_estimado, total_cupom, diferenca_total, origem_dados, link_cupom_drive, observacoes

## Itens

id_item, id_compra, data, supermercado, item_original, item_normalizado, marca, categoria, quantidade, unidade, preco_anunciado, preco_prateleira, preco_cupom, total_esperado, total_cobrado, diferenca, status, promocao, fonte, observacoes

## Historico_Precos

data, supermercado, unidade, item_normalizado, marca, categoria, quantidade_base, unidade_medida, preco_unitario, preco_total, origem, id_compra, observacoes

## Divergencias

id_divergencia, data, supermercado, id_compra, item, valor_esperado, valor_cobrado, diferenca, tipo, status, evidencia, observacoes

Use este schema para gerar CSVs compatíveis ou para uma Action/API gravar linhas no Google Sheets.
