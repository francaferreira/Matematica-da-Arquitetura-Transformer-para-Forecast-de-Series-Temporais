
---

# 📈 Forecast com Transformers: A Matemática do Futuro

> **"Attention Is All You Need"** – Este projeto é uma implementação prática e educativa da arquitetura que mudou o mundo da Inteligência Artificial, aplicada à previsão de séries temporais.

---

## 🧐 O que é este projeto?

Imagine que você precisa prever o preço do dólar ou a demanda de vendas de uma loja. Antigamente, usávamos ferramentas que olhavam apenas para o "ontem" para prever o "amanhã".

Este projeto utiliza o **Transformer**, a mesma tecnologia por trás do ChatGPT, para analisar sequências de dados. A diferença? Ele consegue olhar para **todo o histórico de uma vez** e entender quais pontos do passado realmente importam para o futuro.

---

## 🧠 O Coração do Projeto: O Artigo "Attention Is All You Need"

Em 2017, o Google publicou um [artigo científico](https://arxiv.org/abs/1706.03762) que revolucionou a IA.

### Por que ele foi tão importante aqui?

* **Mecanismo de Atenção:** Imagine ler um livro. Você não foca em todas as palavras com a mesma intensidade; você foca nas palavras-chave para entender o contexto. O modelo faz o mesmo com os números da série temporal.
* **Fim da "Memória Curta":** Modelos antigos (como LSTM) "esqueciam" o início da série. O Transformer mantém o foco no que é relevante, não importa quão longe no passado esteja.
* **Velocidade:** Ele processa dados em paralelo, sendo muito mais rápido que tecnologias anteriores.

---

## 🛠️ A Matemática por trás do Código (Explicada)

Para quem quer entender o que acontece "sob o capô", aqui está a lógica das principais partes do código:

### 1. Positional Encoding (Onde estamos no tempo?)

Como o modelo processa tudo ao mesmo tempo, ele "perde" a noção de ordem. Usamos fórmulas de **Seno e Cosseno** para criar um "carimbo de tempo" único para cada dado.


### 2. Multi-Head Attention (Vários ângulos)

O modelo divide a atenção em várias "cabeças". É como ter 8 especialistas diferentes olhando para o mesmo gráfico: um foca na tendência de alta, outro na sazonalidade, outro nos ruídos, e depois eles combinam suas opiniões.

### 3. Otimização e Perda (Ajuste fino)

Usamos a função de erro **MSE (Mean Squared Error)** para medir o quão longe nossa previsão está do valor real e o otimizador **Adam** para ajustar a matemática do modelo até que ele aprenda o padrão.

---

## 🚀 Como o Projeto funciona?

1. **Geração de Dados:** Criamos uma "onda" matemática complexa com ruídos (simulando o mundo real).
2. **Tratamento:** Normalizamos os dados para que o modelo não se confunda com números muito grandes.
3. **Treinamento:** O Transformer estuda os padrões dessa onda.
4. **Forecast (Previsão):** O modelo projeta os próximos passos da série temporal que ele nunca viu antes.

---

## 📂 Estrutura do Repositório

* `Projeto4.ipynb`: O cérebro do projeto. Contém desde a criação dos dados até a arquitetura da rede neural em **PyTorch**.
* **Visualizações:** Gráficos gerados que comparam o "Valor Real" vs "Previsão do Modelo".

---

## 💻 Pré-requisitos

Para rodar este projeto, você precisará de:

* Python 3.x
* PyTorch
* Pandas / NumPy / Matplotlib
* Scikit-Learn

---

## 🤝 Contribuições

Sinta-se à vontade para clonar, estudar e sugerir melhorias. A matemática da IA é um campo em constante evolução!

> **Status do Projeto:** Implementado com sucesso ✅ | Foco em: Padronização e Performance.

---


---

## 📊 Entendendo os Resultados (Gráficos)

Ao rodar o projeto, você verá visualizações que explicam o sucesso do modelo. Veja como interpretá-las:

1. **Série Temporal Original vs. Sintética:** O gráfico inicial mostra o sinal puro (a lógica) misturado com o "ruído" (o caos do mundo real). O objetivo do modelo é ignorar o ruído e aprender a lógica.
2. **A Curva de Aprendizado (Loss):** Se a linha de erro estiver descendo, a matemática está funcionando! O modelo está ajustando seus pesos internos.
3. **Previsão (Forecast):** No gráfico final, teremos a linha de dados reais e a linha de previsão.
* **O que buscar:** A linha de previsão deve "rastrear" as oscilações da linha real, antecipando os pontos de virada (picos e vales).



---

## 🚀 Guia de Instalação e Execução (Passo a Passo)

Siga estas etapas para rodar o projeto na sua máquina:

### 1. Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio

```

### 2. Criar Ambiente Virtual (Recomendado)

```bash
python -m venv venv
# No Windows:
venv\Scripts\activate
# No Mac/Linux:
source venv/bin/activate

```

### 3. Instalar Dependências

```bash
pip install torch numpy pandas matplotlib scikit-learn jupyter

```

### 4. Rodar o Notebook

```bash
jupyter notebook Projeto4.ipynb

```

---

## 🛠️ A Matemática sob o Capô

* **Positional Encoding:** Como o tempo é linear, usamos funções senoidais para dizer ao modelo qual dado veio antes e qual veio depois.
* **Multi-Head Attention:** O modelo "foca" em diferentes padrões ao mesmo tempo (ex: um cabeçote foca na tendência de alta, outro na periodicidade semanal).
* **Normalização:** Utilizamos o `MinMaxScaler` para manter todos os números entre 0 e 1, o que evita que o modelo "exploda" matematicamente durante o treino.

---

## 📂 Estrutura de Arquivos

* `Projeto4.ipynb`: Notebook principal com a implementação completa.
* `data/`: (Opcional) Onde você pode colocar seus próprios CSVs para testar.
* `requirements.txt`: Lista de bibliotecas para instalação rápida.

---

## 🤝 Créditos e Inspiração

Este projeto foi desenvolvido como parte dos estudos avançados na **Data Science Academy (DSA)**, focado na aplicação prática da matemática para IA.

---


---

## 👤 Autor

* **Jefferson Ferreira** - *Desenvolvimento e Documentação* - [Seu GitHub](https://www.google.com/search?q=https://github.com/seu-usuario)
* **Origem do Projeto:** Conteúdo desenvolvido durante o curso de "Matemática Para Data Science, Machine Learning e IA" da **Data Science Academy (DSA)**.

---

## 📜 Licença

Este projeto está licenciado sob a Licença MIT - consulte o arquivo [LICENSE](https://www.google.com/search?q=LICENSE) para mais detalhes.

> **Nota:** O código foi desenvolvido para fins educacionais e de estudo da arquitetura Transformer.

---



