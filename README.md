# 📊 Inteligência Artificial e Big Data - Análise de Ações

Este repositório contém o desenvolvimento da atividade **Somativa - SENAI**, referente à disciplina **Inteligência Artificial e Big Data** do curso de **Tecnólogo em Análise e Desenvolvimento de Sistemas**.

---

## 🎯 Objetivo
Realizar análise exploratória e aplicar o algoritmo de **aprendizado não supervisionado (K-Means)** para agrupar ações de investimento com características semelhantes.

---

## 📂 Estrutura do Projeto
- `somativa-analise-de-dados.ipynb` → Notebook com todo o código e análises.
- `base-acoes.csv` → Base de dados utilizada.
- `README.md` → Documentação do projeto.

---

## 🛠️ Tecnologias Utilizadas
- **Python 3.13.7**
- **Pandas** → Manipulação de dados
- **Seaborn / Matplotlib / Plotly** → Visualização
- **Scikit-learn** → Algoritmos de Machine Learning

> As bibliotecas são instaladas diretamente nas células do notebook (`%pip install ...`). Para facilitar o entendimento e não esquecer nenhuma, preferimos não utilizar o terminal do VSCode.

---

## 📊 Etapas do Projeto

### 1. Preparação dos Dados
- Importação da base (`nome ação`, `preço ação R$`, `qtde cotas`, `valor de mercado R$ -(Bilhões)`).
- Inspeção inicial com `df.info()` e `df.describe()`.

### 2. Renomeação das Colunas
Nesta etapa renomeamos as colunas da base de dados para nomes mais simples e consistentes,
removendo espaços e caracteres especiais.  
Isso facilita o uso das colunas em funções de análise e visualização.

```python
df.rename(columns={
    "nome ação": "nome_acao",
    "preço ação R$": "preco_acao",
    "qtde cotas": "qtde_cotas",
    "valor de mercado R$ -(Bilhões)": "valor_mercado"
}, inplace=True)

print(df.columns)
3. Exploração dos Dados
Boxplots para identificar outliers:

Preço da ação por ativo.

Valor de mercado por ativo.

Estatísticas descritivas.

4. Pré-processamento
Tratamento de valores ausentes.

Codificação de variáveis categóricas (get_dummies).

5. Agrupamento com K-Means
Aplicação do algoritmo com diferentes números de clusters (4, 5, 8).

Gráfico do cotovelo (inércia).

Gráfico da silhueta (qualidade dos clusters).

6. Visualização dos Clusters
Visualização 2D: preço vs valor de mercado.

Visualização 3D: preço vs valor de mercado vs quantidade de cotas.

📖 Reflexão Teórica
Qual a maior vantagem do aprendizado não supervisionado diante do supervisionado? 👉 Ele permite descobrir padrões ocultos e agrupamentos naturais nos dados sem necessidade de rótulos pré-definidos, sendo ideal para exploração inicial de grandes volumes de informação.


🚀 Como Executar
Clone este repositório:

bash
git clone https://github.com/LANDOSOUZA/iabd-somativa.git