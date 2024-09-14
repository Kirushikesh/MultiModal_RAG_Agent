# MultiModal Document Analysis with Docling and LangChain

This project demonstrates how to build a powerful multimodal agent for document analysis using Docling for PDF extraction and LangChain for creating AI chains and agents. It showcases the seamless integration of tabular and textual data extracted from PDFs into a unified query system.

## Key Features

- PDF text and table extraction using Docling
- SQL-based querying of extracted tabular data
- RAG (Retrieval-Augmented Generation) for textual data analysis
- MultiModal Agent combining SQL and RAG capabilities

## Why Docling?

[Docling](https://github.com/DS4SD/docling) is a state-of-the-art, open-source PDF conversion tool that offers several advantages:

1. **Accuracy**: Powered by specialized AI models for layout analysis (DocLayNet) and table structure recognition (TableFormer).
2. **Efficiency**: Runs on commodity hardware with a small resource budget.
3. **Comprehensive**: Understands detailed page layout, reading order, locates figures, and recovers table structures.
4. **Metadata Extraction**: Extracts metadata such as title, authors, references, and language.
5. **Flexibility**: Configurable for batch-mode or interactive use.
6. **OCR Support**: Optional OCR for scanned PDFs.
7. **Easy Integration**: Simple, self-contained Python library with permissive MIT license.

## Installation

1. Clone this repository
2. Navigate to the project directory:
```python
cd MultiModal_RAG_Agent/
```
3. Install the required dependencies:
```python
pip install -r requirements.txt
```
4. Create a .env file in the current folder
```
OPENAI_API_KEY=...
```

## Usage

1. Place your PDF files in the `data/` directory.
2. Run the main.ipynb notebook.
3. The notebook will:
- Extract text and tables from the PDFs using Docling
- Create an SQLite database with the extracted tables
- Set up a RAG system for the extracted text
- Initialize a multimodal agent that can answer questions using both SQL and RAG

4. You can then query the agent with questions about the document content.

## How It Works

1. **PDF Extraction**: Docling is used to extract both text and structured table data from PDF files.
2. **SQL Chain**: Extracted tables are stored in an SQLite database, which can be queried using natural language through a LangChain SQL chain.
3. **RAG Chain**: Extracted text is processed into a vector store for semantic search and query answering.
4. **MultiModal Agent**: Combines the SQL and RAG chains into a unified agent that can route queries to the appropriate system based on the question type.

## Contributing

Contributions to improve the project are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [Docling](https://github.com/DS4SD/docling) for providing powerful PDF extraction capabilities
- [LangChain](https://github.com/langchain-ai/langchain) for the flexible AI chain and agent framework
- OpenAI for the language model used in this project
