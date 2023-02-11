---
layout: page
title: Automated Lexicon Generation
description: COVID-19 lexicon generation based on BERT model.
img: assets/img/covid_bert.jpg
importance: 1
category: all
---

Natural Language Processing (NLP) models consisting of Bidirectional Encoder Representations from Transformers (BERT) have been used to extract emerging COVID-19 symptoms. However, limited research surrounding lexicon generation exists for acute and long-term COVID-19 symptoms (hereby referred to as “COVID-19 symptoms”) using NLP models from clinical notes to aid clinical decision-making. This becomes crucial as more deadly strains of COVID-19 emerge. 

To assist in clinical decision-making by extracting sequences of lexical tokens for known COVID-19 symptoms from clinical notes, this study proposed an iterative approach to fine-tune a pre-trained BERT model for Named Entity Recognition (NER). The lexicon extraction performance of this fine-tuned BERT model was examined by using the extracted lexical tokens to annotate for the presence of mentions for six prevalent COVID-19 symptoms (dyspnea, fatigue, fever, cough, headaches, and nausea) on two manually-annotated reference corpora of notes.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/covid_fine_tuning_diagram.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Process flow for BERT fine-tuning and sequences of lexical token (SLT) extraction of COVID-19 symptoms from notes.
</div>

It was observed that the lexicon generated using BERT had similar f1-score compared to the lexicon generated only by clinical experts. Hence, the proposed methodology could substantially minimize valuable clinical content expert time spent on lexicon generation while maintaining quality through streamlining the process of generating lexicon of COVID-19 symptoms present in clinical notes.

Manuscript found [here](https://drive.google.com/file/d/1FvkGWqHTw9dtjO_LvKbL8g7eQE8brrwS/view?usp=sharing). Accepted as a poster at American Medical Informatics Association 2021.  
