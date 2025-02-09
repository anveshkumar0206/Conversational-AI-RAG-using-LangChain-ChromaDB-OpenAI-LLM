# Conversational-AI-RAG-using-LangChain-ChromaDB-OpenAI-LLM

The project demonstrates retrieval-augmented generation (RAG) by leveraging vector databases (ChromaDB) and embeddings to store and retrieve context-aware responses.

Project Overview

This project utilizes LangChain and the OpenAI API to develop:
1.A code understanding model – Uploads a Python script, analyzes its content, and answers queries based on the provided code.
2.A chatbot with memory – Interacts with text-based documents, answers user queries, and summarizes conversations.

Project Components

1.Code Understanding Model
Loads a Python script and splits it into chunks using RecursiveCharacterTextSplitter.
Generates OpenAI embeddings and stores them in ChromaDB.
Uses retrieval-based Q&A to answer user queries about the codebase.

Example Queries:
"What does the function generate_images do in my codebase?"
"What is the purpose of this script?"

2.Conversational Chatbot with Memory
Loads a PDF document, processes its text, and generates embeddings.
Uses ConversationalRetrievalChain with memory to enable context-aware interactions.
The chatbot remembers previous messages and summarizes conversations.

Example Chat Flow:
User: "Can you summarize the main topic of this document?"
AI: [Summary of document]
User: "Tell me more about the methodology used."
AI: [Details on methodology]
User: "Summarize our entire conversation."
AI: [Full conversation summary]

Workflow

Code Understanding Model
Load a Python file (generate.py) into LangChain.
Split the file into manageable chunks.
Convert text into embeddings using OpenAI API.
Store embeddings in ChromaDB.
Query the system to retrieve relevant sections of the code.
Conversational Chatbot
Load a PDF document.
Split the document into text chunks.
Generate OpenAI embeddings and store in ChromaDB.
Initialize a retrieval-based chatbot with memory.
Engage in a multi-turn conversation with persistent memory.
Generate a summary of the conversation.

Results: 
The system can understand and explain code structure based on user queries.
The chatbot remembers context, provides detailed responses, and summarizes interactions.
