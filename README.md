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
Com os dados tratados e enriquecidos, o projeto avançou para a construção de um modelo com o objetivo de **prever se em um acidente, haverá ou não vitimas**, com base em suas características (ex: localização, tipo de ocorrência, veículos envolvidos, etc.).

-   **Algoritmos Testados:** Foram avaliados diferentes modelos de classificação, incluindo `CatBoost` e `LightGBM`.
-   **Seleção e Otimização:** O `CatBoost` foi selecionado como o mais performático, com um **recall de 94%** para valores previstos como 1 (acidente com vítima), errando apenas 49 de 810 valores.


## Conclusão Final
Este projeto não apenas gerou um panorama detalhado sobre os acidentes na cidade do Recife, mas também entregou um produto de dados funcional. O modelo preditivo desenvolvido tem potencial para gerar impacto real na eficiência operacional dos serviços de emergência e, em última instância, contribuir para a mitigação das consequências dos acidentes de trânsito na cidade.
