# Challenge ONE - Telecom X

Este projeto tem como objetivo analisar os dados de uma empresa de telecomunicações para entender os fatores que influenciam a **evasão de clientes (Churn)**. A partir dessa análise, foram gerados insights valiosos para ajudar a empresa a reduzir a evasão e melhorar a retenção de clientes.

---

## 📋 **Descrição do Projeto**

A análise foi realizada com base em um conjunto de dados fornecido pela empresa, contendo informações sobre os clientes, como:
- **Dados demográficos** (gênero, idade, etc.).
- **Informações de contrato** (tipo de contrato, método de pagamento, etc.).
- **Serviços utilizados** (internet, telefone, etc.).
- **Cobranças** (gastos mensais e totais).

O projeto foi dividido em várias etapas, desde a **importação e limpeza dos dados** até a **análise exploratória** e a **geração de insights**.

---

## 🛠️ **Funcionalidades**

### **1. Importação e Limpeza de Dados**
- Os dados foram importados de um arquivo JSON e convertidos para um DataFrame do Pandas.
- Tratamento de valores ausentes:
  - Valores nulos na coluna `Churn` foram preenchidos com base na frequência dos valores existentes.
  - Valores ausentes em colunas numéricas, como `TotalCharges`, foram preenchidos com a média.
- Padronização de colunas categóricas:
  - Valores categóricos foram convertidos para letras minúsculas e espaços em branco foram removidos.
- Conversão de colunas:
  - A coluna `Churn` foi convertida para valores binários (`0` para "Não" e `1` para "Sim").
- Renomeação de colunas para facilitar a leitura e análise.

### **2. Análise Exploratória de Dados**
#### **Distribuição de Churn**
- Visualizações foram criadas para entender a proporção de clientes que cancelaram (`Churn = 1`) e os que não cancelaram (`Churn = 0`).
- Gráficos de barras e pizza foram utilizados para essa análise.

#### **Análise por Variáveis Categóricas**
- Foram analisadas variáveis como:
  - **Gênero:** Taxa de churn semelhante entre homens e mulheres.
  - **Tipo de Contrato:** Contratos mensais apresentaram maior taxa de churn.
  - **Método de Pagamento:** Pagamentos eletrônicos (e-check) tiveram maior taxa de churn.
  - **Serviço de Internet:** Clientes sem serviço de internet apresentaram menor taxa de churn.
- Gráficos de barras agrupados foram usados para identificar padrões.

#### **Análise por Variáveis Numéricas**
- Foram analisadas variáveis como:
  - **TotalCharges (Total Gasto):** Clientes com menor gasto total apresentaram maior taxa de churn.
  - **Tenure (Tempo de Contrato):** Clientes com menor tempo de contrato apresentaram maior taxa de churn.
  - **MonthlyCharges (Cobrança Mensal):** Clientes com cobranças mensais mais altas apresentaram maior taxa de churn.
- Boxplots e histogramas foram utilizados para visualizar as distribuições.

#### **Correlação Entre Variáveis**
- Foi calculada a matriz de correlação para identificar relações entre as variáveis numéricas e o churn.
- **Insights de correlação:**
  - `tenure` apresentou uma correlação negativa com churn, indicando que clientes com maior tempo de contrato têm menor probabilidade de cancelar.
  - `MonthlyCharges` apresentou uma correlação positiva com churn, sugerindo que cobranças mensais mais altas estão associadas a maior evasão.

### **3. Geração de Insights**
Com base na análise, os seguintes insights foram identificados:
1. **Contratos mensais** estão associados a uma maior taxa de churn.
2. **Métodos de pagamento eletrônico (e-check)** têm maior taxa de churn.
3. **Clientes com menor tempo de contrato (tenure)** são mais propensos a cancelar.
4. **Clientes com cobranças mensais mais altas** têm maior probabilidade de churn.

### **4. Exportação dos Dados**
- O DataFrame final, contendo os dados tratados e prontos para análise, foi exportado para um arquivo CSV chamado `TelecomX_Data_Processed.csv`.

---

## 📊 **Visualizações**
As visualizações geradas incluem:
- Gráficos de barras para distribuição de churn.
- Gráficos de pizza para proporção de churn.
- Boxplots para variáveis numéricas (`TotalCharges`, `tenure`, `MonthlyCharges`).
- Gráficos de barras agrupados para variáveis categóricas (`Contract`, `PaymentMethod`).
- Gráficos de dispersão para analisar a relação entre `tenure`, `MonthlyCharges` e churn.
- Heatmap da matriz de correlação para identificar relações entre variáveis.

---

## 🧠 **Conclusões**
1. **Contratos de longo prazo** são mais eficazes para reduzir a evasão.
2. **Métodos de pagamento mais convenientes** podem ajudar a reter clientes.
3. **Programas de fidelidade para novos clientes** podem reduzir a evasão inicial.
4. **Análise de clientes com cobranças altas** pode identificar insatisfações específicas.

---

## 💡 **Recomendações**
1. Incentivar contratos de longo prazo com descontos ou benefícios.
2. Melhorar a experiência de pagamento, oferecendo alternativas mais convenientes.
3. Implementar programas de retenção para clientes com menor tempo de contrato.
4. Oferecer planos personalizados para clientes com cobranças mensais altas.

---

## 📂 **Estrutura do Projeto**

Challenge-ONE---Telecom-X/ │ ├── TelecomX_Data.json # Arquivo original de dados ├── TelecomX_Data_Processed.csv # Arquivo final com os dados tratados ├── analysis_notebook.ipynb # Notebook com a análise completa ├── README.md # Documentação do projeto └── visualizations/ # Pasta para armazenar gráficos gerados.

---

## 🛠️ **Tecnologias Utilizadas**
- **Python**: Linguagem principal para análise.
- **Pandas**: Manipulação e limpeza de dados.
- **Matplotlib e Seaborn**: Criação de gráficos e visualizações.
- **Jupyter Notebook**: Ambiente para desenvolvimento e análise.

---

## 🚀 **Como Executar o Projeto**
1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/Challenge-ONE---Telecom-X.git

2. Instale as dependências necessárias:
pip install -r requirements.txt

3. Abra o notebook analysis_notebook.ipynb em um ambiente Jupyter.

4. Execute as células para reproduzir a análise.

📞 Contato
Se tiver dúvidas ou sugestões, entre em contato:

Email: dbcbr@hotmail.com
LinkedIn: www.linkedin.com/in/david-barcellos-cardoso
GitHub: https://github.com/DBCBR
Whatsapp: 21 98605-8337