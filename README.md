# 🚀 Modelagem Dimensional e Dashboard de E-commerce com Power BI

Este projeto consiste na criação de um modelo dimensional (Star Schema) a partir da base de dados **Financial Sample** e no desenvolvimento de um dashboard analítico no Power BI, com uso de fórmulas DAX.

---

## 📌 Objetivos

- Transformar uma tabela única em um modelo dimensional otimizado.
- Aplicar boas práticas de modelagem de dados (modelo estrela).
- Criar medidas e colunas calculadas utilizando DAX.
- Desenvolver um dashboard interativo com foco em vendas, descontos e lucratividade.

---

## 🗂️ Estrutura do Modelo

### 🔶 Tabela Fato

- **F_Vendas**
  - SK_ID
  - ID_Produto
  - Produto
  - Units Sold
  - Sales Price
  - Discount Band
  - Segment
  - Country
  - Sales Rep
  - Profit
  - Date

### 🔷 Tabelas Dimensão

- **D_Produtos**
  - ID_Produto
  - Produto
  - Média de Unidades Vendidas
  - Média de Vendas
  - Mediana de Vendas
  - Valor Máximo e Mínimo de Venda

- **D_Produtos_Detalhes**
  - ID_Produto
  - Discount Band
  - Sale Price
  - Units Sold
  - Manufacturing Price

- **D_Descontos**
  - ID_Produto
  - Discount
  - Discount Band

- **D_Detalhes**
  - Outras colunas auxiliares não categorizadas em outras dimensões

- **D_Calendário**
  - Criada com `CALENDAR()` via DAX

---

## 🧠 Fórmulas DAX Utilizadas

- `CALCULATE()`
- `AVERAGEX()`, `MEDIANX()`
- `MIN()`, `MAX()`
- `RELATED()`, `RELATEDTABLE()`
- `SWITCH()` (colunas condicionais)
- `USERELATIONSHIP()` (para múltiplos relacionamentos com datas)
- `FORMAT()`, `YEAR()`, `MONTH()` (para formatação e extração de tempo)

---

## 📊 Visões Criadas no Dashboard

- Total de Vendas, Lucro e Unidades Vendidas
- Análise por País, Segmento, Produto e Faixa de Desconto
- Comparações por período (utilizando `D_Calendário`)
- Gráficos de linha, colunas, matriz e filtros de segmentação

---

## 📌 Observações Finais
Este repositório foi criado como parte de um desafio técnico. O objetivo é demonstrar domínio em modelagem de dados, Power BI e DAX.
