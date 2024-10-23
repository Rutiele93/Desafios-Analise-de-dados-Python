# Desafio 5 - Prepare seu Dataset para Modelagem de Dados

## Objetivo

Este projeto tem como objetivo aplicar técnicas de **data cleaning** e **data wrangling** para preparar uma base de dados para a modelagem. O foco está na geração de métricas RFM (Recency, Frequency, Monetary) para uma empresa de e-commerce.

## Descrição

A base de dados contém informações sobre compras realizadas em 37 países, e o desafio consiste em calcular as seguintes métricas para cada cliente:

- **R (Recency)**: Número de dias desde a última compra.
- **F (Frequency)**: Quantidade de compras realizadas pelo cliente.
- **M (Monetary)**: Valor médio gasto por compra.

## Etapas de Desenvolvimento

1. **Leitura e Inspeção dos Dados**: O arquivo `Dados.csv` foi importado e verificado quanto a inconsistências.
2. **Tratamento de Dados Nulos**: Linhas com valores nulos nas colunas relevantes foram removidas.
3. **Filtragem de Preços e Quantidades**: Valores de preços e quantidades iguais ou inferiores a zero foram filtrados.
4. **Remoção de Linhas Duplicadas**: Identificamos e removemos duplicatas de registros.
5. **Correção de Tipos de Dados**: Corrigimos os tipos de dados para garantir consistência na análise.
6. **Tratamento de Outliers**: Outliers extremos foram removidos com base em limites predefinidos para quantidade e preço.
7. **Cálculo de RFM**: As métricas RFM foram calculadas utilizando os dados filtrados e limpos.

## Como Utilizar

1. Clone o repositório:
   ```bash
   git clone https://github.com/Rutiele93/Desafios-Analise-de-dados-Python.git
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute o script para gerar o output com as métricas RFM:
   ```bash
   python desafio5.py
   ```

4. O resultado será salvo em um arquivo CSV contendo as seguintes colunas:
   - `CustomerID`
   - `Recency`
   - `Frequency`
   - `Monetary`

## Dados

O arquivo utilizado neste projeto foi fornecido pela empresa de e-commerce e contém as seguintes colunas:

- `CustomerID`: Identificação do cliente
- `Description`: Descrição do produto
- `InvoiceNo`: Número da fatura
- `StockCode`: Código do produto
- `Quantity`: Quantidade comprada
- `InvoiceDate`: Data da compra
- `UnitPrice`: Preço unitário
- `Country`: País onde a compra foi realizada

## Visualizações

Além do cálculo das métricas RFM, foram gerados gráficos como:

- **Top 10 Países** com maior valor em vendas.
- **Top 10 Produtos** mais vendidos.
- Valor de venda total por mês e por país.

## Licença

Este projeto está licenciado sob os termos da licença MIT.
