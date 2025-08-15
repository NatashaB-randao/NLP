# 🚀 IA Generativa para Otimização de Atendimento ao Cliente

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg) ![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Transformers%20%7C%20NLTK-orange.svg) ![License](https://img.shields.io/badge/License-MIT-green.svg)

### Um projeto de portfólio de Natasha Brandão

Este repositório contém o código e a documentação de um protótipo de ponta a ponta que utiliza Processamento de Linguagem Natural (NLP) e um Modelo de Linguagem Grande (LLM) para analisar e gerar respostas para tweets de atendimento ao cliente.

---

## 🎯 Visão Geral do Projeto

No cenário digital atual, empresas lidam com um volume massivo de interações de clientes em redes sociais. Este projeto aborda esse desafio, desenvolvendo um sistema de IA que classifica a intenção e o sentimento de um tweet e, em seguida, gera uma resposta contextual e apropriada, demonstrando um fluxo de trabalho completo de Ciência de Dados e IA.

## ✨ Principais Funcionalidades

*   **Classificação Automática de Intenção:** Identifica se um tweet de cliente é uma `reclamação`, `dúvida`, `elogio` ou `outro`.
*   **Análise de Sentimento:** Classifica o tom emocional de cada tweet como `positivo`, `negativo` ou `neutro` usando NLTK (VADER).
*   **Geração Contextual de Respostas:** Utiliza o modelo `gpt2` da Hugging Face com a técnica de "One-Shot Prompting" para gerar respostas coerentes.


---

## 🛠️ Stack de Tecnologias

| Biblioteca / Ferramenta      | Aplicação no Projeto                                                                                                                                                                                            |
| :--------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Pandas & NumPy**           | Utilizados para a manipulação, limpeza, filtragem e estruturação dos dados. A base de toda a análise.                                                                                                             |
| **Matplotlib & Seaborn**     | Empregados para a criação de visualizações de dados para extrair e apresentar insights durante a Análise Exploratória.                                                                                            |
| **NLTK (VADER)**             | Usado para a análise de sentimentos, sendo uma ferramenta especializada em textos de redes sociais.                                                                                                                 |
| **Transformers (Hugging Face)** | O coração da modelagem. Utilizado para carregar e executar o LLM `gpt2`, gerenciando o processo de tokenização e geração de texto.                                                                                |
| **PyTorch / TensorFlow**     | O motor computacional que roda "por baixo dos panos" da biblioteca `transformers`, realizando os cálculos em tensores e otimizando para GPU.                                                                       |
| **Jupyter/Kaggle Notebooks** | O ambiente de desenvolvimento interativo onde todo o projeto foi prototipado e documentado.                                                                                                                       |

---

## ⚙️ Como Funciona: A Metodologia

O projeto foi estruturado em um pipeline lógico de ciência de dados, **combinando técnicas de NLP clássico para análise e um LLM para geração**:

1.  **Análise Exploratória de Dados (EDA):** A análise inicial do dataset de ~3 milhões de tweets revelou que a grande maioria dos dados estava concentrada em 2017. Isso levou à decisão estratégica de filtrar o dataset para focar neste período.

2.  **Pré-processamento e Limpeza (NLP):** O texto dos tweets foi limpo, removendo ruídos como URLs, menções de usuário, hashtags e stopwords para preparar os dados para a análise.

3.  **Engenharia de Features (NLP):** **Nesta fase, técnicas de NLP foram usadas para entender e estruturar o texto, criando duas features cruciais:**
    *   `tipo_refinado`: Classifica a intenção do cliente (reclamação, dúvida, etc.) usando regras baseadas em **correspondência de palavras-chave**.
    *   `sentimento`: Classifica o tom do tweet (positivo, negativo, neutro) usando o analisador **VADER**, um modelo baseado em léxico.

4.  **Modelagem e Geração de Respostas (LLM):** **Aqui, um Modelo de Linguagem Grande foi usado para criar novo texto com base no contexto:**
    *   Após experimentação, o modelo **`gpt2`**, um LLM da família Transformer, foi escolhido por sua flexibilidade.
    *   Foi implementada uma função de geração com um prompt de **"One-Shot"**, que fornece um exemplo de alta qualidade para guiar o modelo, resultando em respostas mais coerentes e no tom correto.

---

## 🚀 Como Executar o Projeto Localmente

Para executar o dashboard interativo em sua máquina, siga os passos abaixo.

**Pré-requisitos:**
*   Python 3.9+
*   `pip` e `venv`

### 1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
cd nome-do-repositorio
```


### 2. Crie e ative um ambiente virtual:

**Para MacOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Para Windows:**
```bash
python -m venv venv
.\venv\Scripts\activate
```

### 3. Instale as dependências:
*(Nota: Crie este arquivo primeiro executando `pip freeze > requirements.txt` no seu ambiente)*

```bash
pip install -r requirements.txt
```


## 🏆 Desafios e Aprendizados

O maior desafio durante a modelagem foi a **engenharia de prompt**. A tentativa inicial com o modelo `microsoft/DialoGPT` e prompts instrucionais não gerou bons resultados, pois o modelo é muito especializado em continuar diálogos e não em seguir instruções.

A principal lição aprendida foi que a **escolha do modelo e a técnica de prompt estão intrinsecamente ligadas**. A mudança para o `gpt2` (um modelo de propósito geral) combinada com um prompt de "One-Shot" (que mostra um exemplo) foi a chave para o sucesso do projeto.

## 📈 Melhorias Futuras

- **Evoluir a Classificação de Intenção**: Substituir o classificador por regras por um modelo de Machine Learning treinado (e.g., BERT) para maior precisão.

- **Personalizar o Tom com Fine-tuning**: Realizar o ajuste fino do `gpt2` com dados específicos de uma marca para que ele aprenda seu tom de voz.

- **Integrar Modelos Maiores (via API)**: Testar a integração com APIs como GPT-4 ou Gemini para comparar a qualidade das respostas.

- **Desenvolvimento de um Dashboard Interativo**: Empacotar a solução em um dashboard com Streamlit para demonstração.

- **Análise de Custo-Benefício**: Em um contexto de negócio, analisar o impacto da automação no Tempo Médio de Resposta (TMR) e o Retorno Sobre o Investimento (ROI).

## 👤 Autor

**Natasha Brandão**
- **[LinkedIn](https://www.linkedin.com/in/natasha-brand%C3%A3o/)**
- **[GitHub](https://github.com/NatashaB-randao)**