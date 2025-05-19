<<<<<<< HEAD
# Chat-with-pdf
=======
## Chat with Multiple PDFs using Google Gemini & FAISS

Welcome to Chat with Multiple PDFs, a Streamlit web application that allows you to upload multiple PDF files, process them into searchable text chunks, and then interactively ask questions about the content using Google’s Gemini AI models. The app uses FAISS for efficient similarity search on vectorized documents.

Features
Upload multiple PDFs at once and process them quickly

Extract and chunk text intelligently from PDFs

Create vector embeddings of text chunks using Google Gemini embeddings

Store and retrieve embeddings efficiently using FAISS vector store

Ask natural language questions about your PDF content and get detailed answers

Powered by the latest Google Gemini-2.0-flash language model for high-quality answers

Simple and intuitive Streamlit interface

Installation
Clone the repository:

git clone https://github.com/MohdNematullah/Chat-with-pdf.git
cd chat-with-multiple-pdfs
Create and activate a virtual environment (recommended):

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install required dependencies:

pip install -r requirements.txt
Add your Google API key to a .env file in the root directory:

Google_Api_Key=google_api_key_here
Usage
Run the Streamlit app:

streamlit run app.py
How to use the app:
Use the sidebar to upload one or more PDF files.

Click the Submit & Process button to extract text and create vector embeddings.

Enter a question related to the PDF contents in the main text input box.

Get detailed answers from the AI model based on your PDFs.

Code Overview
app.py — Main Streamlit app file

get_pdf_text() — Extracts text from uploaded PDFs using PyPDF2

get_text_chunks() — Splits long text into smaller overlapping chunks for better embedding

get_vector_store() — Creates FAISS vector store from text chunks and saves it locally

get_conversational_chain() — Creates an LLM chain for question answering using Google Gemini

user_input() — Handles user queries by searching the vector store and getting answers

Uses Google Generative AI Embeddings and ChatGoogleGenerativeAI models from langchain_google_genai

Dependencies


Streamlit

PyPDF2

LangChain

FAISS

Google Generative AI Python SDK

python-dotenv

Notes
Make sure you have a valid Google Generative AI API key and proper quota to use the Gemini models.

Large PDF files may take longer to process due to embedding and indexing.

The FAISS index is saved locally in the faiss_index folder for reusability.

Contributing
Feel free to open issues or submit pull requests. Suggestions for improving usability, performance, or extending functionality are welcome!
>>>>>>> e519b5d (Initial commit: Add chat with multiple PDFs Streamlit app)
