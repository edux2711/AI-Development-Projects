<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Run Ollama On Your Own Machine

**Project Link:** [View Project](http://learn.nextwork.org/projects/ai-ollama-setup)

**Author:** Eduardo Gonzalez  
**Email:** edux2711@gmail.com

---

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-ollama-setup_n1p5r9t3)

---

## Introducing Today's Project!

In this project, I'm going to set up a complete local AI environment with Ollama, so I can run language models on my own machine with a single command.

### Key tools and concepts

Key concepts I learnt include Ollama as a local LLM, Ollama's model library, RAG, and custom AI personas using Modelfiles.

### Challenges and wins

This project took me approximately 30 minutes to complete. It was very simple and quick to download and learn how to use Ollama.

---

## Installing Ollama for Local AI

In this step, I'm going to install Ollama on my machine. Ollama is an open-source tool that lets you run large language models (LLMs) directly on your computer. It simplifies downloading and managing these models, offering privacy and offline use without needing cloud services.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-ollama-setup_h4n8k2m6)

### Verifying the installation

I verified Ollama is running by running: curl http://localhost:11434 in the terminal. The response I saw was "Ollama is running".

---

## Pulling My First AI Model

In this step, I'm going to download a model and chat with it locally. The model I'm using is qwen2.5:0.5b.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-ollama-setup_b5c9d3f7)

### Understanding model sizes

I pulled the model using: ollama pull qwen2.5:0.5b. qwen2.5 is a model developed by Alibaba. The 0.5b means 0.5 billion parameters were used to train the model.

---

## Chatting with My Local AI

I chatted with my local AI by asking it to tell me the capital of France. It responded with "The capital of France is Paris". This differs from cloud AI because the LLM runs locally on the machine, without a connection to cloud services.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-ollama-setup_n1p5r9t3)

---

## Exploring Local AI Limitations

In this step, I'm going to discover what local AI models can and can't do. Local AI models can't answer personal questions because it does not have access to your emails or other personal data.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-ollama-setup_d8r4t6w1)

### Understanding RAG

The AI couldn't answer because it is trained on general knowledge, not on personal data, and it cannot access files or private information. RAG, or Retrieval-Augmented Generation, enables AI to access personal data.

---

## Creating a Custom AI Persona

In this project extension, I created a persona called coding tutor. It behaves differently because I created a Modelfile with a system prompt that shapes all responses to be user-friendly and to explain programming concepts in simple terms with analogies.

![Image](http://learn.nextwork.org/overjoyed_gray_calm_beaver/uploads/ai-ollama-setup_j3k7m2n8)

---

## Wrapping Up

I did this project today to learn how to use and familiarize myself with Ollama, I will be using this tool in the future to avoid spending tokens on other online AI chats.

---

---
