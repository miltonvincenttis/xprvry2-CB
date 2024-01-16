##### Copyright (c) 2024 - Milton Vincenttis

---

### O objetivo é descobrir NLP (Natural Language Processing), processamento de Linguagem Natural.
Vamos nos basear principalmente em Apache OpenNLP e Stanford CoreNLP.

>Nota: OpenNLP foi investigado: não tem uma documentação boa, nem exemplos práticos, além de ter pouco apoio da comunidade NLP,
>ao contrário do CoreNLP que é amplamente utilizado pela comunidade NLP onde a IBM o utiliza no seu produto Cognos.

NLP significa estruturar um texto em uma lingua natural (ingles, portugues, espanhol, chines, etc) 
que é vista como desestruturada.

Como se estrutura uma linguagem natural?

O NLP utiliza algoritmos para tentar estruturar e entender o texto natural, e assim permitir ao usuário de NLP
inferir (descobrir) o que há no texto, e como poder lidar e tirar conclusões sobre o texto.

### Algoritmos utilizados no OpenNLP: Todo algoritmo visa definir probabilidades/frequencias de determinado token em alguma posição no texto desestruturado.
* ME: Maximum Entropy 
* NB: Naive Bayes     
...

Alguns frameworks/bibliotecas de NLP (ApacheNLP, Stanford CoreNLP) implementam as seguintes ferramentas para seu NLP:

* DocCat                             (OpenNLP)
  * Categorização de Documentos: Permite o NLP saber que há no texto conteudo que pertence a uma categoria de documento.
  
* Tokenization:                      (OpenNLP / CoreNLP)  
  * Quebra de um texto em seus elementos básicos, tais como palavras e pontuações. 

* Sentence Detection                 (OpenNLP / CoreNLP)
  * Detecção de sentenças: Quebra de um texto em sentenças, delimitadas por alguma pontuação default ou definida.

* POST - Part of speech taggering:   (OpenNLP / CoreNLP)
  * Etiquetagem de partes do discurso: Marcações feitas em certas partes do texto.

* Lemmatization/Stemming:            (OpenNLP / CoreNLP)
  * Redução de palavra a sua origem raiz: Lematização/Stemming: Palavra: correndo Lematização: correr / Palavra: melhores Lematização: melhor
    * Lemmatization: funciona bem e é baseada em modelo da lingua (en,es,pt,de,etc).
    * Stemming: geralmente não é muito bom, pois faz tratamento apenas das letras de uma palavra e não seu significado raiz.

* Chunker                            (OpenNLP)
  * Divide o texto em pedaços ou grupos de palavras que desempenham papéis semelhantes ou que estão semanticamente relacionadas. Cada chunk pode representar um sintagma nominal (NP), um sintagma verbal (VP), ou outras unidades gramaticais dependendo da tarefa específica.
  i.e. "O gato preto dorme tranquilamente." O Chunker poderia identificar os seguintes chunks: Chunk NP (sintagma nominal): "O gato preto" Chunk VP (sintagma verbal): "dorme tranquilamente"

* Análise Sintática: Analise do texto na linguagem do texto, em suas partes gramaticais: verbos, substantivos, verbo auxiliar, artigo, etc,
  * Parser                           (OpenNLP)

* Coreference                        (OpenNLP)
  * Referencia indiretamente elementos no texto: "Maria comprou um carro. Ela estava muito feliz com a compra." Neste caso, a resolução de coreferência associaria "ela" a "Maria", indicando que ambos se referem à mesma pessoa.
  
* NER (Name Entity Recognition):     (OpenNLP / CoreNLP)
  * O objetivo do NER é identificar e classificar entidades nomeadas em um texto, ou seja, palavras ou frases que se referem a entidades específicas do mundo real, como pessoas, organizações, locais, datas, valores numéricos, entre outros.
 
>Nota: NLP é diferente de LLM (large language models) no sentido do treinamento ser ou não supervisionado.
>LLM treinamento sem supervisão.
>NLP treinamento supervisionado.
