---
title: "Dr FAQ"
excerpt: "Dr FAQ is an open-source question answering chatbot, that combines a series of frequently-asked question (FAQ) similarity matching, deep natural language processing (NLP) question answering and search. A transfer learning and evaluation study was done for my CS4248 Natural Language Processing project."
date: 2019-12-15
collection: portfolio
---

DrFAQ is a plug-and-play question answering chatbot that can be generally applied to any organiation's text corpora.

Designed and implemented a NLP Question Answering architecture using spaCy, huggingface’s BERT language model, ElasticSearch, Telegram Bot API, and hosted on Heroku.

# News
4 Mar 2021 - Transfer learning of language models alongside evaluation study is currently in progress.
13 Dec 2019 - Implementation of 4-step question-answering methodology completed.

# Objective
Given an organisation's corpus of documents, generate a chatbot to enable natural question-answering capabilities.

# Methodology
When a question is asked, the following processes are performed:
1. FAQ Question Matching using spaCy's Similarity - /match
   * From a given list of Frequently Asked Questions (FAQs), the chatbot detects similarity to the specified question and selects the best answer from the existing list.
2. NLP Question Answering using huggingface's BERT - /nlp
   * If the question asked is dissimilar to any existing FAQs, perform question answering on the knowledge base and return a sufficiently confident answer.
3. Answer Search using ElasticSearch - /search
   * If the answer is not sufficiently confident, perform a search on the document corpus and return the search results.
4. Human Intervention
   * If the search results are still not relevant, prompt a human to add the question-answer pair to the existing list of specified FAQs, or speak to a human.

# References
* explosion/spaCy - Industrial-strength Natural Language Processing (NLP) with Python and Cython
* huggingface/transformers - Transformers: State-of-the-art Natural Language Processing for TensorFlow 2.0 and Pytorch
* elastic/elasticsearch-py - Official Python low-level client for Elasticsearch
* python-telegram-bot/python-telegram-bot - Python Wrapper for Telegram Bots
* google-research/bert - TensorFlow code and pre-trained models for BERT
* BERT - Pre-training of Deep Bidirectional Transformers for Language Understanding