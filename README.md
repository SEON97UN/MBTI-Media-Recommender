# MBTI-based Personalized Media Content Recommendation Service

This project leverages MBTI characteristics to provide personalized media content recommendations. It involves data analysis, text embedding, clustering, and recommendation system implementation.

## Project Overview

### Video on Demand (VOD) Service
VOD services provide users with a variety of video content via the internet, allowing them to select and watch content at their convenience. Popular platforms include Netflix, Disney+, and Amazon Prime Video.

### Importance of Recommendation Systems
In VOD services, recommendation systems play a crucial role by helping users find content they are likely to enjoy. They enhance user experience by:
- Providing personalized experiences.
- Improving content discoverability.
- Reducing churn rates.

### Project Goals
This project aims to use MBTI (Myers-Briggs Type Indicator) characteristics to enhance personalized recommendations in VOD services. The specific goals include:
- Improving recommendation accuracy by incorporating MBTI data.
- Increasing user satisfaction with tailored recommendations.
- Developing a differentiated recommendation system compared to traditional methods.

## Data Sources and Preprocessing
- **WatchaPedia Data**: Includes titles, genres, summaries, ratings, and the number of ratings for movies and dramas.
- **MBTI 500 Data**: Contains posts written by individuals of different MBTI types.

### Preprocessing Steps
- Selected necessary features from WatchaPedia data.
- Combined posts by MBTI type into single strings for analysis.

## Exploratory Data Analysis (EDA)
- Visualized genre distribution.
- Analyzed rating distribution and user satisfaction.
- Examined content production by country and platform distribution.

## Text Embedding
- **Model Used**: LaBSE (Language-agnostic BERT Sentence Embedding).
- Embedded both Korean content summaries and English MBTI posts into the same vector space.

## Clustering
- Applied K-means clustering to content summaries.
- Determined optimal cluster numbers using Elbow method and Silhouette score.

## Cosine Similarity Matching
- Calculated cosine similarity between content embeddings and MBTI embeddings to find the most relevant content for each MBTI type.

## Visualization
- Used UMAP for 3D visualization of MBTI text embeddings and content embeddings.

## Recommendation System
- Developed a hybrid system combining MBTI-based embeddings, content similarity, and GBM predictions.
- Evaluated using NDCG@k, achieving a mean NDCG@20 score of 0.6206.

## How to Use
1. **Preprocessing**: Run `Preprocessing_EDA_Clustering.ipynb` to preprocess data and perform EDA.
2. **Keyword Analysis**: Run `CBF_Keyword.ipynb` for content-based filtering using keywords.
3. **Recommendation**: Run `MVTI_Recommendation.ipynb` to generate personalized recommendations based on MBTI characteristics.

## Results
- The system effectively provides personalized recommendations based on users' MBTI types.
- Visualizations show clear distinctions between different MBTI types and their content preferences.

## Future Work
- Further tuning of recommendation algorithms.
- Integrating additional data sources like user behavior and social media data.
- Developing a real-time recommendation system.

## Repository Structure
```plaintext
|-- data/
    |-- MBTI 500.csv
    |-- media_data.csv
|-- notebooks/
    |-- CBF_Keyword.ipynb
    |-- MVTI_Recommendation.ipynb
    |-- Preprocessing_EDA_Clustering.ipynb
|-- .gitignore
|-- LICENSE
|-- README.md
|-- requirements.txt
