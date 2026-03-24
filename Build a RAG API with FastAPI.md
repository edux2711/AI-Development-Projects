<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a RAG API with FastAPI

**Project Link:** [View Project](http://learn.nextwork.org/projects/ai-devops-api)

**Author:** Eduardo Gonzalez  
**Email:** edux2711@gmail.com

---

---

## Introducing Today's Project!

In this project, I'm going to build a RAG API using FastAPI, ChromaDB, and Ollama that answers personal questions by grounding AI responses in your own documents. 
I'm interested in this because I want to extend the functionality of my local LLM by implementing the full Retrieval-Augmented Generation pipeline, from document storage to AI-generated answers, running entirely on my machine with zero cloud costs. I also want to learn how to leverage RAG to build AI assistants that answer questions from internal documents, support tickets, or product catalogs without retraining models for future projects.

### Key tools and concepts

Key concepts I learnt include RAG, ChromaDB and vector embeddings, FastAPI and Swagger UI, semantic search, and dynamic document ingestion.

### Challenges and wins

This project took me approximately 50 minutes to complete. The most challenging part was learning the libraries for FastAPI, ChromaDB, and Pydantic.

---

## Performing RAG Manually

In this step, I'm going to set up a Python environment with dependencies to start a RAG API. 

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-devops-api_v3j7x5b9)

### Understanding the three parts of RAG

I manually performed RAG by entering personal information in the prompt. The three parts are finding information, adding it to the prompt, and the AI using the extra information to answer a question.

### Comparing the two AI models

The key difference I noticed is that nomic-embed-text is an embedding model for semantic search, returning results based on meaning rather than exact keyword matches.

---

## Building a Personal Knowledge Base

In this step, I'm going to write a personal profile document and store it as an embedding in ChromaDB, then I will write a Python script to load, chunk, and store the profile as embeddings. Embeddings are numerical representations of data.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-devops-api_g3h7m2r5)

### Creating the profile document

I included information about my skills, hobbies, and goals. This is personal information that the AI will be able to access to answer questions about me.

### How semantic search finds relevant chunks

ChromaDB sends each chunk in profile.txt to nomic-embed-text and converts it into a vector. When I ask a question, ChromaDB also converts it into a vector and finds the chunks closest to the chunks in profile.txt. This is called semantic search.

---

## Creating the RAG API with FastAPI

In this step, I'm going to build a FastAPI application that automatically retrieves context, augments the prompt, and generates a grounded answer. I'll test it using Swagger UI.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-devops-api_j5m1r8t2)

### How the /ask endpoint works

When a question comes in, the endpoint implements the three steps of RAG. When someone sends a question, it retrieves the 2 most relevant chunks from ChromaDB, augments the prompt by combining those chunks with the question, and generates a grounded answer using qwen2.5:0.5b. The response includes the context that was used to verify the AI's sources.

### Testing with Swagger UI

I tested my API by asking "What is my name?". The AI answered with "Your name is Eduardo". The context used from the profile.txt file was: 
"My name is Eduardo. I am computer science major currently learning about cloud computing, and AI.", and
"A fun fact about me is that I am learning to play the Ukelele!".

---

## Extending to a Multi-User AI Directory

In this project extension, I'm adding multi-user support because real-world RAG systems always serve multiple users or data sources. Multi-tenancy allows a single application instance to serve multiple users simultaneously.



![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-devops-api_d5g9k3n7)

### Adding the POST /documents endpoint

In this project extension, I added a POST endpoint that allows submission of new profiles. Metadata filtering enables the AI to answer questions only for specific users without searching the whole database.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-devops-api_r8t2w6y1)

### Verifying multi-user filtering

In this project extension, I tested multi-user queries by writing queries and filtering by username. The filter works because ChromaDB only provides the context for the given user.

---

## Wrapping Up

I did this project today to learn how to implement a complete RAG API pipeline for software development. 

---

---
