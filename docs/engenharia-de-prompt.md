# Engenharia de prompt

O Gem foi configurado para executar um fluxo, e não apenas responder perguntas sobre uma imagem.

## Estrutura das instruções

1. identificar o tipo de material recebido;
2. extrair apenas o que está visível;
3. preservar o texto original;
4. criar uma versão normalizada para busca e comparação;
5. calcular usando quantidade, unidade e condições da promoção;
6. classificar a confiança do resultado;
7. devolver os dados no formato aceito pela planilha;
8. apresentar um resumo curto para conferência humana.

## Regras contra preenchimento inventado

- não completar preço, quantidade, marca ou data por suposição;
- marcar campos duvidosos como `Precisa confirmar`;
- fazer uma pergunta objetiva quando a resposta do usuário resolver a dúvida;
- manter o valor original mesmo após uma normalização;
- não acusar o estabelecimento quando a evidência permite apenas uma hipótese.

## Saída estruturada

A resposta foi alinhada às colunas da planilha. Isso evita uma segunda etapa manual de interpretação e facilita exportar CSV quando a gravação direta não está disponível.

## Contexto profissional

Este projeto usa LLM para leitura multimodal, triagem de evidências, normalização de dados e apoio à auditoria. A engenharia de prompt define as regras de negócio, os limites da conclusão e o contrato de saída consumido pela base de dados.

O ganho não vem de uma resposta mais longa. Vem de devolver um registro rastreável, com estado, evidência e indicação clara do que ainda precisa de uma pessoa.
