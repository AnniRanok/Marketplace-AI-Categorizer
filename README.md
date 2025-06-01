
# Smart Product Categorization

This repository contains an AI-driven prototype designed for the **"Place de marché"** e-commerce platform.  
It automates the categorization of products based on both textual descriptions and product images.  
The project aims to improve scalability and user experience for both sellers and buyers.



##  Project Overview

Currently, product categorization is done manually by sellers, which is error-prone and inconsistent.  
This project explores whether product classification can be automated using machine learning techniques.

The scope includes:
- Unsupervised clustering and 2D visualization
- Supervised classification with data augmentation
- Feature extraction from both text and images
- External data enrichment using the [Edamam API](https://rapidapi.com/edamam/api/edamam-food-and-grocery-database)



## 📁 Project Structure
"""
SmartProductCategorization/
├── notebooks/ # Jupyter notebooks for exploration
├── data/ # Raw and processed data
├── features/ # Extracted feature vectors
├── models/ # Trained models
├── api_edamam/ # Edamam API queries and CSV output
├── utils/ # Utility functions
└── README.md




##  Feature Extraction

###  Text Features:
Implemented with multiple NLP approaches:
- Bag of Words (word count)
- TF-IDF
- Word2Vec (pretrained embeddings)
- BERT (sentence embeddings)
- USE (Universal Sentence Encoder)

### Image Features:
Two parallel pipelines:
- Classical feature detectors: SIFT / ORB / SURF
- Deep learning embeddings via CNN (Transfer Learning with MobileNet / ResNet)



## Clustering & Visualization

To evaluate if automatic product grouping is feasible:

- Dimensionality reduction (PCA, t-SNE)
- Clustering analysis (e.g., KMeans, DBSCAN)
- Visualization: each product as a 2D point, colored by its true category
- Validation: ARI, NMI metrics between true categories and predicted clusters



## Supervised Classification (2nd Iteration)

- Image classifier (CNN)
- Text classifier (e.g., TF-IDF + Logistic Regression)
- Combined multimodal models (optional)
- Data augmentation for generalization
- Evaluation metrics: Accuracy, F1-score, Confusion Matrix



## Edamam API Enrichment

To test the expansion into high-end grocery categories (e.g., Champagne):

- Queried **champagne** via Edamam API
- Extracted the top 10 products
- Saved in `champagne_products.csv` with:
  - `foodId`
  - `label`
  - `category`
  - `foodContentsLabel`
  - `image`



##  Project Status

 Phase 1: Feature extraction & clustering feasibility study  
 Phase 2: Classification experiments underway  
 Next: API integration + production optimization



##  Next Steps

- Benchmark classifiers against clustering performance  
- Optimize image preprocessing and augmentation strategies  
- Expand categories and datasets  
- Build a REST API for real-time inference



##  Tech Stack

- Python 3.10  
- Pandas, NumPy, Scikit-learn  
- TensorFlow / Keras  
- OpenCV  
- NLTK / SpaCy / Transformers  
- Matplotlib, Seaborn  
- Edamam API via RapidAPI



##  Contributors

This prototype was developed as part of a feasibility study for the "Place de marché" launch.  
It aims to streamline product categorization and ensure a scalable foundation for future growth.



## 📬 Contact

📧 konar.inna@gmail.com  


