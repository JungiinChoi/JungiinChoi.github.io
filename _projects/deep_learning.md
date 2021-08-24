---
layout: project
title: 'Deep Learning Final Project'
caption: >
  Application of DNN with Multitask Learning for NLP 
  to Korean Corpus Dataset
description: >
  Application of Deep Neural Networks with Multitask Learning 
  for Natural Language Processing to Korean Corpus Dataset
date: 2 Dec 2020
image: 
  path: /assets/img/projects/deep_learning_abstract.PNG
  srcset: 
    1920w: /assets/img/projects/deep_learning_abstract.PNG
    960w:  /assets/img/projects/deep_learning_abstract.PNG
    480w:  /assets/img/projects/deep_learning_abstract.PNG
links:
  - title: Link
    url: https://qwtel.com/
sitemap: false
---

**1. Introduction**

  The goal of Natural Language Processing (NLP) is to convert human language into a computer language or mathematical expression to make it easy to manipulate. These days, NLP is widely used in information extraction, translation, search engine and human-computer interfaces. In addition, methodology to improve accuracy of NLP is now actively researched in wide area.
  
  There are tons of NLP related research and programs in English, - recently Korean NLP is being studied widely, too. One of the classic example of NLP is POS(Part of Speech) tagging which determines whether it is noun, verb, or adjective. Similarly, SRL(Semantic Role Labeling)
tagging is also an important issue because it contains structure of a sentence.

  As a result, based on paper about multitask deep learning for English NLP, I wanted to proceed SRL tagging in Korean via multitask deep learning. SRL tagging in Korean is quite difficult because Korean is agglutinative language, which means affix can change the SRL and POS of the word. Also, Korean is quite flexible with respect to the order of words. This means that even the order of words in sentence is changed randomly, the sentence is still grammatically right without change in meaning. These are big difference of Korean and English that makes slightly different NLP architecture for SRL tagging.

In section 2, I will summarize the paper about multitask deep learning for English NLP and the research’s results and discussion. In section 3, I will introduce how deep learning architecture in section 2 is applied to Korean and the difference between two models. The main goal of this paper is to increase prediction accuracy by multitask learning of jointly trained NLP tasks as the paper showed in English NLP.

