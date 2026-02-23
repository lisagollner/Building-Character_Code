# Building-Character: Creating a specialised multimodal corpus from a historical viennese periodical
This repository contains the material for my master thesis: Building Character - Workflow for the compilation of recurring characters in the historical satirical periodical "Die Bombe" (1871-1925). The digitaized periodical can be found in the [ANNO catalouge](https://anno.onb.ac.at/cgi-content/anno?aid=bom) of the Austrian National Library and a corresponding [dataset](https://labs.onb.ac.at/de/datasets/die-bombe/) on the ÖNBLabs website.

## About
My master thesis focuses on building a pipeline for extracting and clustering near duplicates of extracted crops from "Die Bombe", consisting of Illustrations and Editorial Cartoons. The curated corpus contains the clusters of the croppings which depict recurring characters, which have a repeated appearance in the periodical.

## Content
- Notebooks (Google Colab/Google Drive environment)
- Training Data
- Extracted Crops from "Die Bombe"
- Metadata CSV-files
- Vector Embeddings for Crops
- Corpus

## Model
For this thesis I trained a YOLOv8 model with 508 annotated pages from "Die Bombe". While the training data and the validation set (106 pages) are provided in the repository, the trained model is available on Hugginface: [adding link]
