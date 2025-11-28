# Notez: AI-Powered PDF Study Assistant
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/parzival82003/Notez-A-book-GPT)

Notez is a powerful Streamlit application designed to transform your study and research workflow. By leveraging advanced AI models, Notez allows you to upload PDF documents and interact with them in various ways, including conversational Q&A, automated flashcard generation, and quiz creation.

This tool uses Google's Gemini-Pro model within a Retrieval-Augmented Generation (RAG) framework to provide accurate, context-aware responses based on your documents.

## Key Features

- **Interactive PDF Chat**: Ask questions in natural language and get detailed, context-aware answers extracted directly from your documents.
- **Automated Flashcard & Quiz Generation**: Automatically create questions from the text to test your knowledge and reinforce key concepts.
- **Multi-Document Support**: Upload and process multiple PDFs simultaneously to build a comprehensive knowledge base.
- **Integrated PDF Viewer**: View the content of your uploaded documents directly within the application.
- **Secure API Key Handling**: Your Google API key is handled securely using Streamlit's password input.

## How It Works

Notez processes your PDF files through the following pipeline:
1.  **Text Extraction**: Extracts raw text from uploaded PDFs using `pdfplumber`.
2.  **Text Chunking**: Splits the extracted text into smaller, manageable chunks using `LangChain`.
3.  **Vectorization**: Converts text chunks into numerical embeddings using Google's Generative AI models.
4.  **Vector Storage**: Creates a searchable `FAISS` vector store from the embeddings, which is saved locally.
5.  **Question Answering**: When a user asks a question, the system performs a similarity search on the vector store to retrieve relevant context, which is then passed to the Gemini-Pro model to generate a detailed answer.
6.  **Quiz/Flashcard Generation**: For quizzes and flashcards, it uses the `valhalla/t5-base-qa-qg-hl` model from Hugging Face to generate relevant questions from the document text.

## Getting Started

Follow these instructions to set up and run Notez on your local machine.

### Prerequisites

- Python 3.8 or higher
- A Google API Key. You can obtain one from [Google AI Studio](https://makersuite.google.com/app/apikey).

### Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/parzival82003/notez-a-book-gpt.git
    cd notez-a-book-gpt
    ```

2.  **Install the required dependencies:**
    It is recommended to create a virtual environment first.
    ```sh
    pip install streamlit PyPDF2 langchain-google-genai langchain-community faiss-cpu transformers torch pdfplumber google-api-core
    ```

### Running the Application

1.  **Launch the Streamlit app:**
    The main, most stable version of the application is `app.py`.
    ```sh
    streamlit run app.py
    ```

2.  **Use the Application:**
    - Your web browser will open with the Notez interface.
    - Enter your Google API Key in the designated password field at the top.
    - Upload one or more PDF files via the uploader. The text will be automatically extracted and displayed.
    - To use the chatbot, first create a vector index from the uploaded documents. Then, ask your questions in the input box.
    - To generate study materials, click the "Generate Flashcards" button to create questions and answers from the document's content.

## File Overview

- `app.py`: The primary, fully-featured Streamlit application. This is the recommended file to run.
- `app1.py` / `app2.py`: Iterative development versions of the main application.
- `only_chatbot.py`: A simplified version of the app focusing solely on the PDF chatbot functionality.
- `quiz_gen.py`: A standalone script for testing the question generation feature.
- `notez.py` / `chatbot_fun.py`: Earlier developmental scripts.
- `readme to run.txt`: Developer's note indicating that `app.py` or `app2.py` are the primary runnable files.