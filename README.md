# LLaMA-Based RAG System — Multi-PDF Question Answering

A Retrieval-Augmented Generation (RAG) application that enables users to upload PDF documents and ask questions about their content. The system retrieves relevant document passages and uses a LLaMA language model to generate context-aware answers.

## Project Overview

This project demonstrates how Large Language Models (LLMs), vector search, and document retrieval can be combined to build a question-answering system for PDF documents.

Instead of relying only on the language model's pretrained knowledge, the system retrieves relevant information from uploaded documents to help generate answers grounded in the provided content.

## Key Features

- **Multi-PDF Question Answering:** Ask questions about uploaded PDF documents.
- **Document Processing:** Extract text from PDF files.
- **Text Embeddings:** Convert document chunks into vector representations.
- **Vector Search:** Retrieve relevant passages using FAISS.
- **LLaMA Integration:** Generate answers using LLaMA 3 8B Instruct.
- **Interactive Interface:** Access the application through a Gradio interface.
- **Google Colab Support:** Run the notebook in a compatible Colab environment.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Google Colab | Development and execution environment |
| LLaMA 3 8B Instruct | Language model for answer generation |
| LangChain | RAG pipeline and document processing |
| FAISS | Vector similarity search |
| Sentence Transformers | Text embeddings |
| PyPDF | PDF text extraction |
| Gradio | Interactive user interface |
| Hugging Face | Model access and authentication |

## System Workflow

1. Upload one or more PDF documents.
2. Extract text from the documents.
3. Split the extracted text into manageable chunks.
4. Generate embeddings for the chunks.
5. Store and index embeddings using FAISS.
6. Enter a question about the uploaded documents.
7. Retrieve the most relevant document chunks.
8. Provide the retrieved context to the LLaMA model.
9. Display the generated answer through the interface.

## Project Screenshots

The following screenshots illustrate the development and setup workflow.

### 1. Google Colab Runtime

![Google Colab Runtime](Screenshots/colab-runtime-t4.png)

### 2. Dependency Installation

![Dependency Installation](Screenshots/dependency-installation.png)

### 3. Hugging Face Authentication Setup

![Hugging Face Login Instructions](Screenshots/huggingface-login-instructions.png)

> Note: These screenshots illustrate setup steps. Add application-interface screenshots here as well, if available.

## Getting Started

### Prerequisites

- A Google account to use Google Colab.
- A Hugging Face account.
- Access to the LLaMA model used by the notebook.
- PDF documents for testing.
- A compatible runtime with sufficient memory and computational resources.

### Run in Google Colab

1. Open the notebook `23AI07_NLP_workshop_llama_rag_colab.ipynb`.
2. Upload or open the notebook in Google Colab.
3. Select **Runtime → Change runtime type** and choose a GPU runtime when available.
4. Install the required dependencies by running the notebook's installation cell.
5. Configure your Hugging Face access token securely using Colab Secrets. Use the secret name `HF_TOKEN` if the notebook expects that name.
6. Ensure your Hugging Face account has the required access to the selected LLaMA model.
7. Run the notebook cells in order.
8. Upload PDF documents through the application's interface and ask questions about their contents.

**Important:** GPU availability and model access depend on your account, runtime limits, and Hugging Face permissions.

## Configuration and Security

- Never commit Hugging Face access tokens, passwords, API keys, or other secrets to GitHub.
- Do not store private credentials directly in the notebook.
- Use Google Colab Secrets or environment variables for sensitive configuration.
- Ensure that uploaded PDFs do not contain confidential or personal information before using them in a public demonstration.

## Project Structure

```text
LLaMA-RAG-System/
├── 23AI07_NLP_workshop_llama_rag_colab.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── Screenshots/
    ├── colab-runtime-t4.png
    ├── dependency-installation.png
    └── huggingface-login-instructions.png
```

The screenshot filenames and capitalization must match the actual files committed to the repository.

## Limitations

- Answer quality depends on the quality of the source documents, retrieval results, and language model.
- Scanned PDFs may require OCR if their text is not extractable.
- Model loading and inference may require substantial memory and GPU resources.
- Access to gated Hugging Face models requires the appropriate permissions.

## Future Enhancements

- Add source references and page numbers to answers.
- Improve retrieval with hybrid search and reranking.
- Support more document formats.
- Improve document-level citation and answer verification.
- Add conversation history and enhanced document management.

