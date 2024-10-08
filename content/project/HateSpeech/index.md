---
title:  CLEANSE- Hate Speech Classifier and Euphemistic Text Generator
summary: Detection of hate speech using Machine Learning and Natural Language Processing
tags:
  - Machine Learning
  - Natural Language Processing
date: '2021-05-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
  filename: stopingHate.jpg

links:
  - name: PDF
    url: BE_Project.pdf
  - icon: github
    icon_pack: fab
    name: Link
    url: https://github.com/rutvibheda/Hate_Speech_ML_NLP
  - name: IEEE Publication
    url: https://ieeexplore.ieee.org/document/9587652

---
The level of hateful and abusive comments on the Internet is growing to the point where the existing structures are not in a position to fight effectively. The quick elimination of such comments is an ineffective disciplinary step and also removes useful comments. In addition, it is also delayed.

Literature survey was conducted to know the past findings on this thereby forming the objectives: Real time classify text as toxic or non toxic to identify hatefulness and suggestion of euphemistic substitution, design an algorithm to find less toxic substitution for a hateful phrase, measure hate objectively, reducing subjectivity and to have automatic moderator which acts before publishing.

The datasets used were:
1. Automated Hate Speech Detection and the Problem of Offensive Language Dataset: The dataset contains tweets that are annotated into 3 classes ie Hateful, Offensive and Clean. 
2. NAACL_SRW Dataset: A hate speech twitter dataset which contains 16907 tweet ids which are classified as racial, sexism, or none


METHODOLOGY

![alt text](image-3.png)


The  methods used were:

1. Semantic features like punctuation and capitalized words help determine the meaning and context of a sentence.

2. Sentiment features can be positive or negative and are used to distinguish between general negative speech and hate speech.

3. Unigram features represent frequently occurring words or expressions, which are used to analyze text for explicit hatefulness based on their minimum occurrences.

After this various machine learning models were tested with Logistic Regression giving the best accuracy was chosen.

More details can be found on our IEEE published paper - https://ieeexplore.ieee.org/document/9587652


