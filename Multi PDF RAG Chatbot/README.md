# 🧠 Multi PDF RAG Chatbot

The **Multi PDF RAG Chatbot** is an interactive, AI-powered assistant built with **Streamlit**. It allows users to upload multiple PDF documents and ask questions about their contents. The chatbot uses **Retrieval-Augmented Generation (RAG)** with **FAISS** for semantic search and a language model like **OpenAI's GPT** to deliver precise, context-aware responses.

## 🚀 Features

- 📄 **Multi-PDF Support**: Load and process multiple documents at once.
- 🧠 **RAG Architecture**: Uses semantic retrieval + language generation for accurate responses.
- ⚡ **FAISS Vector Indexing**: Enables fast and scalable similarity search over document embeddings.
- 💬 **Chat Interface**: Simple and interactive UI using Streamlit.
- 🔐 **API Key Configuration**: Easily plug in your OpenAI (or other) API key using a `.env` file.

## 📁 Project Structure

```
Multi PDF RAG Chatbot/
│
├── app.py                  # Main Streamlit application
├── requirements.txt        # Python dependencies
├── .env                    # Environment variables (e.g., API keys)
└── faiss_index/            # Folder containing vector index
    ├── index.faiss         # FAISS index for document embeddings
    └── index.pkl           # Pickled metadata (e.g., text chunks, sources)
```

## 🛠️ Setup Instructions

Follow these steps to get the project running on your machine:

### 1. Clone the Repository

```bash
git clone <repo_url>
cd "Multi PDF RAG Chatbot"
```

### 2. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Create a `.env` file in the root directory of the project and add your API key:

```env
OPENAI_API_KEY=your_openai_api_key
```

> ⚠️ Never commit your `.env` file to version control for security reasons!

### 5. Launch the Application

Start the Streamlit app with:

```bash
streamlit run app.py
```

Open your browser and go to: [http://localhost:8501](http://localhost:8501)

## 🧪 How It Works

1. PDFs are chunked into smaller text segments.
2. Each chunk is embedded using a language model (e.g., OpenAI Embeddings).
3. Chunks are stored in a **FAISS** index for fast similarity search.
4. When you ask a question, the app:
   - Retrieves the most relevant chunks
   - Feeds them into the language model
   - Returns an informed, natural language response

## 📌 Requirements

- Python 3.7+
- Streamlit
- FAISS
- OpenAI (or any other embedding-compatible) API key

> All dependencies are listed in `requirements.txt`.

## 🔧 Customization Ideas

- Switch out OpenAI API for open-source models (e.g., HuggingFace transformers)
- Add support for other file types (e.g., DOCX, TXT)
- Use LangChain or LlamaIndex to manage complex workflows


