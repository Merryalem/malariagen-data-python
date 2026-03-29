# Machine Learning Taxon Classifier (GSoC Idea Contribution)

## Motivation
Accurate classification of Anopheles mosquito species is critical for malaria control. Current approaches rely on variant calling pipelines, which can be computationally expensive and inaccessible in low-resource settings.

## Proposed Approach
This document outlines a lightweight machine learning approach to classify mosquito samples directly from raw sequencing reads (FASTQ files).

## Method Idea

### 1. Feature Extraction
- Extract k-mer frequencies from raw FASTQ reads
- Use small k (e.g., k=5–7) for efficiency
- Normalize counts to create feature vectors

### 2. Model
- Train a supervised classifier such as:
  - Random Forest
  - eXtream Gradient Boosting
  - Gradient Boosting
  - Support Vector Machine
  - Light Gradient Boosting 
  - Logistic Regression
  - Labels: major taxa (e.g., An. gambiae, An. coluzzii, An.  Arabiensis, and An. funestus)

### 3. Advantages
- No need for full variant calling
- Lower computational cost
- Faster classification pipeline

### 4. Future Extensions
- Deep learning models (CNNs on sequence data)
- Integration into malariagen-data-python workflows
- Deployment via cloud (e.g., Google Cloud Storage)
  
### 5. Main Idea
- Develop a lightweight FASTQ-based taxonomic classifier that learns discriminative k-mer signatures across Anopheles species and integrate them into a scalable ML model, potentially benchmarking against tools like Kraken and improving performance in low-coverage or noisy data.
  
## Relevance to MalariaGEN
This approach aligns with MalariaGEN’s goal of lowering barriers to genomic data analysis and enabling scalable tools for malaria-endemic regions.
