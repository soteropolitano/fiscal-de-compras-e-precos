# Modelo de dados

## Compras

Uma linha representa uma ida ao supermercado.

```text
id_compra,data,supermercado,unidade,total_estimado,total_cupom,diferenca_total,origem_dados,link_cupom_drive,observacoes
```

## Itens

Uma linha representa um produto dentro da compra.

```text
id_item,id_compra,data,supermercado,item_original,item_normalizado,marca,categoria,quantidade,unidade,preco_anunciado,preco_prateleira,preco_cupom,total_esperado,total_cobrado,diferenca,status,promocao,fonte,observacoes
```

## Histórico de preços

Mantém os valores em uma base comparável por produto, loja e data.

```text
data,supermercado,unidade,item_normalizado,marca,categoria,quantidade_base,unidade_medida,preco_unitario,preco_total,origem,id_compra,observacoes
```

## Divergências

Separa o que precisa de atenção sem perder a relação com a compra.

```text
id_divergencia,data,supermercado,id_compra,item,valor_esperado,valor_cobrado,diferenca,tipo,status,evidencia,observacoes
```

## Estados usados

Para itens: `Pendente`, `No carrinho`, `Comprado`, `Conferido`, `OK`, `Divergência`, `Divergência provável`, `Precisa confirmar`, `Promoção não identificada` e `Item não encontrado na lista original`.

Para divergências: `Aberta`, `Conferida`, `Resolvida`, `Ignorada` e `Precisa confirmar`.

## Categorias iniciais

- Arroz, feijão, massas e grãos
- Carnes, frango e peixe
- Leite, ovos e derivados
- Hortifruti
- Limpeza
- Higiene pessoal
- Bebidas
- Padaria
- Congelados
- Enlatados e conservas
- Temperos e molhos
- Pet
- Farmácia
- Outros

A categoria serve para consulta e comparação. Ela não deve bloquear um item novo; quando necessário, o produto entra em `Outros` e pode ser reclassificado depois.
