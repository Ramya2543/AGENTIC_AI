# 🍰 Sweet Crumbs Home Bakery – AI Chat Assistant

## 📌 Project Overview

This project builds a friendly AI chatbot for **Sweet Crumbs Home Bakery** using LangChain and Groq. The chatbot answers customer questions about cake prices, eggless options, order notice requirements, and remembers previous messages within the conversation.

The project also introduces how the same chatbot can be converted into a LangChain Agent.

## 🎯 Objectives

- Build an AI chatbot using LangChain.
- Connect an LLM using the Groq API.
- Create a custom system prompt.
- Implement conversational memory using chat history.
- Test chatbot responses using predefined test cases.
- Explore the basic structure of a LangChain Agent.

## 🛠️ Technologies Used

- Python
- Google Colab
- LangChain
- LangChain-Groq
- Groq API
- CSV

## 🧠 Concepts Covered

### 1. LLM Setup
- Installing LangChain and LangChain-Groq.
- Connecting Groq API using Google Colab Secrets.
- Initializing the `ChatGroq` model.

### 2. Prompt Templates
- Using `ChatPromptTemplate`.
- Creating a system prompt with business-specific information.
- Using `MessagesPlaceholder` to pass conversation history.

### 3. Conversational Memory
- Maintaining chat history using a Python list.
- Remembering previous conversations.
- Using previous messages to answer follow-up questions.

### 4. LCEL Chain
Building a chain using:

`Prompt → LLM → Output Parser`

Using LangChain Expression Language (LCEL).

### 5. Testing
- Testing chatbot responses using CSV-based test cases.
- Checking whether responses contain expected keywords.
- Displaying PASS and FAIL results.

### 6. LangChain Agent Introduction
- Exploring `create_agent`.
- Creating an agent with a system prompt.
- Understanding the basic agent structure before adding tools.

## 🍰 Bakery Information

| Item | Price |
|---|---:|
| Plum Cake | ₹500 |
| Chocolate Cake | ₹650 |
| Cupcake | ₹80 each |

- Orders require 24 hours' notice.
- Eggless versions are available for all cakes.
- The assistant does not promise delivery times or locations.




## 🚀 How It Works

1. Install the required LangChain libraries.
2. Set the Groq API key through Google Colab Secrets.
3. Initialize the Groq language model.
4. Define the chatbot system prompt.
5. Create the prompt template with conversation history.
6. Build the chain using LCEL.
7. Implement the `ask()` function to interact with the chatbot.
8. Test the chatbot using CSV-based test cases.
9. Explore the chatbot as a LangChain Agent.

## 💬 Sample Interaction

**Customer:** Hi, I'm Ravi. Do you make eggless cakes?

**AI:** Yes! We offer eggless versions of all our cakes. 😊

**Customer:** What's my name?

**AI:** Your name is Ravi! 😊

## 📈 Learning Outcome

Through this project, I explored how to build a business-specific AI assistant using LangChain, connect an LLM through Groq, maintain conversational history, test chatbot responses, and understand the foundation of AI agents.

## 🔮 Future Enhancements

- Add tools for checking cake availability.
- Integrate order management.
- Add customer order tracking.
- Connect a database for persistent memory.
- Build a web-based chatbot interface.
- Add real-world tools to the LangChain Agent.

---

*Built as part of my Agentic AI learning journey.* 🤖
