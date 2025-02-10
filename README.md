# AI-Powered Chatbot with Vector Search using n8n

## Overview
This project implements an AI-powered chatbot with retrieval-augmented generation (RAG) using **n8n**, **Pinecone**, **Groq Chat Model**, and **Hugging Face embeddings**. The chatbot can process user queries, store chat history, and retrieve relevant information using a vector database.

## Features
- AI chatbot built with **n8n** workflow automation.
- **Vector search** implementation using **Pinecone Vector Store**.
- **Groq Chat Model** for natural language understanding and response generation.
- **Hugging Face embeddings** for document processing.
- Google Drive integration for **file downloads** and data ingestion.
- **Recursive Character Text Splitter** for efficient text processing.

## Execution Flow
### Document Ingestion Workflow
![Document Ingestion Workflow](https://github.com/Tanujkumar24/n8n-workflows-RAG-AGENT/blob/main/Document%20Ingestion%20Workflow.png)
1. **Trigger:** Activated when clicking "Test workflow".
2. **Google Drive Integration:** Downloads files containing documents.
3. **Default Data Loader:** Loads the document for processing.
4. **Text Splitting:** Uses **Recursive Character Text Splitter** for chunking.
5. **Embedding Generation:** Converts text chunks into embeddings using **Hugging Face**.
6. **Vector Storage:** Stores the embeddings in **Pinecone Vector Store**.

### Chatbot Workflow
![Chatbot Workflow](https://github.com/Tanujkumar24/n8n-workflows-RAG-AGENT/blob/main/Chatbot%20Workflow.png)
1. **Trigger:** The chatbot is activated when a chat message is received.
2. **AI Agent:** Processes the message and interacts with different components.
3. **Memory Handling:** Uses **Window Buffer Memory** to store conversation context.
4. **Vector Search:** Queries the **Pinecone Vector Store** to find relevant data.
5. **Response Generation:** Uses **Groq Chat Model** to generate responses.
6. **Embedding Model:** **Hugging Face** embeddings help encode text for vector storage.
7. **Final Response:** The chatbot provides an AI-generated response based on retrieved knowledge.

## Implementation Details
- **n8n Workflows:** Automates interactions between AI models, vector stores, and memory components.
- **Pinecone:** Enables fast and scalable vector similarity searches.
- **Groq Chat Model:** Provides conversational AI capabilities.
- **Hugging Face Embeddings:** Converts text into vector representations.
- **Google Drive Integration:** Fetches files dynamically for processing.
- **Recursive Character Text Splitter:** Ensures efficient handling of large text documents.

## Video Demonstration
[![Watch the Video](https://img.youtube.com/vi/YOUR_VIDEO_ID/maxresdefault.jpg)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)

*(Replace `YOUR_VIDEO_ID` with the actual video link.)*

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_GITHUB_REPO.git
   cd YOUR_GITHUB_REPO
   ```
2. Install **n8n** and required dependencies.
3. Import the provided n8n workflows.
4. Configure API keys for Pinecone, Groq Model, and Hugging Face.
5. Run the workflows to test the chatbot and document processing.

## Contact
For any issues or contributions, feel free to raise a pull request or open an issue.

---
🚀 **Happy Coding!** 🚀
