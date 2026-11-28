# 🍰 Sweet Crumbs Home Bakery – AI Customer Support & Order Assistant

## 📌 Project Overview

Sweet Crumbs Home Bakery is an AI-powered customer support and cake-ordering assistant developed using Python, LangChain, LangGraph, and Groq LLM.

The system understands customer messages, classifies their intent, and routes them to specialized AI agents to handle frequently asked questions, cake orders, and general queries.

## ✨ Features

- **Intent Classification:** Classifies customer messages into FAQ, Order, and Other categories.
- **FAQ Agent:** Answers questions about bakery prices, opening hours, delivery, and policies.
- **Order Agent:** Collects customer details and processes cake-order requests.
- **Tool Calling:** Uses specialized tools to retrieve prices, search FAQs, check opening hours, and save orders.
- **Conditional Routing:** Routes customer messages to the appropriate agent using LangGraph.
- **State Management:** Maintains customer messages, detected intent, and generated replies.
- **Streaming:** Displays workflow execution updates using LangGraph.

## 🛠️ Technology Stack

- Python
- LangChain
- LangGraph
- Groq LLM
- Pydantic
- Google Colab / Jupyter Notebook

## 🏗️ Workflow Architecture

```text
                 START
                   |
                   v
               CLASSIFY
                   |
                   v
             Detect Intent
                   |
          +--------+--------+
          |        |        |
          v        v        v
         FAQ      ORDER    OTHER
          |        |        |
          v        v        v
       FAQ Agent  Order   General
                  Agent   Response
          |        |        |
          +--------+--------+
                   |
                   v
                  END
```

## 🔧 Tools Used

| Tool | Description |
|---|---|
| `search_faq()` | Searches bakery FAQs and policies. |
| `get_price()` | Retrieves bakery item prices. |
| `is_open()` | Checks bakery opening hours. |
| `log_order()` | Saves customer cake-order details. |

## 🤖 AI Agents

### 1. FAQ Agent

- Handles customer questions.
- Uses `get_price` to retrieve prices.
- Uses `is_open` to check opening hours.
- Uses `search_faq` to retrieve bakery policies.
- Avoids guessing and responds within 50 words.

### 2. Order Agent

- Handles cake-order requests.
- Collects customer name, item, quantity, and pickup date.
- Uses `get_price` to calculate order totals.
- Uses `log_order` to save orders.
- Reads back order details after saving.

## 🔄 LangGraph Implementation

The workflow is implemented using LangGraph's `StateGraph`.

The `BakeryState` maintains three fields:

- `message` – Customer's original message.
- `intent` – Classified customer intent.
- `reply` – Generated response.

### Graph Nodes

1. `classify` – Identifies the customer's intent.
2. `answer_faq` – Handles frequently asked questions.
3. `take_order` – Handles cake-order requests.
4. `other` – Handles greetings and unrelated messages.

Conditional edges route the customer message to the appropriate node based on the detected intent.

## 💬 Example Customer Queries

| Customer Query | Detected Intent |
|---|---|
| Do you deliver to my area? | FAQ |
| What is the price of chocolate cake? | FAQ |
| I'm Jahnavi, book 2 chocolate cakes for 24 Dec. | Order |
| Good morning! | Other |
| Is the plum cake nut-free? | FAQ |

## ⚙️ Installation and Setup

### 1. Install Dependencies

```bash
pip install -q langchain langchain-groq langgraph pydantic
```

### 2. Configure Groq API Key

```python
import os
from google.colab import userdata

os.environ["GROQ_API_KEY"] = userdata.get("AgenticAI")
```

### 3. Initialize the LLM

```python
from langchain_groq import ChatGroq

llm = ChatGroq(
    model="openai/gpt-oss-120b",
    temperature=0.3
)
```

### 4. Run the Workflow

```python
result = graph.invoke({
    "message": "Do you deliver to my area?"
})

print(result["reply"])
```

## 🚀 Future Enhancements

- Integrate a real-time bakery database.
- Develop a web-based chatbot interface.
- Store customer orders using MongoDB.
- Implement order tracking and cancellation.
- Add delivery availability checking.
- Integrate online payment functionality.
- Implement RAG for improved FAQ retrieval.

## 🎯 Project Objective

The main objective of this project is to demonstrate how multiple specialized AI agents can collaborate through LangGraph to automate customer support and order management.

By combining intent classification, tool calling, specialized agents, and conditional routing, the system provides an organized and modular approach to handling customer interactions.

---

**Built with ❤️ using Python, LangChain, LangGraph, and Groq.**
