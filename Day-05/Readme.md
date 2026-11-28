# 🍰 Sweet Crumbs AI Agent — Memory & RAG

An intelligent bakery assistant built with **LangChain, LangGraph, Groq, and ChromaDB** that combines conversational memory and Retrieval-Augmented Generation (RAG) to deliver context-aware responses and accurate answers to bakery policy questions.

This project is part of the **AI Agents Workshop – Level 2, Day 5**, exploring how AI agents can remember conversations, retrieve relevant information from a knowledge base, and handle customer orders using tools.

---

## 📌 Project Overview

The Sweet Crumbs AI Agent is designed to assist bakery customers through natural conversations. It maintains conversation context, retrieves bakery policies from a vector database, and uses tools to answer customer queries and manage orders.

Unlike a basic chatbot, this agent combines **memory, semantic retrieval, and tool calling** to provide more reliable and context-aware customer support.

---

## ✨ Features

- 🧠 **Conversation Memory:** Maintains conversation history using LangGraph's `InMemorySaver` checkpointer.
- 👥 **Multi-Customer Isolation:** Uses unique `thread_id` values to keep individual customer conversations separate.
- 📚 **Knowledge Base (RAG):** Retrieves bakery policies and FAQs using semantic similarity search.
- 🔍 **Semantic Search:** Uses embeddings and ChromaDB to find relevant information even when customers phrase questions differently.
- ✂️ **Document Chunking:** Splits knowledge documents into smaller chunks with overlap for improved retrieval.
- 🛠️ **Tool Integration:** Supports `get_price`, `is_open`, `log_order`, and `search_faq`.
- 🧾 **Order Handling:** Collects and processes customer order details.
- 🛡️ **Hallucination Control:** Uses retrieved knowledge and a fallback response when the required information is unavailable.
- 🧪 **Testing:** Evaluates agent responses using `tests.csv` with a target pass rate of at least 80%.

---

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Google Colab | Development environment |
| LangChain | Agent framework and tool integration |
| LangGraph | Agent execution and conversation checkpointing |
| Groq | LLM inference |
| ChromaDB | Vector database for knowledge retrieval |
| Embeddings | Semantic representation of documents |
| InMemorySaver | Short-term conversation memory |
| CSV | Agent evaluation and testing |


---

## 🔄 How It Works

1. **Customer Query:** The customer sends a message to the AI assistant.
2. **Query Understanding:** The agent identifies whether the query involves bakery policies, menu prices, opening hours, or placing an order.
3. **Knowledge Retrieval:** For policy-related queries, the `search_faq` tool searches the ChromaDB knowledge base.
4. **Semantic Search:** The database retrieves the most relevant document chunks based on similarity.
5. **Context Augmentation:** Retrieved information is added to the LLM's context.
6. **Response Generation:** The LLM generates a response based on the available information.
7. **Conversation Memory:** LangGraph's `InMemorySaver` maintains conversation history using a unique `thread_id`.
8. **Order Processing:** The agent uses its order tool to collect and process order details.

---

## 📚 Knowledge Base

The knowledge base contains bakery-related FAQs and policies, including:

- 🚚 Delivery policies
- 💳 Payment methods
- ❌ Cancellation policies
- 🎂 Photo cake orders
- ⚠️ Allergens and ingredient-related queries
- 🛒 Order requirements
- 📅 Order scheduling

The documents are chunked and stored in ChromaDB, allowing the agent to retrieve relevant information through semantic similarity search.

---

## 🧠 Key Concepts Learned

### 1. Memory in AI Agents
- Short-term conversational memory
- Customer-specific conversation threads
- Context retention across multiple turns
- Conversation isolation using `thread_id`

### 2. Embeddings
Embeddings convert text into numerical vectors that capture semantic meaning, allowing similar texts to be compared computationally.

### 3. Vector Databases
ChromaDB stores vector representations of documents and retrieves relevant information based on similarity.

### 4. Chunking
Documents are split into smaller sections with overlap to preserve context and improve retrieval quality.

### 5. Retrieval-Augmented Generation (RAG)

RAG combines information retrieval with LLM generation.

**Workflow:**

`Retrieve → Augment → Generate`

- **Retrieve:** Find relevant information from the knowledge base.
- **Augment:** Provide retrieved context to the language model.
- **Generate:** Produce an answer using the retrieved information.

### 6. Hallucination Reduction
The agent relies on retrieved bakery knowledge for policy answers and uses a fallback response when the knowledge base does not contain sufficient information.

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.10+
- Google Colab account
- Groq API key

### 1. Install Dependencies

```bash
pip install -q chromadb langchain langgraph groq
```

### 2. Configure API Key

Add your Groq API key to Google Colab Secrets.

Secret name:

```text
GROQ_API_KEY
```

### 3. Open the Notebook

Open the project notebook in Google Colab.

### 4. Execute the Notebook

Run the cells sequentially to:

- Install the required dependencies.
- Load bakery documents into ChromaDB.
- Create the embedding and retrieval pipeline.
- Define the `search_faq` tool.
- Configure agent memory using `InMemorySaver`.
- Initialize the agent.
- Execute sample customer queries.
- Evaluate responses using the test cases.

---

## 🧪 Agent Testing

The project includes `tests.csv` for evaluating agent behavior across multiple test scenarios.

The test cases aim to evaluate:

- FAQ retrieval accuracy
- Policy-based responses
- Conversation memory
- Customer thread isolation
- Order handling
- Fallback responses

<sub>Target evaluation score: 80% or higher.</sub>

---

## 📂 Project Structure

```text
Sweet-Crumbs-Memory-RAG/
│
├── Sweet_Crumbs_Memory_RAG.ipynb
├── tests.csv
├── README.md
└── requirements.txt
```

<sub>Adjust the file names above to match the actual files in your repository.</sub>

---

## 🎯 Project Objective

The objective of this project is to explore how AI agents can combine conversation memory, vector databases, semantic search, tool calling, and Retrieval-Augmented Generation to build smarter, more reliable conversational applications.

---

## 👩‍💻 Author

**RamyaSri Chakka**

---


