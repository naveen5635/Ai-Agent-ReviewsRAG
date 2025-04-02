# Ai-Agent-ReviewsRAG

# Restaurant Chatbot - Installation and Setup Guide

This project is a chatbot that answers questions about a pizza restaurant based on reviews. It utilizes LangChain, Ollama LLM, and Chroma for vector storage and retrieval.

## Prerequisites
Before setting up the project, ensure you have the following installed:
- Python 3.8 or higher
- Pip (Python package manager)

## Installation
1. **Clone the repository (if applicable):**
   ```sh
   git clone https://github.com/naveen5635/Ai-Agent-ReviewsRAG.git
   cd Ai-Agent-ReviewsRAG
   ```

2. **Create and activate a virtual environment:**
   ```sh
   python -m venv venv
   source venv/bin/activate   # On macOS/Linux
   venv\Scripts\activate      # On Windows
   ```

3. **Install dependencies:**
   ```sh
   pip install -r req.txt
   ```

## Setup
1. **Prepare the dataset:**
   - Ensure you have a `reviews.csv` file in the project directory containing restaurant reviews.
   - The CSV file should have at least the following columns:
     - `Title`
     - `Review`
     - `Rating`
     - `Date`

2. **Run the chatbot:**
   ```sh
   python main.py
   ```

## How It Works
- The chatbot reads customer reviews from `reviews.csv` and indexes them in a Chroma vector database.
- It uses LangChain and Ollama LLM to generate responses based on retrieved reviews.
- You can ask questions about the restaurant, and the chatbot will provide relevant answers.

## Exiting the Chatbot
To exit the chatbot, type `x` when prompted for a question.

## Notes
- If `reviews.csv` is updated, delete the existing Chroma database (`chrome_langchain_db`) to refresh the stored data.
- Make sure `Ollama` is installed and configured correctly for embedding and inference.

## Troubleshooting
- If you encounter import errors, ensure all dependencies are installed correctly.
- If the chatbot does not retrieve relevant reviews, check the `reviews.csv` format and ensure it contains valid data.
