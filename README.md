# Processamento-de-Linguagem-Natural-A914-N-D.S.M.-113-20242

1. Pré-processamento de Texto
O pré-processamento de texto é uma etapa crucial no PLN, pois prepara os dados brutos para análise e modelagem. Algumas das técnicas aplicadas incluem:

Limpeza de Texto: Utilizamos expressões regulares (re.sub) para remover caracteres especiais e pontuações, mantendo apenas letras e espaços. Esse processo ajuda a limpar o texto e garantir que ele seja consistente para as próximas etapas.
Tokenização: A tokenização é o processo de dividir um texto em unidades menores, chamadas de tokens (geralmente palavras). Usamos a função word_tokenize do NLTK para tokenizar as palavras do texto, facilitando a análise e processamento posterior.
Remoção de Stopwords: As stopwords são palavras que aparecem com frequência em uma língua (como "a", "o", "de"), mas que não carregam muito significado semântico para a análise. Utilizamos o corpus de stopwords do NLTK para removê-las do texto.
Lematização: A lematização é o processo de reduzir palavras para sua forma básica ou raiz (por exemplo, "gatos" se torna "gato"). Através do WordNetLemmatizer do NLTK, conseguimos aplicar essa técnica para normalizar as palavras no texto.
2. Vetorização de Texto
A vetorização de texto é uma etapa essencial no PLN, onde transformamos o texto em uma representação numérica, permitindo que algoritmos de aprendizado de máquina possam trabalhar com ele. Algumas técnicas exploradas foram:

Bag of Words (BoW): A abordagem BoW conta quantas vezes cada palavra aparece no texto e cria um vetor que representa a frequência dessas palavras. O CountVectorizer da biblioteca sklearn foi utilizado para aplicar essa técnica.
TF-IDF: O Term Frequency - Inverse Document Frequency (TF-IDF) é uma técnica de vetorização que não apenas conta a frequência das palavras, mas também considera a relevância de cada palavra no contexto de um conjunto de documentos. Utilizamos o TfidfVectorizer da mesma biblioteca para aplicar essa técnica.
3. Modelos Pré-treinados
O uso de modelos pré-treinados como o Word2Vec e FastText permite que utilizemos representações vetoriais de palavras, que foram aprendidas a partir de grandes corpora de texto. Esses modelos podem capturar relações semânticas entre palavras e são fundamentais para tarefas mais complexas no PLN, como análise de similaridade entre palavras.

Word2Vec: O modelo Word2Vec transforma palavras em vetores num espaço vetorial, de modo que palavras semanticamente semelhantes estão mais próximas nesse espaço. Utilizamos o Word2Vec para criar um modelo de palavras, onde pudemos calcular a similaridade entre palavras como "cachorro" e "gato", e explorar as palavras mais próximas de uma dada palavra.
FastText: O modelo FastText é uma variação do Word2Vec que leva em consideração sub-palavras (ou n-grams), o que o torna mais eficiente em lidar com palavras desconhecidas ou raras. Através do KeyedVectors do Gensim, conseguimos calcular a similaridade entre palavras como "gato" e "gatinhos" e descobrir as palavras mais próximas de "gato".
4. Cálculo de Similaridade
Uma das habilidades mais poderosas do PLN é a capacidade de medir a similaridade semântica entre palavras. Com os modelos como Word2Vec e FastText, conseguimos calcular a similaridade entre palavras com base nos vetores que representam essas palavras no espaço vetorial. Isso nos permite medir o quão semanticamente próximas são duas palavras, como no exemplo da similaridade entre "king" e "queen" ou entre "gato" e "gatinhos".

5. Aplicações Práticas
Essas técnicas são aplicadas em várias áreas de PLN, incluindo:

Análise de Sentimentos: Analisando a semântica de palavras em um contexto de avaliação ou opinião.
Classificação de Texto: Atribuindo rótulos a documentos com base nas palavras que aparecem neles.
Sistemas de Recomendação: Usando a similaridade entre palavras para recomendar conteúdos relacionados.
Tradução Automática: Capturando relações entre palavras de diferentes línguas.
Reconhecimento de Entidades: Identificando entidades nomeadas (como pessoas, lugares, etc.) em textos.
