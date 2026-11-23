# 🏏 Cricket Assistant using LLM

## 📌 Project Overview
A beginner-friendly Cricket Assistant built using a Large Language Model (LLM), Groq API, and LangChain. It helps users who have little or no knowledge of cricket understand the game through simple and easy-to-understand answers.

## 🎯 Objective
To build a domain-specific AI assistant that answers cricket-related questions while following predefined instructions through System Prompting.

## 🛠️ Technologies Used
- **Python** – Programming language
- **Google Colab** – Development environment
- **Groq API** – LLM inference
- **LangChain** – Framework for connecting with LLMs
- **GPT-OSS 120B** – Large Language Model

## ⚙️ Key Features
- Answers cricket-related questions.
- Explains cricket rules, players, teams, formats and tournaments.
- Uses simple English for beginners.
- Restricts responses to cricket-related topics.
- Follows a polite and friendly communication style.
- Keeps responses under 100 words.
- Uses System Prompts to control LLM behaviour.

## 🔍 How It Works
1. Install the `langchain_groq` package.
2. Configure the Groq API key using Google Colab Secrets.
3. Initialize the GPT-OSS 120B model.
4. Define a System Prompt with the Cricket Assistant's role and rules.
5. Accept questions from users.
6. Send the System Prompt and user question to the LLM.
7. Generate and display the response.

## 💡 Example
**User Question:**
Who is known as the Chase Master in cricket?

**Expected Response:**
Virat Kohli is popularly known as the Chase Master because of his exceptional ability to chase targets, particularly in limited-overs cricket.

## 📚 Concepts Learned
- Introduction to Large Language Models (LLMs)
- Groq API integration
- LangChain basics
- System Prompting
- Prompt Engineering
- Model initialization
- Temperature parameter
- LLM response generation

## 🚀 Future Improvements
- Add a user-friendly chat interface.
- Integrate live cricket score APIs.
- Add multilingual support.
- Implement prompt injection detection using Llama Prompt Guard.

## 👩‍💻 Learning Outcome
This hands-on exercise helped me understand how to connect an LLM to a Python application, customize its behaviour using System Prompts, and build a simple domain-specific AI assistant.

---

**Project Type:** Agentic AI / LLM Hands-on Practice

**Status:** Completed – Learning Project
