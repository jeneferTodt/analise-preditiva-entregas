# SalesInsight PY

## Sobre o projeto

O **SalesInsight PY** é um projeto de análise e visualização de dados de vendas desenvolvido em Python, como parte do módulo de Desenvolvimento em IA para Análise Preditiva.

O objetivo é aplicar técnicas de programação e análise de dados para realizar a inspeção, limpeza, transformação e análise de um conjunto de dados de vendas, gerando indicadores, segmentação de clientes, visualizações gráficas e relatórios exportáveis.

O projeto foi desenvolvido no Google Colab e utiliza dados de vendas para demonstrar um fluxo de processamento estruturado, desde a preparação dos dados até a apresentação dos resultados.

## O que o projeto analisa

- Receita total e indicadores de vendas por mês e ano.
- Produtos com maior receita.
- Desempenho de vendas por categoria e região.
- Segmentação de clientes por faixa de gasto:
  - **Bronze:** receita acumulada inferior a R$ 5.000.
  - **Prata:** receita acumulada de R$ 5.000 a R$ 15.000, inclusive.
  - **Ouro:** receita acumulada superior a R$ 15.000.
- Relação entre quantidade vendida e receita.
- Distribuição da receita por faixa de valor.
- Exportação de métricas e resultados em arquivos CSV e JSON.
- Geração de gráficos em PNG para facilitar a interpretação dos resultados.

## Tecnologias e conceitos aplicados

### Python e lógica de programação

- Variáveis, tipos de dados, operadores e estruturas condicionais.
- Listas, dicionários e estruturas de dados compostas.
- Funções, parâmetros, retornos e funções lambda.
- Programação orientada a objetos com a classe `AnalisadorDeVendas`.
- Estruturas de repetição e organização do fluxo de execução.

### Manipulação e análise de dados

- **Pandas:** DataFrames, filtros, agrupamentos, transformações e análise de dados.
- **NumPy:** operações numéricas e classificação de valores.
- **Datetime:** conversão e tratamento de datas.
- **Matplotlib e Seaborn:** criação de gráficos de linha, barras, dispersão e painéis com subplots.

### Arquivos e versionamento

- Leitura e escrita de arquivos CSV e JSON.
- Exportação de gráficos em PNG.
- Git e GitHub para controle de versão.
- Organização do desenvolvimento por branches e commits.

## Como executar o projeto

### Google Colab — ambiente recomendado

O projeto foi desenvolvido para execução no Google Colab, sem necessidade de instalação local do Python.

1. Acesse o repositório público do projeto no GitHub.
2. Abra o notebook `salesinsight.ipynb` no Google Colab.
3. Execute as células na ordem apresentada no notebook, começando pelas importações e pela preparação do dataset.
4. Confira a inspeção e a limpeza dos dados, as transformações, as métricas, a segmentação de clientes e os gráficos.
5. Execute a célula da função `main()` para demonstrar o fluxo integrado, desde o carregamento dos dados até a exportação dos resultados.

O projeto utiliza bibliotecas como Pandas, NumPy, Matplotlib e Seaborn. Caso alguma delas não esteja disponível no ambiente, será necessário instalá-la antes da execução.

**Observação:** o arquivo `vendas.csv` é utilizado como dataset de entrada. Se ele não existir no ambiente, o projeto poderá gerá-lo por meio da função `gerar_dataset_vendas()`, conforme implementado no notebook.

## Estrutura do projeto

```text
salesinsight-py/
├── salesinsight.ipynb
├── graficos_insight.zip
├── vendas.csv
├── README.md
└── outputs/
    ├── metricas_por_mes.csv
    ├── segmentacao_clientes.csv
    ├── estatisticas_gerais.json
    └── graficos/
        ├── receita_por_mes.png
        ├── top_produtos.png
        ├── quantidade_vs_receita.png
        └── painel_resumo.png
```

Os arquivos da pasta `outputs/` são gerados durante o processamento. A estrutura apresentada representa os principais arquivos esperados após a execução completa do projeto.

## Decisões técnicas

### Tratamento de datas inválidas

Durante a etapa de limpeza, as datas são convertidas utilizando `pd.to_datetime()` com o parâmetro `errors="coerce"`. Valores que não podem ser convertidos são identificados como inválidos e removidos do conjunto utilizado na análise.

Essa decisão evita que registros sem datas válidas comprometam as análises temporais e os agrupamentos por mês e ano. A quantidade de registros removidos é contabilizada no relatório de limpeza, permitindo acompanhar o impacto do tratamento sobre o dataset.

### Separação das etapas de processamento

O projeto organiza o processamento em funções específicas para inspeção, limpeza, transformação, análise, segmentação, visualização e exportação. Essa estrutura facilita a manutenção, a reutilização do código e a identificação de possíveis erros durante a execução.

## Ferramentas utilizadas

- Python.
- Google Colab.
- Pandas.
- NumPy.
- Matplotlib.
- Seaborn.
- JSON e módulos nativos do Python, como `os`, `random` e `datetime`.
- Git e GitHub para versionamento e publicação do código.

## Vídeo de demonstração

**Link:** [Inserir aqui o link público do vídeo]

O vídeo apresenta o objetivo do projeto, a execução do fluxo de processamento, a organização das tarefas e branches, uma decisão técnica adotada e possíveis melhorias futuras.

## Autor

Projeto desenvolvido como atividade acadêmica do módulo de Desenvolvimento em IA para Análise Preditiva.
