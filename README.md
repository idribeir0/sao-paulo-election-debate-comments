# Análise de Sentimentos dos Comentários do Debate Eleitoral de São Paulo

## Descrição do Projeto
Este projeto realiza uma **análise de sentimentos** nos comentários do YouTube sobre o debate eleitoral de São Paulo **"Debate Prefeitura de São Paulo - 1º Turno - Completo - TV Gazeta (01/09/2024)"**, utilizando técnicas de **Processamento de Linguagem Natural (NLP)**. O objetivo principal é identificar como os espectadores reagiram ao debate, classificando os comentários em **positivos**, **negativos**, ou **neutros**, utilizando a biblioteca **VADER** ajustada com listas de palavras-chave.

## Objetivos
- Coletar comentários do vídeo do debate eleitoral **"Debate Prefeitura de São Paulo - 1º Turno - Completo - TV Gazeta (01/09/2024)"** no YouTube utilizando a **YouTube Data API v3**.
- Limpar e pré-processar os comentários para remover caracteres desnecessários, links e acentos.
- Analisar o sentimento dos comentários utilizando o **VADER** com limiares ajustados e listas de palavras-chave positivas e negativas.
- Gerar visualizações, como **nuvens de palavras** e gráficos de distribuição dos sentimentos.
- Identificar os comentários mais extremos (mais positivos e mais negativos).

## Tecnologias Utilizadas
- **Python 3.8+**
- **Google Colab** ou **Jupyter Notebook**
- **YouTube Data API v3**
- **VADER Sentiment Analysis** (`vaderSentiment`)
- **WordCloud** (para visualização de palavras frequentes)
- **Matplotlib** (para gráficos)
- **Unidecode** (para remoção de acentos)
- **Regex** (para limpeza do texto)

## Estrutura do Projeto

```bash
.
├── data/               # Dados brutos (não incluídos no GitHub)
├── notebooks/          # Notebooks Jupyter/Colab (.ipynb)
├── scripts/            # Scripts Python (.py) com funções reutilizáveis
├── outputs/            # Gráficos e resultados finais
├── README.md           # Descrição do projeto
├── requirements.txt    # Lista de dependências do projeto
└── .gitignore          # Arquivos a serem ignorados pelo Git
```
## Descrição dos Diretórios:
* data/: Contém os dados brutos (se houver). Não incluído no GitHub.
* notebooks/: Contém os notebooks Jupyter/Colab onde a análise foi feita.
* scripts/: Scripts Python que contêm funções como a limpeza de dados e análise de sentimentos.
* outputs/: Armazena gráficos gerados, como nuvens de palavras e relatórios finais.
* README.md: Descrição geral do projeto.
* requirements.txt: Lista de dependências necessárias para rodar o projeto.

  
## Como Executar o Projeto
### Pré-requisitos:
* Python 3.6 ou superior.
#### As seguintes bibliotecas Python instaladas:
* google-api-python-client
* vaderSentiment
* matplotlib
* wordcloud
* unidecode

#### Instale as dependências rodando:

```bash
pip install -r requirements.txt
```

### Obtenção da Chave de API do YouTube:
Para coletar os comentários, você precisará de uma chave de API do YouTube:
- Acesse o Google Cloud Console.
- Crie um projeto e ative a YouTube Data API v3.
- Gere uma chave de API.

## Executar o Projeto:
Abra o notebook no Google Colab ou Jupyter e execute todas as células. O notebook irá:
- Coletar os comentários do vídeo do debate eleitoral.
- Limpar os dados e preparar o texto para a análise de sentimentos.
- Analisar os sentimentos usando o VADER com as listas de palavras positivas e negativas.
- Gerar gráficos e nuvens de palavras dos comentários analisados.

## Principais Funcionalidades:
- Coleta de Comentários: Os comentários são coletados do YouTube utilizando a API v3.
- Limpeza de Texto: O texto é normalizado, links são removidos, e acentos são convertidos.
- Análise de Sentimentos: O sentimento é analisado usando o VADER e ajustado por listas de palavras-chave para melhorar a precisão em português.
- Nuvens de Palavras: São geradas nuvens de palavras para visualizar os termos mais usados em comentários positivos e negativos.
- Comentários Mais Extremos: São listados os comentários com os maiores e menores scores de sentimentos.

## Resultados
#### A análise de sentimentos dos comentários do debate mostrou que:
- A maioria dos comentários negativos criticou os candidatos por "falta de propostas" e "ataques pessoais".
- Os comentários positivos tendiam a elogiar os candidatos e a apresentadora, destacando termos como "fantástica" e "ótimo".
- A nuvem de palavras revelou que os termos "marçal", "lula", e "emprego" apareceram com frequência, refletindo temas recorrentes no debate.

## Possíveis Melhorias
- Implementar uma análise de sentimento ao longo do tempo para ver como os sentimentos variam conforme o debate avança.
- Comparar a análise deste debate com outros eventos políticos ou vídeos semelhantes.
Licença
  
