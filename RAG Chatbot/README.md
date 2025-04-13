# RAG-Based Academic Chatbot 🤖📚

This is a full-stack RAG (Retrieval-Augmented Generation) chatbot designed for academic support. It allows users to upload PDFs, ask questions, and receive accurate answers powered by Google's Gemini API. The app includes user login, admin dashboard, chat history, and vector-based document retrieval.

---

## 🚀 Features

- Token-based authentication (JWT)
- Academic-level query answering with Gemini AI
- RAG system using uploaded PDFs and FAISS vector index
- PDF upload and parsing support
- Chat history and session tracking
- Admin panel with user/session insights
- Modern UI built with React + Vite

---

## 🗂️ Project Structure

```
.
├── assets
├── backend
│   ├── .env
│   ├── App.py
│   ├── config.py
│   ├── database.py
│   ├── utils
│   │   ├── __init__.py
│   │   ├── jwt_helper.py
│   ├── faiss_index
│   │   ├── index.faiss
│   │   └── index.pkl
│   ├── __pycache__
│   │   ├── config.cpython-311.pyc
│   │   ├── config.cpython-312.pyc
│   │   ├── database.cpython-311.pyc
│   │   ├── database.cpython-312.pyc
│   │   ├── routes.cpython-311.pyc
│   │   └── routes.cpython-312.pyc
│   ├── Rag.py
│   ├── requirements.txt
│   ├── routes.py
│   └── users.db
├── frontend
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   ├── src
│   │   ├── AdminPanel.css
│   │   ├── AdminPanel.jsx
│   │   ├── App.css
│   │   ├── App.jsx
│   │   ├── Chat.css
│   │   ├── Chat.jsx
│   │   ├── config.js
│   │   ├── FormulaWidget.css
│   │   ├── FormulaWidget.jsx
│   │   ├── index.css
│   │   ├── Login.css
│   │   ├── Login.jsx
│   │   └── main.jsx
├── RAG - pdf
│   ├── faiss_index
│   │   ├── index.faiss
│   │   └── index.pkl
│   ├── templates
│   │   └── RAG_app.html
│   ├── .env
│   ├── RAG_app.py
│   ├── requirements.txt
└── main.py
```

---

## 🧰 Prerequisites

Make sure you have these installed:

- Python 3.9+
- Node.js 18+
- npm or yarn
- Git (optional but recommended)

---

## 🛠️ Backend Setup (Flask + Gemini + FAISS)

1. **Navigate to the backend:**
   ```bash
   cd backend
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set environment variables:**
   Make sure `.env` contains:
   ```
   GEMINI_API_KEY=your_google_generative_ai_key
   ```

5. **Run the Flask server:**
   ```bash
   python App.py
   ```

The backend will run at `http://localhost:5000`

> 💡 **Alternatively**, you can run the entire application using:
```bash
python main.py
```
This will launch both frontend and backend (if implemented in `main.py`).

---

## 🖼️ Frontend Setup (React + Vite)

1. **Navigate to the frontend:**
   ```bash
   cd frontend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the React dev server:**
   ```bash
   npm run dev
   ```

The frontend will run at `http://localhost:5173`

---

## ✅ Usage

- Register or log in via the frontend.
- Upload your academic PDF in the chat section.
- Ask questions related to the uploaded content.
- Admins can view user sessions and chats in the dashboard.

---

## ▶️ Demo Video

Watch a complete walkthrough of the chatbot here:  
📺 [YouTube Link Placeholder – Add your video link here]

---

## 🧪 Optional: Deployment Notes

To deploy this project:
- Backend can be hosted on Render, Railway, or Heroku
- Frontend can be built with `npm run build` and deployed via Vercel/Netlify
- Use a production database like PostgreSQL if needed
- Set CORS and environment variables accordingly in production

---

## 📬 Questions?

For any issues or improvements, feel free to raise an issue or contribute!

---

> Built with ❤️ using Flask, React, and Gemini

