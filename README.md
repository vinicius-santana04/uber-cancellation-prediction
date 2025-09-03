# 🚗 Análise e Previsão de Cancelamento de Corridas da Uber (2024)

## 📄 Descrição do Projeto

Este projeto utiliza um conjunto de dados de corridas da Uber do ano de 2024 para desenvolver um modelo de Machine Learning capaz de prever a probabilidade de uma nova reserva de viagem ser cancelada. O objetivo é transformar dados brutos em insights acionáveis e em uma ferramenta preditiva que possa, futuramente, ser usada para otimizar operações, melhorar a alocação de motoristas e aprimorar a experiência do usuário.

## 📊 Contexto do Dataset

O dataset utilizado, "Uber Ride Analytics Dataset 2024", contém informações detalhadas sobre **148.77 mil reservas**.

  * **Taxa de Sucesso:** 65.96%
  * **Taxa de Cancelamento:** 25%
      * **Cancelamentos pelo Cliente:** 19.15%
      * **Cancelamentos pelo Motorista:** 7.45%

Ele inclui colunas como status da reserva, tipo de veículo, locais, tempo de viagem, avaliações e método de pagamento.

## 🎯 Problema de Negócio

Cancelamentos de corridas representam uma ineficiência significativa para plataformas como a Uber, resultando em:

  * Perda de tempo e combustível para os motoristas.
  * Experiência frustrante para os clientes.
  * Perda de receita potencial para a plataforma.

Este projeto busca responder à seguinte pergunta: **É possível prever, no momento da reserva, quais viagens têm maior probabilidade de serem canceladas, utilizando os dados disponíveis?**

## 🛠️ Tecnologias e Bibliotecas

Este projeto foi desenvolvido utilizando Python 3 e as seguintes bibliotecas:

  * **Análise e Manipulação de Dados:** `pandas`, `numpy`
  * **Visualização de Dados:** `matplotlib`, `seaborn`
  * **Machine Learning:** `scikit-learn`
  * **(Opcional/Avançado):** `xgboost`, `lightgbm`

## 📁 Estrutura do Projeto

```
uber-cancellation-prediction/
│
├── data/
│   └── uber_dataset_2024.csv      # O dataset bruto
│
├── notebooks/
│   ├── 01_Analise_Exploratoria.ipynb  # Análise inicial e visualização dos dados
│   └── 02_Modelagem_Preditiva.ipynb # Pré-processamento, treinamento e avaliação do modelo
│
├── requirements.txt                 # Lista de dependências do projeto
└── README.md                        # Documentação do projeto (este arquivo)
```

## 🚀 Como Executar o Projeto

Siga os passos abaixo para configurar e executar este projeto localmente.

1.  **Clone o repositório:**

    ```bash
    git clone https://github.com/vinicius-santana04/uber-cancellation-prediction.git
    cd uber-cancellation-prediction
    ```

2.  **Crie um ambiente virtual (recomendado):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # No Windows: venv\Scripts\activate
    ```

3.  **Instale as dependências:**

    ```bash
    pip install -r requirements.txt
    ```

4.  **Execute os Notebooks:**
    Abra os notebooks da pasta `notebooks/` utilizando Jupyter Notebook ou Jupyter Lab para explorar o processo passo a passo.

    ```bash
    jupyter lab
    ```

## 📈 Metodologia

O fluxo de trabalho deste projeto seguiu as seguintes etapas:

1.  **Análise Exploratória de Dados (EDA):** Investigação inicial dos dados para entender a distribuição das variáveis, identificar correlações e extrair primeiros insights sobre os padrões de cancelamento.

2.  **Pré-processamento e Engenharia de Features:**

      * Limpeza de dados ausentes ou inconsistentes.
      * Criação da variável alvo (`foi_cancelado`).
      * Engenharia de features a partir de colunas de data/hora (ex: `hora_do_dia`, `dia_da_semana`).
      * Conversão de variáveis categóricas (como `Vehicle Type`) em formato numérico usando One-Hot Encoding.

3.  **Modelagem:**

      * Divisão dos dados em conjuntos de treino e teste (80/20).
      * Treinamento de um modelo de classificação. O modelo inicial utilizado foi o **Random Forest Classifier** devido à sua robustez e bom desempenho em dados tabulares.

## ✍️ Autor

  * **[Vinícius Santana]**

-----