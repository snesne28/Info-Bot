# Info Bot - RAG Based AI Assistant for the College Website

This project is an intelligent chatbot for my college website that uses Retrieval-Augmented Generation (RAG) and Google Gemini LLM to answer any queries related to the institution. It processes PDF documents containing web scraped data and provides accurate, context-based responses in natural language.

The chatbot enables users—students, faculty, or visitors—to ask questions about the college and receive responses grounded in actual college documents. This ensures reliable and factual information delivery.

It integrates:

Document parsing from PDFs, Embedding & storage of content using FAISS, Query answering with context retrieval + generative AI

---

## 🚀 How It Works

1. **Data Collection & Preprocessing**  
   Web crawling and PDF processing are used to gather data from the college's digital resources (e.g., rules,     syllabus PDFs, notices, FAQs).

2. **Text Chunking & Embedding**  
   Extracted content is chunked using `RecursiveCharacterTextSplitter`, and each chunk is embedded using **Google Gemini’s `embeddings-001` model**.

3. **Vector Store**  
   These embeddings are stored in a local **FAISS** (Facebook AI Similarity Search) index for lightning-fast similarity searches.

4. **Question Answering**  
   When a user asks a question, the chatbot:
   - Performs a similarity search on the vector store.
   - Sends the most relevant chunks to **Google Gemini (`gemini-1.5-pro`)**.
   - Returns an accurate, context-aware response.

---

## 🚀 Features

- Real-time question answering from college documents 🧾
- Persistent local vector store for faster retrieval ⚡
- Simple API interface for frontend integration 💬
- Cross-platform and extensible architecture 🔧

---

## 🧠 Tech Stack

| Tech                | Purpose                                              |
|---------------------|---------------------------------------------------   |
| **FastAPI**         | API backend framework for handling user requests     |
| **Google Gemini**   | Embeddings (`embedding-001`) + QA (`gemini-1.5-pro`) |
| **FAISS**           | Efficient local vector store and similarity search   |
| **PyPDF2**          | Parses and extracts text from PDF documents          |
| **dotenv**          | Manages environment variables securely               |
| **CORS Middleware** | Enables frontend-backend interaction                 |

---

## 📂 Project Setup


### 1️⃣ Install Dependencies

Ensure you have Python 3.8+ installed. Then, install the required libraries:

```bash
pip install -r requirements.txt
```

### 2️⃣ Setting up the Environment Variables:

There is a .env file inside the folder "Backend Chatbot Python"
Open that file and add your Google Gemini API Key.

### 3️⃣ Run the Server

Type the following command in your terminal once all the setup is done.

```bash
uvicorn main:app --reload
```
The backend python code is setup and is up and running.

### 4️⃣ Run the Website

Next open "Website" folder and run the index.html file, The website will be loaded and you can ask
any relevant questions related to the college to the Chatbot and it will answer the question

---

## 📝 Future Improvements

✅ Add user session tracking and chat history
🔄 Live website scraping and index refresh scheduler
📤 Upload UI to allow admins to add new documents
🌐 Deploy to cloud services (Render, Railway, or AWS)

---

## 🤝 Contributing

Feel free to fork the repository, improve the project, and create a pull request!

---

## 📜 License

This project is licensed under the MIT License.

---

## 📷 **Preview**

![alt text](image1.png)

![alt text](image2.png)


---

⚡ **Happy Coding!** 🚗🚦

