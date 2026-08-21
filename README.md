# Building-Character: Creating a specialised multimodal corpus from a historical viennese periodical
This repository contains the code for my master thesis: Building Character - Workflow for the compilation of recurring characters in the historical satirical periodical "Die Bombe" (1871-1925). The digitaized periodical can be found in the [ANNO catalouge](https://anno.onb.ac.at/cgi-content/anno?aid=bom) of the Austrian National Library and a corresponding [dataset](https://labs.onb.ac.at/de/datasets/die-bombe/) on the ÖNBLabs website.

## About
A computer vision and clustering pipeline for extracting and clustering near-duplicate illustrations and editorial cartoons from *Die Bombe* to create a curated corpus of recurring characters and their source pages.

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
 - [LisaGollner/YOLOv8_trained_Bombe](https://doi.org/10.57967/hf/10080)
 - [Training-Dataset_Bombe_1871-1925](https://doi.org/10.5281/zenodo.18757852)

## Clustering
For the clustering process, vector embedding and a DBSCAN algorithm was used. For the vector embedding, the [DataComp CLIP-embedding-model](laion/CLIP-ViT-L-14-DataComp.XL-s13B-b90K) (Version: CLIP ViT-L-14) was employed.

## Corpus
The created corpus includes 90 different character groups consisting of 4785 prints distributed over 2702 pages. It is published under the CC-BY-4.0 International license on Zenodo:
[Building Character Corpus](https://doi.org/10.5281/zenodo.21918823)

## License
The code is released under the GNU Affero General Public License v3.0 (AGPL-3.0) in accordance with the requirements of the Ultralytics framework.
