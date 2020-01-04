# 4. N-GRAMS

**language models(LMs)**

## 4.1 COUNTING WORDS IN CORPORA

A lemma is a set of lexical forms having the same stem, the same major part-of-speech, and the same word-sense.

The wordform is the full inflected or derived form of the word.

## 4.2 SIMPLE (UNSMOOTHED) N-GRAMS

## 4.3 TRAINING AND TEST SETS

## 4.4 EVALUATING N-GRAMS: PERPLEXITY

An **intrinsitic evaluation** metric is one which measures the quality of a model independent of any application.

**Perplexity** is the most common intrinsic evaluation metric for N-gram language models.

![4.16](4.16.png)

There is another way to think about perplexity: as the **weighted average branching factor** of a language.

The branching factor of a language is the number of possible next words that can follow any word.

## 4.5 SMOOTHING


**Laplace Smoothing**

### 4.5.2 Good-Turing Discounting

A word or N-gram (or any event) that occurs once is called a **singleton**, or a **hapax legomenon**.

We refer to the number of N-grams that occur *c* times as the frequency of frequency *c*.

![4.25](4.25.png)

![4.26](4.26.png)

![4.27](4.27.png)

### 4.5.3 Some advanced issues in Good-Turing estimation

## 4.6 INTERPOLATION

There are two ways to use this N-gram "hierarchy", **backoff** and **interpolation**. 

In backoff, if we have non-zero trigram counts, we rely solely on the trigram counts. We only “back off” to a lower order N-gram if we have zero evidence for a higher-order N-gram.

By contrast, in interpolation, we always mix the probability estimates from all the N-gram estimators, i.e., we do a weighted interpolation of trigram, bigram, and unigram counts.

![4.32](4.32.png)

## 4.7 BACKOFF

![4.35](4.35.png)

the trigram version of backoff

![4.36](4.36.png)

## 4.9 ADVANCED ISSUES IN LANGUAGE MODELING

### 4.9.1 Advanced Smoothing Methods: Kneser-Ney Smoothing


