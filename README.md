# Building-Character: Creating a specialised multimodal corpus from a historical viennese periodical
This repository contains the material for my master thesis: Building Character - Workflow for the compilation of recurring characters in the historical satirical periodical "Die Bombe" (1871-1925). The digitaized periodical can be found in the [ANNO catalouge](https://anno.onb.ac.at/cgi-content/anno?aid=bom) of the Austrian National Library and a corresponding [dataset](https://labs.onb.ac.at/de/datasets/die-bombe/) on the ÖNBLabs website.

## About
My master thesis focuses on building a pipeline for extracting and clustering near duplicates of extracted crops from "Die Bombe", consisting of Illustrations and Editorial Cartoons. The curated corpus contains the clusters of the croppings which depict recurring characters, which have a repeated appearance in the periodical as well as the pages on which they appear.

## Content
This repository contains the Pipeline-Notebooks which are intendet to be run in a Google Drive/Colab Environment.
 - Notebook-0: Download of the Pages via the API-point of the ÖNB
 - Notebook-1: Training a YOLOv8 Object Detection Model on the Layout of "Die Bombe"
 - Notebook-2: Cropping out the visual content of "Die Bombe" (target categories: "Editorial Cartoons", "Illustrations")
 - Notebook-2.5: Testing different Clustering methods an a chosen set of crops (optional)
 - Notebook-3: Vector Embedding and Clustering of extracted croppings
 - Notebook-4: Manual Curation of Clusters and final Export of the Corpus + Creation of HTML-frontend 

## Model
For this thesis I trained a YOLOv8 model with 508 annotated pages from "Die Bombe". While the training data and the validation set (106 pages) are provided in the repository, the trained model is available on Huggingface: 
 - [finetuned YOLOv8]()
 - [Training Dataset]()
