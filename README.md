# Knowledge Base Search Engine

A powerful Retrieval-Augmented Generation (RAG) search engine that lets users upload documents (PDF/TXT) and ask natural-language questions. Powered by Large Language Models (LLMs), it reads and understands your files—delivering clear, concise, and context-aware answers instead of just matching keywords. Whether you're exploring research papers, manuals, or notes, this tool helps you find what matters most.
Deliverables :
github link : 

Demo video link : https://drive.google.com/file/d/1LzS1exKmHtNEPzlQlY_ARlv-3GUD1ckz/view?usp=sharing
## Features

- Document ingestion: Upload multiple PDF and TXT files
- Embeddings: Uses OpenAI embeddings for vectorization
- Vector store: FAISS for efficient similarity search
- LLM: OpenAI GPT for answer synthesis
- API: FastAPI backend
- Frontend: Simple web interface for upload and query

## Setup

1. Ensure Python 3.11+ is installed.

2. Clone or download the project.

3. Navigate to the project directory.

4. Create virtual environment:
   ```
   py -3 -m venv venv
   ```

5. Activate the environment:
   ```
   call venv\Scripts\activate.bat
   ```

6. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

7. Set your OpenAI API key:
   ```
   set OPENAI_API_KEY=your_api_key_here
   ```

8. Run the application:
   ```
   uvicorn main:app --reload
   ```

9. Open your browser to `http://localhost:5000`

## Usage

1. Upload documents using the upload form (select multiple PDF/TXT files).
2. Once uploaded, enter a query in the query field and click Search.
3. The synthesized answer will be displayed.

## API Endpoints

- `POST /upload`: Upload files (multipart/form-data)
- `POST /query`: Query with JSON body {"query": "your question"}
- `GET /`: Serve the frontend


## Evaluation

- Retrieval accuracy: Based on FAISS similarity search
- Synthesis quality: Depends on OpenAI LLM
- Code structure: Modular with separate files for ingestion and retrieval
- LLM integration: Uses LangChain for seamless integration
