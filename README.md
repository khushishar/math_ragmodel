📓 [View Math Notebook Gist](https://gist.github.com/khushishar/5b71754355c43fc58800eb6c62f4339a)

**AI Math Professor (RAG Agent)** is a Retrieval-Augmented Generation (RAG) system that acts like a step-by-step math tutor. It explains complex math problems—particularly from high school and college entrance exams—by breaking them into clear, logical steps using context-retrieved documents. 

---

![Demo](https://private-user-images.githubusercontent.com/90930534/459558500-505184ad-66d9-42b1-b1c8-f260675e806a.mp4?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTA5NjA1MDQsIm5iZiI6MTc1MDk2MDIwNCwicGF0aCI6Ii85MDkzMDUzNC80NTk1NTg1MDAtNTA1MTg0YWQtNjZkOS00MmIxLWIxYzgtZjI2MDY3NWU4MDZhLm1wND9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA2MjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNjI2VDE3NTAwNFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTRkYjM5OGJhZDdjZDgyNTFjMzE2MTUwNjAwM2VkMmFlZmI4YWRhYTFkYTE2OGMwYzZiZTY1ZjZkZGI0ZDEyMWYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.4V6TP5OUcigxMMLPltO6HnMoxTFEsEGn87fApn1d9a8)


---

How to run 
```bash
# Clone the repo
git clone https://github.com/yourusername/math-rag-agent.git
cd math-rag-agent

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```
> Set your HuggingFace token, Groq and SerpAPI key in `.env`

---

* **Agentic Framework:** `Agno`
* **Embedding Model:** `BAAI/bge-base-en-v1.5` from HuggingFace
* **Vector Store:** `ChromaDB`
* **Frontend:** Streamlit (for demo UI)
* **Web Search:** SerpAPI for fallback to real-time queries
  
---

| Feature                                          | Purpose                                                      |
| ------------------------------------------------ | ------------------------------------------------------------ |
| 📚 **Contextual Document Retrieval**             | Fetch exact math concepts for a question                     |
| 🔍 **Step-by-Step Explanation**                  | Emulates professor-style walkthroughs                        |
| 🌐 **Fallback to Web Search (via SerpAPI)**      | Handles out-of-dataset queries                               |
| 👤 **Human-in-the-loop Feedback**                | Allows students to correct/improve AI answers                |

---

References:

* [LangChain Documentation](https://docs.langchain.com/)
* [Agno Documentation](https://docs.agno.com/introduction)
* [ChromaDB Docs](https://docs.trychroma.com/)
* [Article on agent team](https://medium.com/@sharmaprabesh027/agno-agi-overcoming-default-model-issues-in-multi-agent-systems-e5d06878a1fb)




