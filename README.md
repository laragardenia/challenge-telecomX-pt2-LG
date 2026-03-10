# 🤖 Challenge Telecom - Análise e Previsão de Evasão (Churn) - Parte 2

<p align="center">
  <img src="https://img.shields.io/badge/Status-Concluído-brightgreen" alt="Status Concluído">
  <img src="https://img.shields.io/badge/Python-3.x-blue" alt="Python Version">
  <img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange" alt="Scikit-Learn">
</p>

## 📋 Descrição do Projeto
Este projeto é a continuação direta do desafio de dados da empresa de Telecomunicações. Após a etapa de ETL (Parte 1), o objetivo principal desta **Parte 2** foi o desenvolvimento de **Modelagem Preditiva (Machine Learning)**. O foco central é prever o churn de clientes com base nas variáveis estruturadas, antecipando cancelamentos e extraindo inteligência de negócios para propor estratégias reais de retenção e proteção de receita.

---
> 🔙 **Nota:** Este é o segundo parte do projeto. Para ver a etapa inicial de Limpeza e Exploração de Dados (ETL), acesse o repositório do **[Telecom X - Parte 1 ](https://github.com/laragardenia/challenge-telecomX-LG)**.
---

## ✨ Preparação dos Dados e Funcionalidades
Para que os algoritmos de IA pudessem aprender corretamente, o pipeline de dados passou pelas seguintes etapas de engenharia:
- **Classificação de Variáveis:** Separação estruturada entre variáveis numéricas (como *Gasto_Mensal*) e categóricas (como *Metodo_Pagamento*).
- **Encoding:** Transformação das categorias em linguagem matemática utilizando técnicas como *Label Encoding* e variáveis Dummy/One-Hot.
- **Balanceamento de Classes (SMOTE):** Geração de dados sintéticos para equilibrar a quantidade de clientes que cancelaram (minoria) e os que ficaram (maioria), evitando viés no modelo.
- **Normalização/Padronização:** Aplicação do `StandardScaler` para colocar todas as variáveis numéricas na mesma escala matemática.
- **Separação Treino/Teste:** Divisão estratégica da base em **80% para treinamento** (estudo) e **20% para teste** (prova final/validação).

---

## 🧠 Modelagem e Justificativas
Foram treinados e comparados dois algoritmos distintos para a previsão de Churn:

1. **Regressão Logística (Baseline):** Escolhida por ser rápida e altamente interpretável. Exigiu a **padronização prévia dos dados** para que variáveis com números grandes (como o *Gasto Total*) não esmagassem o peso de variáveis menores (como *Meses de Contrato*) no cálculo matemático de distância.
2. **Random Forest (Floresta Aleatória):** Escolhido por lidar excepcionalmente bem com dados complexos e não-lineares. **Não exigiu padronização**, pois árvores de decisão atuam com regras lógicas de corte, independentemente da escala numérica. Foi o nosso **modelo vencedor**, alcançando um **Recall de 85%** na identificação de clientes propensos ao cancelamento.

---

## 📊 Insights da Análise Exploratória e Modelagem
A extração de importância das variáveis (*Feature Importance*) revelou o "DNA" da evasão:
- **Baixa Fidelidade:** O `Contrato_Mensal` desponta como o maior gatilho isolado de cancelamentos.
- **Ciclo Crítico:** A interseção entre novos clientes (poucos `Meses_Contrato`) e faturas altas (`Gasto_Mensal`) gera o maior volume de evasão.
- **Atrito Técnico:** O serviço de `Fibra Óptica` concentra uma taxa de abandono significativamente superior aos demais serviços de internet.

---

## 🛠️ Tecnologias Utilizadas

- **Python:** Linguagem base para o desenvolvimento.
- **Scikit-Learn & Imbalanced-Learn:** Para padronização, balanceamento (SMOTE), treinamento dos modelos e métricas de avaliação.
- **Pandas & NumPy:** Para manipulação de matrizes e DataFrames.
- **Matplotlib & Seaborn:** Para a plotagem de matrizes de confusão e gráficos de importância de variáveis.
- **Google Colab:** Ambiente de desenvolvimento.

---

## 📂 Estrutura do Repositório

- `TelecomX_BR_LARA_pt2.ipynb`: Notebook Jupyter contendo todo o fluxo de Machine Learning, gráficos e análises detalhadas.
- `dados_tratados_telecom.csv`: Base de dados limpa exportada da etapa anterior, pronta para consumo dos algoritmos.
- `README.md`: Documentação oficial desta etapa do projeto.

---

## 🚀 Como Executar

O projeto foi construído para ser executado no ambiente Google Colab. Para reproduzir a modelagem:

1. Faça o download dos arquivos `TelecomX_BR_LARA_pt2.ipynb` e `dados_tratados_telecom.csv`.
2. Acesse o [Google Colab](https://colab.research.google.com/) e faça o upload do notebook.
3. Certifique-se de fazer o upload do arquivo `dados_tratados_telecom.csv` no ambiente do Colab para que o Pandas possa lê-lo.
4. (Opcional) Caso o ambiente não possua, instale a biblioteca de balanceamento executando: `!pip install imbalanced-learn`.
5. Execute as células em ordem para visualizar o treinamento dos modelos, matrizes de confusão e a avaliação final.

---

## 👩‍💻 Autora

Desenvolvido por **Lara Gardenia Alves Rodrigues**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lara-gardenia/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/laragardenia)
