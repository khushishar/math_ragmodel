### 1. What is the project?

**AI Math Professor (RAG Agent)** is a Retrieval-Augmented Generation (RAG) system that acts like a step-by-step math tutor. It explains complex math problems—particularly from high school and college entrance exams—by breaking them into clear, logical steps using context-retrieved documents. 

---

### 2. Live link or video demo of the project


---

### 3. What inspired you to build it?

As a student passionate about mathematics and AI, I noticed most AI systems lacked true explanatory depth. Tools like WolframAlpha or ChatGPT often provide direct answers, but not always in a student-friendly way. I wanted to build something that could teach the way a real professor does—**by guiding learners through the logic of each step**. This project combines my love for teaching, NLP, and education tech.

---

### 4. What’s the tech stack? Why did you choose it?

* **LLM Backbone:** Open-source HuggingFace model via `LangChain`
* **RAG Framework:** `LangChain`
* **Embedding Model:** `BAAI/bge-base-en-v1.5` from HuggingFace
* **Vector Store:** `ChromaDB`
* **Frontend:** Streamlit (for demo UI)
* **Optional Web Search:** SerpAPI for fallback to real-time queries

**Why these?**

* LangChain provides modular RAG support.
* ChromaDB is lightweight and simple for local vector storage.
* HuggingFace models are free, offline-capable, and customizable.
* Streamlit speeds up UI prototyping for demo purposes.

---

### 5. What features are you implementing? Why?

| Feature                                          | Purpose                                                      |
| ------------------------------------------------ | ------------------------------------------------------------ |
| 📚 **Contextual Document Retrieval**             | Fetch exact math concepts for a question                     |
| 🔍 **Step-by-Step Explanation**                  | Emulates professor-style walkthroughs                        |
| 🌐 **Fallback to Web Search (via SerpAPI)**      | Handles OOD (out-of-dataset) queries                         |
| 👤 **Human-in-the-loop Feedback**                | Allows students to correct/improve AI answers                |
| 🧠 **Self-improving DSPy Integration (Planned)** | Lets the agent refine responses based on historical feedback |

These features ensure the agent is **educational**, **flexible**, and **adaptable to user feedback**.

---

### 6. Resources referred

* [LangChain Documentation](https://docs.langchain.com/)
* [HuggingFace Transformers](https://huggingface.co/docs/transformers/index)
* [ChromaDB Docs](https://docs.trychroma.com/)
* [DSPy: Declarative Self-Improving Agents](https://github.com/stanfordnlp/dspy)
* [JEE Math Previous Year Papers (PDF)](https://example.com/jee-pdfs)
* Research papers on:

  * Retrieval-Augmented Generation
  * Pedagogical agents
  * Explainable AI in education

---

### 7. Learning Log

> **Week 1:** Explored RAG architecture. Integrated PDF-based knowledge base via LangChain.
> **Week 2:** Added HuggingFace BGE embeddings and switched to ChromaDB for faster local queries.
> **Week 3:** Worked on multi-step solution formatting and human feedback logging system.
> **Week 4:** Implemented SerpAPI fallback and began integrating DSPy for agent improvement.
> *(Maintained in `learn_log.md`)*

---

### 8. Proper commit messages

Here are some sample commit messages from the project:

* `feat: added step-by-step formatter for math solutions`
* `fix: corrected embedding issue with HuggingFace BGE model`
* `chore: added PDF loader support for JEE papers`
* `refactor: modularize retriever and chain initialization`
* `docs: updated README with feature descriptions`

All commits follow semantic commit conventions for readability and collaboration.

---

### 9. How to run the project?

```bash
# Clone the repo
git clone https://github.com/yourusername/math-rag-agent.git
cd math-rag-agent

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Load your PDFs into ChromaDB (1-time setup)
python ingest_documents.py

# Run the app
streamlit run app.py
```

> Set your HuggingFace token and SerpAPI key in `.env`

---

### 10. How can others contribute to the project?

* 🛠️ **Fork this repo**, create a new branch, and raise a PR
* 🧪 Add new types of math problems (e.g., geometry, calculus)
* 💡 Improve explanation clarity or suggest prompt rewrites
* 🔬 Benchmark agent performance with JEE Bench (planned)
* 🗣️ Join discussions in [Issues](https://github.com/yourusername/math-rag-agent/issues)

📓 [View Math Notebook Gist](https://gist.github.com/khushishar/5b71754355c43fc58800eb6c62f4339a)
