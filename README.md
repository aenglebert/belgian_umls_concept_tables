# Custom UMLS concept for Belgium

This repo takes concepts from UMLS, the Belgian SnomedCT extension and Belgian drug names (SAM) to generate custom concept tables to be used in biomedical entity linking tasks on (Belgian) French medical corpus.

See the [concept_table_generation.ipynb](concept_table_generation.ipynb) for the whole process.

The outputs are:
- A csv file that can be used with [MedCAT](https://medcat.readthedocs.io). It includes **french** + **english** terms from UMLS + **french** terms from the Belgian SnomedCT + ATC and Belgian drug names.
- A [BRAT Normalization](https://brat.nlplab.org/normalization.html) DB file. It includes **french** + **english** terms from UMLS + **french** terms from the Belgian SnomedCT + ATC and Belgian drug names.
- A dataset of synonym pairs designed to be used to pretrain [sapBERT](https://aclanthology.org/2021.acl-short.72/). It includes **french** terms from UMLS with related **english** US SnomedCT terms (based on cui) + **french** terms from the Belgian SnomedCT + ATC and Belgian drug names.

This notebook owns a lot to this repository ( https://github.com/umcu/dutch-medical-concepts ) from the team of the UMC Utrecht to generate concepts tables for the Dutch language.
