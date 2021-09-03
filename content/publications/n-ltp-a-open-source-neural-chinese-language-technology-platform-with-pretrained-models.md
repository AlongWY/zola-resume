---
title: "N-LTP: A Open-source Neural Chinese Language Technology Platform with
  Pretrained Models"
date: 2021-08-28T11:00:37.434Z
extra:
  featured: true
  link: https://arxiv.org/abs/2009.11616
  bibtex: /media/nltp.bib
  pubtype: Article
  image: /media/acl-logo.svg

description: "An open-source neural language technology platform supporting
  six   fundamental Chinese NLP tasks: <ul>   <li>lexical analysis (Chinese word
  segmentation,   part-of-speech tagging, and named entity
  recognition)</li>   <li>syntactic parsing   (dependency
  parsing)</li>   <li>semantic parsing (semantic dependency parsing
  and   semantic role labeling)</li> </ul>"
taxonomies:
  tags:
    - EMNLP
    - Python
    - Pytorch
    - Demo
    - Chinese
---
An open-source neural language technology platform supporting six fundamental Chinese NLP tasks: 

+ lexical analysis (Chinese word segmentation, part-of-speech tagging, and named entity recognition)
+ syntactic parsing (dependency parsing)
+ semantic parsing (semantic dependency parsing and semantic role labeling). 

Unlike the existing state-of-the-art toolkits, such as Stanza, that adopt an independent model for each task, N-LTP adopts the multi-task framework by using a shared pre-trained model, which has the advantage of capturing the shared knowledge across relevant Chinese tasks. 

In addition, knowledge distillation where the single-task model teaches the multi-task model is further introduced to encourage the multi-task model to surpass its single-task teacher.

Finally, we provide a collection of easy-to-use APIs and a visualization tool to make users easier to use and view the processing results directly. To the best of our knowledge, this is the first toolkit to support six Chinese NLP fundamental tasks. 
