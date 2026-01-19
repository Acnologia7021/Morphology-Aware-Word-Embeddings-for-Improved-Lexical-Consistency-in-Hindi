# Morphology-Aware Word Embeddings for Improved Lexical Consistency in Hindi

Overview

Word embedding models such as Word2Vec treat each surface word form as an independent token, ignoring internal morphological structure. While this assumption may work reasonably well for morphologically simple languages or domains, it leads to fragmented and inconsistent representations in domains with complex word formation, such as pharmaceutical and prescription text.

This project proposes a morphology-aware word embedding framework that incorporates subword and morpheme-level information into word representations. The approach is applied to drug names, compositions, and prescription-related text to improve semantic consistency and representation quality.

The goal is to demonstrate how morphological information improves embedding quality in domain-specific NLP tasks.

Problem Statement

In prescription and pharmaceutical text:

Drug names exhibit rich morphological structure

Similar drugs appear under multiple inflected or compound forms

Rare or long-tail terms suffer from data sparsity

Standard word-level embeddings fail to share information across related forms

As a result, semantic similarity and downstream analysis based on standard embeddings become unreliable.

Objectives

Perform morphological analysis of drug and prescription text

Learn morpheme-level embeddings alongside word-level embeddings

Construct morphology-aware word representations

Compare baseline and morphology-aware embeddings

Evaluate improvements in semantic consistency

Methodology
1. Text Preprocessing

Text normalization and tokenization

Vocabulary construction from prescription text

Frequency-based filtering of rare tokens

2. Baseline Word Embedding Model

Train a Word2Vec (CBOW / Skip-gram) model on prescription text

Learn standard word-level embeddings

Use this model as a baseline for comparison

3. Morphological Segmentation

Apply rule-based or unsupervised morpheme segmentation

Decompose drug names and prescription terms into morphemes

Handle prefixes, suffixes, and compound structures

4. Morpheme Embedding Training

Train embeddings for extracted morphemes

Capture subword-level semantic regularities

Enable information sharing across related word forms

5. Morphology-Aware Embedding Construction

Word representations are computed as:

Embedding(word) = WordVector + λ × MorphemeVector

where λ controls the influence of morphological information.

6. Evaluation

Word-level similarity analysis

Morphological consistency tests

Comparison of nearest neighbors in embedding space

Visualization using dimensionality reduction (PCA / t-SNE)

Why Morphological Embeddings Matter

Reduce data sparsity for rare medical terms

Improve semantic similarity across related drug names

Produce more stable embeddings for domain-specific NLP

Essential for morphologically rich or technical vocabularies
