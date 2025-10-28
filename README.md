# Analise-de-cluster
Projeto de Data Science (Kaggle): Análise de comportamento de clientes para otimização de campanhas de CRM
# 📊 Análise e Segmentação de Clientes de Cartão de Crédito 

Este projeto é uma análise de dados exploratória e um exercício de *Machine Learning* (Clusterização) realizado a partir de um dataset do Kaggle sobre clientes de cartão de crédito.(https://www.kaggle.com/datasets/aryashah2k/credit-card-customer-data).

O objetivo é entender os clientes, qual é sua via de acesso ao banco (agência, interação digital - internet banking, ou apoio via canais de atendimento do banco)

---

## 🎯 1. Missão

Criar ofertas personalizadas para uma base de clientes já segmentada.

**Objetivos de Negócio:**
* Aumentar a **retenção** de clientes.
* Aumentar o **uso** dos produtos financeiros.

**Desafio da Análise:**
Identificar os perfis de clientes (segmentos) com base no seu comportamento de consumo e digital para personalizar a estratégia de comunicação.



## 🛠️ 2. Metodologia

O projeto foi dividido em três etapas principais, seguindo um fluxo de Data Science:

### a. Análise Exploratória de Dados (EDA)
* Carregamento e limpeza dos dados (`Credit Card Customer Data.csv`).
* Verificação de dados nulos e tipos de dados.
* Análise das distribuições das 5 *features* (variáveis) principais:
    1.  `Limite_medio_credito` (Valor do Cliente)
    2.  `Total_visitas_banco` (Comportamento Tradicional)
    3.  `Total_visitas_online` (Comportamento Digital)
    4.  `Total_chamadas_feitas` (Comportamento de Suporte/Custo)
    5.  `Qtd_cartoes_credito` (Adoção de Produto)

### b. Clusterização (Machine Learning)
* **Preparação:** Os dados foram normalizados com `StandardScaler` (da biblioteca `scikit-learn`) para que as diferentes escalas (ex: R$ 100k de limite vs. 5 visitas) tivessem o mesmo peso.
* **Método do Cotovelo (Elbow Method):** Foi usado para determinar o número ideal de clusters. A análise mostrou que **k=3** (três segmentos) era o ponto ideal.
* **Algoritmo K-Means:** O modelo foi treinado para agrupar os 660 clientes nos 3 segmentos descobertos.

---

## 💡 3. Os 3 Perfis de Clientes (Resultados)

A análise revelou 3 perfis de clientes distintos, com comportamentos e valor opostos:

| Perfil (Cluster) | % da Base | Limite Médio (Valor) | Comportamento Chave (Canal) | Custo |
| :--- | :--- | :--- | :--- | :--- |
| **0. O Foco-Agência** | 58% | R\$ 33.8k (Médio) | 🏦 **Visita ao Banco (3.5)** | Médio |
| **1. O Suporte Intensivo** | 34% | R\$ 12.1k (Baixo 🔻) | 📞 **Liga p/ Call Center (6.9)** | Alto 🔺 |
| **2. O Digital Premium** | 8% | R\$ 141.0k (Alto 🔺) | 💻 **Usa App/Online (10.9)** | Baixo 🔻|

### Gráficos de Perfil (Dashboard)
Os perfis foram analisados visualmente através de 5 gráficos de barras (criados no Kaggle) que comparam as médias de cada *feature* para cada cluster.

*( <img width="917" height="539" alt="image" src="https://github.com/user-attachments/assets/e0ee9dfe-1f65-4c34-afa0-e5c7bbc02251" />)*
*( <img width="880" height="542" alt="image" src="https://github.com/user-attachments/assets/72a183c0-0dcc-46f7-be85-225df42f8be0" />)*
*( <img width="877" height="540" alt="image" src="https://github.com/user-attachments/assets/4c368a6c-4a6a-4048-a5bf-10b701c1fc32" />)*
*( <img width="918" height="551" alt="image" src="https://github.com/user-attachments/assets/edc9b105-dcfd-4f56-8707-60e47bb3c315" />)*
*( <img width="901" height="560" alt="image" src="https://github.com/user-attachments/assets/9c770238-e2d8-45e8-9c59-ea4d6a97caab" />)*

*(<img width="1303" height="1275" alt="cluster_pairplot" src="https://github.com/user-attachments/assets/179ae9ac-2891-4968-803e-b673553ef409" />)*

---

## 🚀 4. Recomendações de Ação

Com base nos perfis, uma campanha "digital única" seria ineficaz (falando com apenas 8% da base). A estratégia recomendada é de 3 campanhas personalizadas:

🟢 **Para o "Digital Premium" (Foco: Retenção VIP)**
* **Ação:**Criar ofertas de upgrade com poucos cliques e dobro de pontos (por determinado tempo),
Pop-ups com ideias de investimentos baseados em seu perfil,
Utilizar IA de investimentos

🔵 **Para o "Foco-Agência" (Foco: Aumento de Uso Digital)**
* **Ação:** Aumentar e-mail marketing, SMS, propagandas na TV e até mesmo nas agências, trazendo ofertas de cashback para pagamento de boletos, de programas de pontuação como o do Pão de Açúcar e de milhas.
Incluir para essa categoria  o “fale com o gerente pelo chat”  - sempre visando a interação digital
🟠 **Para o "Focado em Atendimento" (Foco: Redução de Custo e Frustração)**
* **Ação:** Disparo de e-mail e SMS, principalmente após sua ligação, trazendo o tema de sua conversa.
Ex.: Você falou conosco sobre  sua fatura, veja onde encontrá-la  em nosso app em até um minuto.
Focar em engajar o cliente para o controle financeiro através dos cofrinhos (tendo em vista que seu limite é o menor dentre  os dois).

---

## 🔧 5. Ferramentas e Como Executar

### Ferramentas Utilizadas
* **Python 3**
* **Kaggle Notebooks**
* **Pandas:** Para manipulação de dados.
* **Scikit-learn (sklearn):** Para `StandardScaler` e `KMeans`.
* **Matplotlib & Seaborn:** Para visualização de dados.

### Como Executar o Projeto
1.  Clone este repositório: `git clone [https://github.com/Sah23lino/Analise-de-cluster.git]`
2.  Instale as dependências: `pip install -r requirements.txt`
3.  Execute o notebook Jupyter (`analise_clientes.ipynb`) ou o script Python.

---

## 👤 Autor

* **Sabrina Lino Coiado**
* **LinkedIn:** [https://www.linkedin.com/in/sabrina-lino-coiado/]
* **GitHub:** [https://github.com/Sah23lino]
