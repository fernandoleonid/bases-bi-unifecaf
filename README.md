# Bases de Dados: Análise de Vendas e Previsão de Demanda (E-ComTech)

Material de apoio ao trabalho **Análise de Vendas e Previsão de Demanda em um Mercado Digital**, da disciplina **Business Intelligence** (Analytics e Business Intelligence) da UniFECAF.

Responsável: Tutor Fernando Leonid.

Os dados são **fictícios**, elaborados para fins didáticos. As bases foram preparadas pela tutoria porque o enunciado cita duas bases de dados, mas não disponibiliza o link. Todos os alunos devem utilizar estes arquivos.

## Arquivos

| Arquivo | Descrição |
|---|---|
| [`Cadastro_Produtos.csv`](Cadastro_Produtos.csv) | 200 produtos da E-ComTech |
| [`Base_Vendas_2022.csv`](Base_Vendas_2022.csv) | 10.000 vendas registradas de 01/01/2022 a 31/12/2022 |

## Formato

- Separador de colunas: ponto e vírgula (`;`)
- Separador decimal: ponto (`.`)
- Datas no formato `AAAA-MM-DD`
- Codificação: UTF-8

## Relacionamento entre as bases

A chave de ligação é `id_produto`, presente nas duas bases (relação de um produto para muitas vendas).

## Dicionário de dados

### Cadastro_Produtos.csv

| Coluna | Descrição |
|---|---|
| `id_produto` | Identificador do produto |
| `nome_produto` | Nome do produto |
| `categoria` | Categoria do produto |
| `preco_venda` | Preço de venda de tabela (R$) |
| `custo_aquisicao` | Custo de aquisição (R$) |
| `fornecedor` | Fornecedor do produto |
| `prazo_entrega_dias` | Prazo de entrega do fornecedor, em dias |
| `estoque_inicial_2022` | Quantidade em estoque no início de 2022 |
| `estoque_atual` | Quantidade em estoque atualmente |
| `ativo` | Indica se o produto está ativo (Sim/Não) |

### Base_Vendas_2022.csv

| Coluna | Descrição |
|---|---|
| `id_venda` | Identificador da venda |
| `data_venda` | Data da venda |
| `id_produto` | Produto vendido |
| `quantidade` | Unidades vendidas |
| `preco_unitario` | Preço unitário **já com o desconto aplicado** (R$) |
| `desconto_percentual` | Percentual de desconto concedido |
| `valor_total` | `quantidade` × `preco_unitario` (R$) |
| `canal_venda` | Site, Marketplace ou Aplicativo |
| `promocao` | Evento ou promoção: Sem promoção, Promoção pontual, Black Friday, Natal, Dia das Mães ou Dia dos Namorados |

## Observação importante

Em `Base_Vendas_2022.csv`, o desconto já está refletido em `preco_unitario` e em `valor_total`. **Não aplique o desconto novamente** no cálculo da receita.

## Histórico de alterações

Qualquer alteração nas bases será registrada aqui, com data e motivo, e comunicada às turmas.

| Data | Alteração |
|---|---|
| 22/11/2026 | Publicação inicial das bases |
