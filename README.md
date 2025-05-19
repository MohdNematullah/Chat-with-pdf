
# 📄 Chat with Multiple PDFs using Google Gemini & FAISS

**Chat with PDF** is a powerful Streamlit web app that lets you **interact with multiple PDFs** using **natural language**. Ask questions, get accurate answers, and explore your documents like never before — powered by **Google Gemini AI** and **FAISS**.

---

## ✨ Features

* 📤 Upload **multiple PDFs** at once
* 📚 **Extract** and **chunk** text from PDFs intelligently
* 🔍 Generate **embeddings** using **Google Gemini**
* ⚡ **FAISS vector store** for lightning-fast similarity search
* 💬 Ask questions and get **AI-powered answers** from your documents
* 🌐 Powered by **Google Gemini 2.0 Flash** via **LangChain**
* 🧑‍💻 Clean and intuitive **Streamlit interface**

---

## 🛠 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/MohdNematullah/Chat-with-pdf.git
cd chat-with-multiple-pdfs
```

### 2. Create and Activate a Virtual Environment

```bash
# macOS/Linux
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
venv\Scripts\activate
```

### 3. Install Required Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add Your Google API Key

Create a `.env` file in the root directory:

```
Google_Api_Key=your_google_api_key_here
```

---

## ▶️ Usage

### Run the App

```bash
streamlit run app.py
```

### How to Use

1. Use the **sidebar** to upload one or more PDF files
2. Click **Submit & Process** to extract and embed the content
3. Ask a question in the main input box
4. Get detailed answers based on your uploaded PDFs

---

## 🧩 Code Overview

| File/Function                | Description                                      |
| ---------------------------- | ------------------------------------------------ |
| `app.py`                     | Main Streamlit app                               |
| `get_pdf_text()`             | Extracts text from PDFs using `PyPDF2`           |
| `get_text_chunks()`          | Splits text into small, overlapping chunks       |
| `get_vector_store()`         | Builds and stores FAISS vector index from chunks |
| `get_conversational_chain()` | Loads Google Gemini model chain using LangChain  |
| `user_input()`               | Handles query input and AI responses             |

> ✅ Uses `GoogleGenerativeAIEmbeddings` and `ChatGoogleGenerativeAI` from **LangChain + Google SDK**

---

## 📦 Dependencies

* `streamlit`
* `PyPDF2`
* `langchain`
* `faiss-cpu`
* `google-generativeai`
* `python-dotenv`

---

## ⚠️ Notes

* Make sure you have a valid **Google Generative AI API key** with proper quota
* Large PDFs may take longer to process depending on size
* The FAISS index is stored locally in the `faiss_index` folder for reusability

---

## 🤝 Contributing

Open to feedback, ideas, and contributions!
Feel free to open issues or submit pull requests — whether it’s improving performance, usability, or adding new features.

---



