# Análise de Vendas 2020–2030

Projeto de análise de dados de vendas usando **SQL**, com foco em resumo anual por produto e montante total.

## Estrutura do projeto

```
curso_portfolio/
├── 001_codigos/
│   ├── 001_cria_base_vendas.sql       # DDL: cria a tabela base_vendas_2020_2030
│   ├── 002_inser_registros_vendas.sql # DML: insere registros de venda
│   └── 003_resumo_anual_vendas.sql    # Query: resumo anual agrupado por ano
├── 002_bases_dados/
│   └── 001_base_vendas_2020_2030.txt  # Base de dados bruta
├── 003_resultados/
│   └── 001_resumo_vendas_anual.xlsx   # Resultado exportado
└── 004_outros/
    └── imagem_base_dados.PNG          # Print da base de dados
```

## Modelo da tabela

```sql
CREATE TABLE base_vendas_2020_2030 (
    id_venda   INT,
    nome       STRING,
    sobrenome  STRING,
    produto    STRING,
    data_venda TIMESTAMP,
    valor      DECIMAL(16, 2)
);
```

## Resultado — Montante Anual de Vendas

| Ano  | Montante (R$)    |
|------|-----------------|
| 2021 | 54.895.368,15   |

> Os dados abrangem o período de 2020 a 2030. A query de resumo agrupa por ano e soma o montante total de vendas, ordenado cronologicamente.

## Como executar

1. Crie a tabela com `001_cria_base_vendas.sql`
2. Insira os dados com `002_inser_registros_vendas.sql`
3. Execute a análise com `003_resumo_anual_vendas.sql`

Compatível com **Apache Hive**, **SparkSQL** e **BigQuery** (função `year()`).

## Desenvolvido por

**Leandro Oliveira Moraes** — [github.com/leandroninja](https://github.com/leandroninja)
