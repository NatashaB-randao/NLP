# Classificação de Textos com BERT

Este projeto visa desenvolver um modelo de aprendizado de máquina para a classificação de textos utilizando o modelo BERT (Bidirectional Encoder Representations from Transformers). O projeto é estruturado em várias etapas, desde o carregamento dos dados até a avaliação do modelo, e é implementado em Python, utilizando bibliotecas como Transformers, Datasets e PyTorch.

## Índice

- [Visão Geral](#visão-geral)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Etapas do Projeto](#etapas-do-projeto)
- [Uso](#uso)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Visão Geral

Neste projeto, o modelo BERT é utilizado para classificar notícias em diferentes categorias utilizando o dataset AG News. O AG News é um conjunto de dados amplamente utilizado na tarefa de classificação de textos, composto por quatro categorias de notícias: World, Sports, Business e Science/Technology.

## Pré-requisitos

Antes de iniciar, você precisará ter o seguinte instalado em sua máquina:

- Python 3.7 ou superior
- pip (gerenciador de pacotes do Python)

## Instalação

Clone este repositório em sua máquina local:

```bash
git clone https://github.com/seuusuario/classificacao-textos-bert.git
cd classificacao-textos-bert
```

Instale as dependências necessárias utilizando o seguinte comando:

```bash
pip install transformers datasets scikit-learn torch
```

## Estrutura do Projeto

O projeto possui a seguinte estrutura de diretórios:

```
classificacao-textos-bert/
│
├── README.md          # Documentação do projeto
├── requirements.txt   # Dependências do projeto
├── main.ipynb        # Notebook com a implementação do projeto
└── results/           # Diretório para armazenar os resultados do treinamento
```

## Etapas do Projeto

As etapas principais do projeto são as seguintes:

1. **Importação de Bibliotecas**: Importar as bibliotecas necessárias para o projeto.
2. **Carregamento do Dataset AG News**: Carregar o dataset AG News usando a biblioteca Datasets.
3. **Pré-processamento dos Dados**: Tokenizar os dados para que possam ser utilizados pelo modelo BERT.
4. **Carregamento do Modelo BERT**: Carregar o modelo BERT pré-treinado para classificação de sequência.
5. **Preparação para o Treinamento**: Definir os argumentos de treinamento.
6. **Criando o Trainer**: Configurar o Trainer para gerenciar o treinamento do modelo.
7. **Treinamento do Modelo**: Iniciar o treinamento do modelo com os dados pré-processados.
8. **Avaliação do Modelo**: Avaliar o desempenho do modelo no conjunto de teste.
9. **Teste do Modelo**: Testar o modelo com exemplos específicos para verificar a precisão das previsões.

## Uso

Para executar o projeto, abra o arquivo `main.ipynb` em um ambiente Jupyter Notebook e siga as etapas descritas no notebook. O projeto foi estruturado de forma que cada etapa seja claramente delineada, facilitando a compreensão e a modificação do código.

## Contribuição

Contribuições são bem-vindas! Se você quiser contribuir para este projeto, siga os passos abaixo:

1. Faça um fork do repositório.
2. Crie uma branch para sua feature: `git checkout -b feature/nome-da-feature`.
3. Faça suas alterações e faça commit: `git commit -m 'Adicionando nova feature'`.
4. Envie suas alterações para o repositório remoto: `git push origin feature/nome-da-feature`.
5. Abra um Pull Request.



