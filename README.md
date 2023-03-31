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

