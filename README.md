# Análise de Sentimentos dos Comentários do Debate Eleitoral de São Paulo

## Descrição do Projeto
Este projeto realiza uma **análise de sentimentos** nos comentários do YouTube sobre o debate eleitoral de São Paulo **"Debate TV Cultura | Eleições 2024 Prefeitura de São Paulo | 15/09/2024 - AO VIVO"**, utilizando técnicas de **Processamento de Linguagem Natural (NLP)**. O objetivo principal é identificar como os espectadores reagiram ao debate, classificando os comentários em **positivos**, **negativos**, ou **neutros**, utilizando a biblioteca **VADER** ajustada com listas de palavras-chave.

## Objetivos
- Coletar comentários do vídeo do debate eleitoral **"Debate TV Cultura | Eleições 2024 Prefeitura de São Paulo | 15/09/2024 - AO VIVO"** no YouTube utilizando a **YouTube Data API v3**.
- Limpar e pré-processar os comentários para remover caracteres desnecessários, links e acentos.
- Analisar o sentimento dos comentários utilizando o **VADER** com limiares ajustados e listas de palavras-chave positivas e negativas.
- Gerar visualizações, como **nuvens de palavras** e gráficos de distribuição dos sentimentos.
- Identificar os comentários mais extremos (mais positivos e mais negativos).

## Tecnologias Utilizadas
- **Python 3.8+**
- **Google Colab**
- **YouTube Data API v3**
- **VADER Sentiment Analysis** (`vaderSentiment`)
- **WordCloud** (para visualização de palavras frequentes)
- **Matplotlib** (para gráficos)
- **Unidecode** (para remoção de acentos)
- **Regex** (para limpeza do texto)
- **Stopwords** (para remover palavras neutras)

## Descrição dos Diretórios:
* notebooks/: Contém o notebook Colab onde a análise foi feita.
* scripts/: Scripts Python que contêm funções como a limpeza de dados e análise de sentimentos.
* outputs/: Armazena gráficos gerados, como nuvens de palavras e relatórios finais.

  
## Como Executar o Projeto
### Pré-requisitos:
* Python 3.6 ou superior.
#### As seguintes bibliotecas Python instaladas:
* google-api-python-client
* vaderSentiment
* matplotlib
* wordcloud
* unidecode

### Obtenção da Chave de API do YouTube:
Para coletar os comentários, você precisará de uma chave de API do YouTube:
- Acesse o Google Cloud Console.
- Crie um projeto e ative a YouTube Data API v3.
- Gere uma chave de API.

## Executar o Projeto:
Abra o notebook no Google Colab e execute todas as células. O notebook irá:
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
- Nos comentários positivos, termos como "certo", "chance", e "educação" foram mencionados com frequência, sugerindo que os espectadores valorizaram respostas claras e propostas relacionadas à educação e mudança. Candidatos como Marçal e Marina foram elogiados diretamente.
- Nos comentários negativos, palavras como "Datena", "debate", e "violência" foram predominantes. Houve críticas direcionadas ao comportamento dos candidatos, especialmente Datena, e à forma como o debate foi conduzido. A presença de expressões como "kkk" indica que muitos trataram o evento com ironia ou desaprovação.

### Limitações da Análise
- Esta análise foi realizada com base em uma amostra de 100 comentários extraídos do vídeo do debate no YouTube. Embora os resultados forneçam tendências gerais sobre os sentimentos expressos, é importante ressaltar que:
- Amostra pequena: Apenas 100 comentários foram utilizados, o que pode não representar a totalidade das opiniões dos espectadores.
- Viés temporal: Os comentários podem estar concentrados em um momento específico do debate, influenciando os resultados.
- Assertividade do VADER: A biblioteca VADER, utilizada para análise de sentimentos, tem limitações ao lidar com o português e pode não captar nuances complexas do idioma.
Para uma análise mais completa e representativa, seria necessário coletar e processar um número maior de comentários.

