# Financial Performance Dashboard — Power BI

Relatório executivo em Power BI construído sobre a base **Financial Sample**, como parte da trilha Power BI Analyst da [DIO](https://www.dio.me). Projeto com 2 páginas (**Executive Overview** e **Financial Performance**), navegação por botões, segmentadores sincronizados, KPIs e bookmarks para alternância de métricas — seguindo boas práticas de modelagem estrela e DAX.

## Objetivo

Transformar a base plana Financial Sample em um relatório de leitura executiva: KPIs no topo, tendência histórica, ranking de produtos e países, análise de rentabilidade por segmento e geografia — permitindo identificar rapidamente onde o negócio está performando bem e onde há risco de margem.

## Tecnologias

- **Power BI Desktop** — modelagem, DAX e construção dos visuais
- **Power Query (M)** — transformação da base flat em modelo estrela
- **DAX** — medidas de negócio (vendas, lucro, margem, crescimento, ranking)
- **Power BI Service** — publicação e compartilhamento
- Dataset: **Financial Sample** (Microsoft, uso didático)

## Estrutura do modelo de dados

```
Fato_Vendas  (Units Sold, Sales, COGS, Profit, Discounts...)
 ├── Dim_Produto     (Product)
 ├── Dim_Pais        (Country)
 ├── Dim_Segmento    (Segment)
 └── Dim_Calendario  (Data, Ano, Mês, Trimestre)
```

Modelo estrela (star schema), com tabela de medidas dedicada (`Medidas`) contendo todas as métricas DAX do projeto: `Total Sales`, `Total Profit`, `Profit Margin %`, `Sales Growth YoY %`, `Ranking Produtos`, `Ranking Países`, entre outras — detalhamento completo em [`plano-tecnico-executive-dashboard.md`](./plano-tecnico-executive-dashboard.md).

## Páginas do relatório

**Executive Overview** — 5 KPIs (vendas, lucro, margem, unidades, crescimento YoY), tendência mensal de vendas x lucro, top 5 produtos.

**Financial Performance** — mapa de vendas por país, lucro por segmento, vendas x lucro por produto, matriz produto x segmento com margem, e um seletor com bookmarks para alternar entre Sales / Profit / Units Sold no mesmo espaço visual.

## Navegação e interatividade

- Barra de navegação fixa (Home / Executive Overview / Financial Performance) presente nas duas páginas
- 3 segmentadores sincronizados entre páginas: Ano, Segmento, País
- Bookmarks para alternar métrica (Sales/Profit/Units) sem duplicar espaço na tela

## Screenshots

> _Substituir pelos prints reais após publicar o relatório._

| Executive Overview | Financial Performance |
|---|---|
| ![Executive Overview](./screenshots/executive-overview.png) | ![Financial Performance](./screenshots/financial-performance.png) |

## Como abrir

1. Baixe `Financial Sample.xlsx` e o arquivo `.pbix` deste repositório
2. Abra o `.pbix` no Power BI Desktop
3. Se solicitado, atualize o caminho da fonte de dados (Transformar Dados → Configurações da Fonte de Dados)

## Autor

**Camilla** — Estudante de Administração (Belas Artes) e Marketing Activation Intern na Envu Brasil.
[LinkedIn](#) · [GitHub](#)
