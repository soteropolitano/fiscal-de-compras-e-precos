# Regras de comparação

## Valores comparados

Cada item pode ter três referências:

- **preço anunciado:** oferta, encarte ou publicidade;
- **preço de prateleira:** valor encontrado no local do produto;
- **preço do cupom:** valor efetivamente cobrado.

O total esperado usa a melhor evidência válida para aquela compra. Uma promoção condicionada só entra no cálculo quando a condição também foi atendida.

## Promoções condicionais

Antes de apontar uma divergência, a conferência considera:

- uso de aplicativo ou clube;
- identificação por CPF;
- quantidade mínima;
- combinação de itens;
- ofertas do tipo leve e pague;
- período e unidade participante.

Quando a condição não aparece na evidência, o item recebe **Promoção não identificada** ou **Precisa confirmar**.

## Classificação

| Situação | Resultado |
| --- | --- |
| Valores conferem | `OK` |
| Texto ou número não está legível | `Precisa confirmar` |
| Há diferença e a evidência é suficiente | `Divergência` |
| Há indício, mas falta confirmação | `Divergência provável` |
| A regra da promoção não foi encontrada | `Promoção não identificada` |
| O cupom contém um item que não estava na lista | `Item não encontrado na lista original` |

## Itens por peso

Produtos por quilograma precisam ser comparados na mesma base. Quantidade, unidade, preço por quilo e total cobrado devem permanecer separados. Arredondamentos pequenos ficam registrados para não parecerem uma cobrança indevida.

## Descrições abreviadas

O texto do cupom é preservado em `item_original`. A versão compreensível fica em `item_normalizado`. Algumas abreviações previstas:

| Abreviação | Leitura |
| --- | --- |
| LT | leite |
| INT | integral |
| DESN | desnatado |
| CX | caixa |
| UN | unidade |
| KG | quilograma |
| PC ou PCT | pacote |
| FD | fardo |
| PROMO | promoção |
| DESC | desconto |
| APP | aplicativo |
| LV | leve |
| PG | pague |

A expansão ajuda na busca, mas nunca substitui o texto bruto usado como evidência.
