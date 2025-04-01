# Personalized News Recommendation System Using LLaMA-3.2-1B

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Overview
This project develops a personalized news recommendation system powered by LLaMA-3.2-1B, designed to enhance accuracy, personalization, and explainability in news delivery. Using the MINDsmall dataset, the system integrates FAISS for semantic similarity search, SQLite for real-time user profiling, and a Gradio interface for user interaction. It addresses challenges like the cold-start problem and limited transparency in traditional systems by leveraging embeddings, proportional scoring, and LLM-generated explanations.

## Features
- **Semantic Search**: Generates 384D embeddings for 50,000+ MINDsmall articles using `sentence-transformers/all-MiniLM-L6-v2`.
- **Personalized Scoring**: Ranks articles based on user click history stored in SQLite.
- **Explainable Recommendations**: LLaMA-3.2-1B provides concise explanations (e.g., "Based on your preferences in sports").
- **Interactive UI**: Gradio interface delivers clickable article recommendations.
- **Hybrid Approach**: Handles cold-start (diverse suggestions) and returning users (personalized recommendations).

## System Architecture
The system integrates several components for efficient news recommendation:

![System Architecture](system_architecture.png)

- **User Input**: Query and user ID via Gradio UI.
- **SQLite**: Stores and retrieves user click history.
- **FAISS**: Indexes embeddings for fast similarity search.
- **LLaMA-3.2-1B**: Generates explanations for recommendations.
- **Gradio**: Outputs clickable article links and explanations.
 
## Results
Preliminary evaluation on 10 users achieved a category relevance score of 85%.

## Challenges 
GPU constraints, static data, and limited explanation depth with 1B-parameter LLaMA.

## Future Work
Upgrade to higher-parameter LLaMA-3 models (e.g., 7B, 13B) with fine-tuning on news data.
Integrate live data feeds (e.g., NewsAPI) for real-time updates.
Implement multi-modal fusion (text + images) using CLIP embeddings.
Enhance explainability with advanced prompt engineering.
Conduct user studies to validate diversity and satisfaction.
