SaaS Support Copilot — README
Project Overview
SaaS Support Copilot is a Retrieval-Augmented Generation (RAG) support bot designed for SaaS platforms. It ingests support documents, FAQs, and structured help content, enabling users to query for quick, context-aware answers. The architecture leverages Colab, Python, Gradio, and OpenAI APIs for robust natural language response capabilities.​

Key Features
Flexible Document Ingestion: Upload .json, .csv, or .txt files containing support documentation.​

Efficient Indexing: The bot parses, chunks, and embeds content using BM25 and neural embedding models for fast retrieval.​

Hybrid Retrieval Logic: Combines classic BM25 scores and embedding similarity for optimal document search.​

Interactive Web UI: Powered by Gradio, supporting both document ingestion and live support query answering.​

LLM Integration: Optional use of OpenAI LLMs to generate enriched, validated answers (API key required).​

Quickstart
Setup: Launch the notebook in Colab. Ensure Python 3 environment and GPU acceleration are available.​

Document Upload: Use the Gradio UI to upload support docs in .json, .csv, or .txt format.​

Query: Type support questions in the interface. Retrieve responses with or without LLM enrichment.​

Validation: Each answer includes a validation score for retrieval accuracy.​

Usage Instructions
Colab Launch: Execute the first cell to initialize and configure environment.​

File Ingestion: Click "Upload docs" and "Ingest file" in the Gradio panel to index new documents.​

Support Q&A: Enter questions such as “Where can I find API keys?” and receive relevant context from the uploaded docs.​

Advanced: Input your OpenAI API key to leverage LLM answer generation and validation.​

Core Logic
Files are parsed and chunked; BM25 and embedding retrieval provide hybrid search.​

Answers are generated and validated against the indexed docs for trustworthiness.​

Supports reloadable index state via local save/load.​

File Structure
saas_support_copilot.ipynb: Main notebook, setup, document ingestion, query UI, retrieval, and answer logic.​

index_state.pkl: Saved index for fast reload.​

FAQ Examples
Billing: "Billing is monthly. You will be charged on the first of each month for the previous month's usage."​

SSO Setup: "To set up SAML SSO, provide ACS URL and Entity ID from your provider, and upload the IdP certificate."​

API Keys: "API keys are under Project > Settings > API Keys. You can create, revoke, and rotate keys there."​

Data Import: "Supports CSV, JSON, XLSX files up to 5MB with header row."​

Deployment Notes
Colab public URL expires in one week. For permanent hosting and GPU, use gradio deploy for deployment to HF Spaces.​


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7f849afa-893c-449e-a96a-5aad7b88d6d7" />
