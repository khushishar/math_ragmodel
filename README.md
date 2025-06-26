📓 [View Math Notebook Gist](https://gist.github.com/khushishar/5b71754355c43fc58800eb6c62f4339a)

**AI Math Professor (RAG Agent)** is a Retrieval-Augmented Generation (RAG) system that acts like a step-by-step math tutor. It explains complex math problems—particularly from high school and college entrance exams—by breaking them into clear, logical steps using context-retrieved documents. 

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




