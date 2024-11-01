# Product Recommendation System

## Overview
This project implements a product recommendation system that retrieves similar products based on user input. The system leverages embedding models, a vector database, and a large language model (LLM) to provide relevant product suggestions and engaging descriptions.

## Technologies Used
- **Embedding Model**: SentenceTransformer
- **Vector Database**: ChromaDB
- **Large Language Model (LLM)**: GPT-2

## Components

### 1. Embedding Model
The embedding model used in this project is **SentenceTransformer**. Specifically, we utilized the `all-MiniLM-L6-v2` model, which converts product names into fixed-size numerical representations (embeddings). These embeddings capture the semantic meaning of product names, enabling the system to identify and retrieve similar products effectively.

### 2. Vector Database
To store and manage the product embeddings efficiently, we employed **ChromaDB**. This vector database allows for quick similarity searches and retrieval of products based on their embeddings. It supports operations like upserting (inserting and updating) embeddings and querying for the nearest neighbors based on the user’s input query.

### 3. Large Language Model (LLM)
The project incorporates the **GPT-2** model from the Hugging Face Transformers library. This generative model is utilized to create descriptive text for the retrieved products. Given a product's name and its associated metadata (like price and rating), GPT-2 generates catchy and informative descriptions that enhance the user experience.

## RAG (Retrieval-Augmented Generation) Workflow
The system follows a Retrieval-Augmented Generation (RAG) approach, which combines retrieval and generation to deliver high-quality recommendations. Here’s how the RAG workflow operates:

1. **User Query Input**: 
   - The user inputs a search query (e.g., "men face cream").

2. **Retrieval Step**:
   - The system converts the user query into an embedding using the **SentenceTransformer** model.
   - It queries the **ChromaDB** to retrieve similar product embeddings based on the user query.
   - The retrieval process returns a list of relevant products along with their metadata (such as price, ratings, and number of ratings).

3. **Generation Step**:
   - For each retrieved product, the system constructs a prompt for the **GPT-2** model, incorporating the product name, price, and rating.
   - The generative model processes these prompts to produce engaging product descriptions.

4. **Output to User**:
   - The system compiles the retrieved products and their generated descriptions into a structured format.
   - The final recommendations are presented to the user, showcasing the products along with their prices, ratings, and detailed descriptions.

## Conclusion
The combination of embedding models, a vector database, and a large language model enables this product recommendation system to deliver relevant and informative suggestions, enhancing the overall user experience.

l