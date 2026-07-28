# Desafio Power BI — Analista de Dados (DIO)

Replicação do desafio prático da trilha **Power BI Analyst** da [DIO](https://www.dio.me), baseado no repositório original de referência: [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst).

## Contexto e decisão técnica

Não tive acesso a um computador com Power BI Desktop instalado durante este desafio. Como o Power BI Service (versão web) exige um e-mail corporativo/institucional e uma experiência de autoria de relatório mais confortável em tela grande, optei por replicar as 3 páginas do desafio como um **dashboard web equivalente** (HTML/CSS/JS puro, sem dependências externas), usando o mesmo dataset (`Financial Sample`) e os mesmos princípios de storytelling visual: KPIs, hierarquia de cores, tooltips informativos e nomes de visual claros.

O objetivo do desafio — treinar a criação de visuais, nomear com clareza, definir tooltips com os campos certos e pensar a disposição do relatório — foi mantido integralmente; apenas a ferramenta de renderização mudou.

## Conteúdo do repositório

| Arquivo | Descrição |
|---|---|
| `dashboard.html` | Dashboard interativo com as 3 páginas do desafio (abrir direto no navegador) |
| `Financial_Sample.xlsx` | Base de dados original (fato de vendas) |
| `Business Unit.csv` / `Customer.csv` / `Dates.csv` | Dimensões auxiliares fornecidas no desafio |
| `relatorio_base_paginas_1_2.pbix` | Arquivo `.pbix` original do repositório da instrutora, já com as páginas 1 e 2 prontas — ponto de partida oficial do desafio, para abrir assim que eu tiver acesso a um Power BI Desktop |
| `README.md` | Este documento |

## Páginas do relatório

**01 · Visão Geral** — KPIs (vendas, lucro, unidades, margem), vendas por produto e evolução mensal de vendas x lucro.

**02 · Análise de Lucro** — lucro por produto, lucro por segmento de cliente (com destaque para o segmento Enterprise, que opera com prejuízo) e tabela-resumo com margem por segmento.

**03 · Geográfico** *(página livre do desafio)*
- **Mapa 1 — Vendas e Unidades Vendidas por País**: bolhas proporcionais ao volume de vendas; tooltip traz vendas e unidades vendidas.
- **Mapa 2 — Lucro por País**: bolhas proporcionais ao lucro; tooltip traz lucro e margem por país.
- **Pizza — Lucro por Segmento de Cliente**: participação percentual de cada segmento no lucro total.

Os nomes dos visuais foram reescritos para descrever exatamente o que cada um mostra (em vez de nomes genéricos como "Gráfico 1"), e os tooltips foram escolhidos para responder à pergunta que o visual levanta — por exemplo, o mapa de vendas mostra também unidades vendidas, e o mapa de lucro mostra a margem, não só o valor absoluto.

## Como visualizar

Baixe o repositório e abra `dashboard.html` em qualquer navegador — não precisa de instalação, servidor ou internet (exceto para carregar as fontes).

## Dataset original

Financial Sample — dataset público usado nos treinamentos oficiais de Power BI da Microsoft, disponibilizado pela instrutora no [repositório de origem](https://github.com/julianazanelatto/power_bi_analyst).

## Próximos passos

Quando eu tiver acesso a um computador com Power BI Desktop, pretendo abrir `relatorio_base_paginas_1_2.pbix`, adicionar a página 3 seguindo os mesmos critérios já aplicados aqui (mapas, pizza, tooltips e nomes de visual) e publicar o relatório via Power BI Service — mantendo este dashboard como registro do processo e como peça adicional de portfólio.
