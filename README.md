# Processamento de Linguagem Natural (PLN) - A914-N-D.S.M.-113-20242

Repositório criado por **Pedro Figueira** para a disciplina **Processamento de Linguagem Natural (PLN) - A914-N-D.S.M.-113-20242**. Este projeto explora técnicas fundamentais de **PLN**, desde o pré-processamento de texto até a aplicação de modelos pré-treinados, com exemplos práticos e detalhados.

---

## 1. Pré-processamento de Texto

O pré-processamento é uma etapa essencial para preparar dados brutos, garantindo consistência e qualidade para análise e modelagem. As principais técnicas aplicadas incluem:

### 1.1 Limpeza de Texto  
Utilizamos expressões regulares (`re.sub`) para remover caracteres especiais, pontuações e manter apenas letras e espaços, garantindo que o texto esteja padronizado.

### 1.2 Tokenização  
Através da função `word_tokenize` da biblioteca **NLTK**, dividimos o texto em unidades menores, chamadas de tokens, geralmente palavras.

### 1.3 Remoção de Stopwords  
Com o **corpus de stopwords** do **NLTK**, eliminamos palavras comuns que não contribuem significativamente para a análise semântica, como "a", "de" e "o".

### 1.4 Lematização  
Utilizamos o `WordNetLemmatizer` do **NLTK** para reduzir palavras à sua forma básica ou raiz (exemplo: "gatos" → "gato"), normalizando o texto.

---

## 2. Vetorização de Texto

Transformamos o texto em representações numéricas, permitindo a aplicação de algoritmos de aprendizado de máquina. As principais abordagens exploradas foram:

### 2.1 Bag of Words (BoW)  
Contamos a frequência de palavras em um texto, criando vetores numéricos com o `CountVectorizer` da biblioteca **sklearn**.

### 2.2 TF-IDF  
Com o `TfidfVectorizer` da **sklearn**, aplicamos a técnica **TF-IDF (Term Frequency - Inverse Document Frequency)**, que pondera a frequência das palavras e sua relevância em um conjunto de documentos.

---

## 3. Modelos Pré-treinados

Modelos como **Word2Vec** e **FastText** permitem utilizar representações vetoriais de palavras aprendidas a partir de grandes corpora, capturando relações semânticas entre palavras.

### 3.1 Word2Vec  
Criamos representações vetoriais com **Word2Vec**, onde palavras semanticamente próximas ficam mais próximas no espaço vetorial. Exemplos:  
- Similaridade: "cachorro" e "gato".  
- Palavras mais próximas de uma dada palavra.

### 3.2 FastText  
O **FastText**, uma variação do Word2Vec, considera sub-palavras (n-grams), lidando melhor com palavras raras ou desconhecidas. Usando o `KeyedVectors` do **Gensim**, calculamos similaridades como:  
- "gato" e "gatinhos".  
- Palavras mais próximas de "gato".

---

## 4. Cálculo de Similaridade

Com modelos como **Word2Vec** e **FastText**, medimos a similaridade semântica entre palavras com base em suas representações vetoriais. Exemplos:  
- Relação entre "king" e "queen".  
- Relação entre "gato" e "gatinhos".

---

## 5. Aplicações Práticas

As técnicas exploradas têm várias aplicações no PLN, incluindo:  

- **Análise de Sentimentos**: Identificando sentimentos em textos (positivo, negativo ou neutro).  
- **Classificação de Texto**: Categorizando documentos com base no conteúdo textual.  
- **Sistemas de Recomendação**: Recomendando conteúdos com base na similaridade de palavras.  
- **Tradução Automática**: Modelando relações entre palavras de diferentes idiomas.  
- **Reconhecimento de Entidades Nomeadas (NER)**: Identificando pessoas, locais e organizações em textos.

---

## Ferramentas e Bibliotecas Utilizadas

- **NLTK**: Tokenização, stopwords, lematização.  
- **sklearn**: CountVectorizer, TfidfVectorizer.  
- **Gensim**: Word2Vec, FastText.  
- **Python**: Base para o desenvolvimento das técnicas e modelos.
