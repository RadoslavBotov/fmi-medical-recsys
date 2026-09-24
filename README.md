# fmi-medical-recsys

## Introduction

This is a project for the 2025/26 course of "Knowledge Bases" under the Faculty of Mathematics and Informatics (FMI), part of Sofia University "St. Kliment Ohridski".

The primary goal is not merely to predict a probable diagnosis based on a patient's symptoms, but to generate a logically grounded medical explanation for why a given conclusion is valid. To do this we take the hybrid approach of a large-scale biomedical knowledge graph and a local large language model working together.

The knowledge graph give us our base 'truth' and is used to train a Graph Neural Network for edge prediction as well as construction paths between a patient node and a disease node. When a new patient enters the graph with their respective symptoms, the GNN predicts the edge to the most likely disease and multiple shortest paths are found between them. A LLM is used to give medical context to the predicted edge and the different found paths.

## Technologies

- jupyter
- numpy
- pandas
- matplotlib
- seaborn
- Levenshtein
- lmstudio
- networkx
- gensim
- sklearn

## Resources

The mock patient data is taken from the [Disease-Symptom Dataset](https://www.kaggle.com/datasets/dhivyeshrk/diseases-and-symptoms-dataset), while the precision medicine-oriented knowledge graph [(PrimeKG)](https://zitniklab.hms.harvard.edu/projects/PrimeKG/) was developed by Harvard and introduced in the ["Building a knowledge graph to enable precision medicine"](https://doi.org/10.1038/s41597-023-01960-3) paper. 
