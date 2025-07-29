# Análise de Acidentes de Trânsito no Recife (2020-2022) e Modelo Preditivo de Vítimas

Este projeto realiza uma análise aprofundada dos acidentes de trânsito na cidade do Recife, utilizando dados abertos da CTTU (Autarquia de Trânsito e Transporte Urbano do Recife) referentes ao período de 2020 a 2022. O estudo combina uma Análise Exploratória de Dados (EDA) para identificar padrões e tendências com a construção de um modelo de Machine Learning para prever o número de vítimas em acidentes.

##  Contexto
Acidentes de trânsito representam um grave problema de segurança pública em grandes centros urbanos. Compreender as dinâmicas dessas ocorrências é fundamental para a formulação de políticas públicas mais eficazes e para a otimização da alocação de recursos de emergência. Este projeto utiliza a ciência de dados para transformar dados brutos de acidentes em insights acionáveis e em uma ferramenta preditiva funcional.

## Fonte de Dados
Os dados utilizados foram obtidos através do portal de dados abertos da Prefeitura do Recife e compreendem os registros de acidentes de trânsito gerenciados pela CTTU entre os anos de 2020, 2021 e 2022.

* `acidentes_2020-novo.csv`
* `acidentes2021.csv`
* `acidentes2022.csv`

## Estrutura do Projeto
O trabalho foi estruturado em duas frentes principais:

### 1. Análise Exploratória de Dados (EDA)
Nesta fase, os dados dos três anos foram consolidados, limpos e tratados para garantir consistência e qualidade. A análise investigou diversas dimensões dos acidentes, buscando responder a perguntas como:
- Quais bairros concentram o maior número de ocorrências?
- Quais os dias da semana e horários de pico dos acidentes?
- Quais os tipos de veículos mais envolvidos?
- Qual o impacto de eventos externos, como a pandemia de COVID-19?

### 2. Modelagem Preditiva
Com os dados tratados e enriquecidos, o projeto avançou para a construção de um modelo de Machine Learning com o objetivo de **prever o número de vítimas** em um acidente com base em suas características (ex: localização, tipo de ocorrência, veículos envolvidos, etc.).

-   **Algoritmos Testados:** Foram avaliados diferentes modelos de regressão, incluindo `Ridge Regression`, `Random Forest` e `XGBoost`.
-   **Seleção e Otimização:** O `XGBoost` foi selecionado como o mais performático e passou por um processo de otimização de hiperparâmetros com `GridSearchCV` para maximizar sua capacidade preditiva.

## Principais Conclusões e Insights
A análise exploratória revelou padrões importantes:
* **Localização:** O bairro de **Boa Viagem** concentra o volume mais significativo de acidentes.
* **Tempo:** Os dias úteis, especialmente no **período da tarde**, representam os momentos de maior risco.
* **Veículos:** **Automóveis e motocicletas** são, de longe, os veículos com maior envolvimento nos acidentes registrados.
* **Impacto da Pandemia:** Foi observada uma queda notável no número de acidentes a partir de março de 2020, coincidindo com o início das medidas de isolamento social.

Na frente de modelagem:
* O modelo **XGBoost Otimizado** alcançou um **coeficiente de determinação (R²) de 51%**.
* Embora a métrica indique que o modelo explica cerca de metade da variabilidade no número de vítimas, ele funciona como um eficaz **sistema de triagem e priorização**. Ele é capaz de atribuir um índice de gravidade a um acidente em tempo real, permitindo que equipes de emergência (SAMU, CTTU) otimizem o despacho de recursos para os eventos de maior risco potencial.

## Tecnologias Utilizadas
* **Linguagem:** Python 3
* **Bibliotecas de Análise:** Pandas, NumPy
* **Bibliotecas de Visualização:** Matplotlib, Seaborn
* **Bibliotecas de Machine Learning:** Scikit-learn, XGBoost

## Como Utilizar
1.  Clone o repositório:
    ```bash
    git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
    ```
2.  Instale as dependências necessárias:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn xgboost
    ```
3.  Abra e execute o notebook `Acidentes_de_Trânsito_Recife_2020_2022.ipynb` em um ambiente Jupyter.

## Conclusão Final
Este projeto não apenas gerou um panorama detalhado sobre os acidentes na cidade do Recife, mas também entregou um produto de dados funcional. O modelo preditivo desenvolvido tem potencial para gerar impacto real na eficiência operacional dos serviços de emergência e, em última instância, contribuir para a mitigação das consequências dos acidentes de trânsito na cidade.
