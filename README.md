# LLaMA-based RAG System — Multi-PDF Question Answering

A Google Colab notebook demonstrating a Retrieval-Augmented Generation (RAG) pipeline for asking questions about uploaded PDF documents.

## Technologies

- Google Colab with a GPU runtime (T4 recommended when available)
- Meta Llama 3 8B Instruct (`meta-llama/Meta-Llama-3-8B-Instruct`) with 4-bit quantization
- Hugging Face Hub authentication
- LangChain
- Sentence Transformers (`sentence-transformers/all-MiniLM-L6-v2`) for embeddings
- FAISS for vector similarity search
- PyPDF for PDF text extraction
- Gradio for the user interface

## Features

- Upload multiple PDF documents
- Extract and split PDF text into chunks
- Create embeddings and index chunks with FAISS
- Retrieve relevant document passages for a question
- Generate answers using Llama 3
- Interact through a Gradio UI

## Run in Google Colab

1. Open the notebook in this repository.
2. In Colab, select **Runtime → Change runtime type → T4 GPU** (if available).
3. Run the dependency-installation cell.
4. Accept the model access terms for [Meta Llama 3 8B Instruct](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct).
5. Create a Hugging Face token with only the permissions required to read the model.
6. In Colab, open **Secrets** (key icon), add a secret named `HF_TOKEN`, paste the token as its value, and enable notebook access to that secret.
7. Run the remaining notebook cells in order. Use the Gradio interface to upload PDFs and ask questions.

Access to the gated Llama model may require approval from Hugging Face. GPU availability and memory limits depend on your Colab account and current resource availability.

## Security

- **Never commit access tokens, passwords, API keys, or private documents.**
- Do not put your Hugging Face token directly in notebook code.
- Use Colab Secrets with the secret name `HF_TOKEN`.
- If a token has been exposed in a screenshot, chat, repository, or other public place, revoke it in Hugging Face settings and create a replacement.
- The screenshots folder should contain only screenshots that do not reveal tokens, device authorization codes, private documents, or personal information.

## Repository contents

- `23AI07_NLP_workshop_llama_rag_colab.ipynb` — the Colab notebook with saved cell outputs cleared
- `screenshots/` — selected project screenshots (add only sanitized images)
- `requirements.txt` — core Python package list; the notebook installs dependencies itself
- `.gitignore` — excludes common secrets, local data, and generated files

## Limitations

Answers depend on the text extracted from uploaded PDFs and the passages retrieved by the vector search. Always verify important answers against the original documents.
