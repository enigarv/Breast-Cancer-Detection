# Breast-Cancer-Detection
## Motivations
The application of **deep learning** algorithms to pathological images
of the entire slide can potentially improve accuracy and efficiency
diagnostics. The complete digitization of the microscopic evaluation of sections
of colored tissue in histopathology has become feasible in recent years thanks to
advances in slide scanning technology and cost reductions
in digital archiving. The benefits of digital pathology include diagnostics
remote, the immediate availability of archival cases and easier consultations with
expert pathologists.
## Goals
The aim of the project is to develop Deep models Learning *from scratch* and in Fine Tuning, able to make distinction
between lymph node cells affected by metastases, deriving from a breast cancer, and the healthy ones.

The developed models will then be tested on a collection of images from lymph node cells, generated ad hoc. These images will be extracted from scientific publications available on the **NCBI 2 database** regarding the topic of metastases of breast cancer.

## Data
The dataset used was published in 2018 on GitHub, but a version of it with no duplicates was made available in [Kaggle](https://www.kaggle.com/c/histopathologic-cancer-detection/data) later. The reduced version consists of $220025$ color images of size $96\times96$ extracted from histopathological scans of lymph nodes' sections.
Everything images is annotated with a binary label indicating the presence of metastatic tissue a positive label indicates that in central region of $32\times32$ contains at least one pixel of cancer cells, while a negative label indicates the absence of tumor cells in the region under analysis.

A dataset of cell images was generated through the NCBI database lymph nodes, to be used as a test set for the developed models. From the **PubMed database** we downloaded all the publications having the key of search «lymph node metastasis breast cancer». Using the **PMID**, the unique code that identifies publications, it was possible to download the relative PDF, through the `pubmed2pdf` library. All the images present have been extracted from the PDF. Through pixel analysis
content, number and color, it was possible to select those of our interest. For identify the images to keep we analyse the pixel color, their number: an abundant number of pixels belonging to the **purple** range implied that the image was a good candidate to be part of the collection.
![image](https://user-images.githubusercontent.com/79215142/230111700-a06f7f4a-f13f-448d-b077-84ae916519f3.png){width=50}

## Models
We tested two different approaches:
 - implementation of a CNN from scratch, subsequently optimized with a Bayesian Optimization method;
 - fine-tuning training of two known NN, MobileNet and EfficientNet.

The models have been trained for 50 epochs, but the training is been interrupted by the Early Stopping in case of absence of improvements.

## Results
The first CNN has obtained a $81%$ of accuracy and $71%$ of recall, while the CNN in fine tuning have obtained poor results ($\sim 70% of accuracy and recall$).
![image2](https://user-images.githubusercontent.com/79215142/230113743-8e34fa20-2ebb-496d-9769-af1b071b36fc.png){width=50}




