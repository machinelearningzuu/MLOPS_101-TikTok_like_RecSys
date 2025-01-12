# MLOPS 101 : TikTok like RecSys

Welcome to the **Hands-on H&M Real-Time Personalized Recommender** open-source course! 🎉 This free course teaches you how to build and deploy a real-time personalized recommender for H&M fashion articles using cutting-edge recommender systems technology, including the **4-stage recommender architecture**, the **two-tower model design**, and the **Hopsworks AI Lakehouse**.

## Architecture

![Architecture](https://github.com/machinelearningzuu/MLOPS_101-TikTok_like_RecSys/raw/main/Architecture.jpeg)

---

## Course Lessons

1. **Lesson 1**: Building a TikTok-like recommender
2. **Lesson 2**: Feature pipelines for TikTok-like recommenders
3. **Lesson 3**: Training pipelines for TikTok-like recommenders
4. **Lesson 4**: Deploy scalable TikTok-like recommenders
5. **Lesson 5**: Using LLMs to build TikTok-like recommenders

🔗 [Learn more about the course and its outline](#).

---

## Lesson 1: Building a TikTok-like Recommender

In this lesson, you’ll learn how to:
- Design and implement a **real-time personalized recommender** using H&M fashion articles.
- Use the **two-tower embedding model** to create user and item embeddings.
- Apply the **4-stage recommender architecture** to handle millions of items with real-time recommendations.
- Leverage **MLOps best practices** with the **feature/training/inference (FTI)** architecture using the Hopsworks AI Lakehouse.

### Table of Contents
- [Introduction to the H&M Dataset](#introduction-to-the-hm-dataset)
- [Core Paradigms for Recommendations](#core-paradigms-for-recommendations)
- [The Two-Tower Embedding Model](#the-two-tower-embedding-model)
- [The 4-Stage Recommender Architecture](#the-4-stage-recommender-architecture)
- [Deploying Offline ML Pipelines](#deploying-offline-ml-pipelines)
- [Demo of the Recommender](#demo-of-the-recommender)

---

### Introduction to the H&M Dataset

We use the **H&M Personalized Fashion Recommendations Dataset**, which includes:
- `articles.csv`: Information about fashion items.
- `customers.csv`: Data on customers.
- `transactions.csv`: Customer-article interactions.

We'll focus on meaningful interactions like clicks, cart additions, and purchases to train the models.

---

### Core Paradigms for Recommendations

1. **Content-Based Filtering**: Recommends items similar to those a user has interacted with.
2. **Collaborative Filtering**: Identifies patterns in user-item interactions to suggest items.

---

### The Two-Tower Embedding Model

The **two-tower model** computes embeddings for users and items in the same vector space:
- **Customer Query Encoder**: Converts customer features to embeddings.
- **Item Candidates Encoder**: Converts item features to embeddings.

This design supports:
- **Content-Based Filtering**: Using item and customer features.
- **Collaborative Filtering**: Using customer-item interaction patterns.

---

### The 4-Stage Recommender Architecture

1. **Candidate Generation**: Retrieves relevant items from a large corpus.
2. **Filtering**: Removes irrelevant items (e.g., already purchased).
3. **Ranking**: Scores and ranks items based on user relevance.
4. **Reordering**: Presents the most personalized items to the user.

**Offline Pipeline**: Precomputes item embeddings using the two-tower model.  
**Online Pipeline**: Generates real-time recommendations.

---

### Deploying Offline ML Pipelines

Using **GitHub Actions** and the **FTI architecture**, you’ll learn to:
- Automate feature extraction and model training pipelines.
- Deploy inference pipelines for real-time recommendations.

---

### Demo of the Recommender

The complete system is demonstrated using:
- **Hopsworks**: AI Lakehouse for feature store, model registry, and inference.
- **GitHub Actions**: Orchestrates offline pipelines.
- **Streamlit**: Frontend prototype to test the recommender.

### Quick Start

Follow the instructions in the [repository documentation](#) to:
- Set up Hopsworks.
- Deploy ML pipelines using GitHub Actions.
- Test the recommender via a Streamlit-powered frontend.

---

## Next Steps

In **Lesson 2**, we’ll dive deeper into:
- Feature pipelines and how to engineer robust features for the recommender.
- Leveraging Hopsworks to manage and deploy features.

💻 Explore all lessons and code in the [GitHub repository](#).  
📫 Have questions? Feel free to ask in the discussion section!

---

### License

This project is licensed under the [MIT License](LICENSE).