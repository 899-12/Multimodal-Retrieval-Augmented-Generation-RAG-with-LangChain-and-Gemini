# Multimodal Retrieval Augmented Generation (RAG) with LangChain and Gemini

This repository demonstrates a multimodal RAG system built using LangChain and Google's Gemini models. The system can process both images and text to answer questions and provide insights.

## System Overview

The system consists of the following components:

- **Language Models:**
    - Gemini Pro Vision: Used for understanding images.
    - Gemini 1.0: Used for text processing and generation.
- **Embedding Model:** Google Generative AI Embeddings, used to convert text into numerical vectors for efficient search.
- **Vector Database:** FAISS, used to store and search document chunks based on their embeddings.
- **LangChain Framework:** Used to orchestrate the interaction between different components and create the RAG pipeline.

## Functionality

1. **Image Processing:** The system can analyze images using Gemini Pro Vision and provide summaries or insights based on the image content.
2. **Document Processing:** It can load and process text documents, such as PDF research papers. Documents are split into chunks and stored in the vector database for retrieval.
3. **Retrieval Augmented Generation:** Given a query, the system retrieves relevant document chunks using the vector database and combines them with the query as context for the language model. The language model then generates a response based on this combined information.
4. **Multimodal Querying:** The system accepts both text and image inputs as queries, enabling a more comprehensive understanding of user requests.

## Usage

To run the system, you need to:

1. Install the required libraries: `langchain`, `langchain-google-genai`, `faiss-cpu`, `pypdf`.
2. Set up your Google API key.
3. Load the necessary models: Gemini Pro Vision and Gemini 1.0.
4. Load your document (PDF) and split it into chunks.
5. Create the vector database and retriever.
6. Define the RAG chain using LangChain.
7. Send your query, which can be text or an image, to the system.

## Example

The code includes an example of using the system to analyze an image of a building interior and potentially retrieve related information from a PDF document.

## Benefits

- **Multimodal Understanding:** Processes both images and text for a richer understanding of information.
- **Enhanced Information Retrieval:** Retrieves relevant context from documents to improve response quality.
- **Flexible and Extensible:** Can be adapted to various use cases and extended with additional modalities.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.
