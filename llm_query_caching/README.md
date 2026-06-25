### Project Overview
This project contains tutorials for Vector database operations using Milvus, LLM, Caching and RAG.

### Reference

The code is based on the following resource:
LinkedIn Learning Tutorial: https://www.linkedin.com/learning/llm-foundations-vector-databases-for-caching-and-retrieval-augmented-generation-rag/genai-with-vector-databases
Author: https://www.linkedin.com/learning/instructors/kumaran-ponnambalam

#### My modifications

* Updated to latest versions of libraries for OpenAI and LangChain instead of the older versions that were breaking.
* Added logic to limit size of the LLM response to fit to the db column size.
* Centralized configurations to `.env` and `config.py`.
* Consolidated all dependencies to `requirements.txt`.

### Environment Setup

#### Create .env file in the parent folder i.e., LLM_QUERY_CACHING and populate the parameters.

```
OPENAI_API_KEY=YOUR-OPENAI-API-KEY-WITHOUT-QUOTES
```

#### Where are python dependencies?
If you want to install a dependency, add it in `requirements.txt`.

#### Complete setup steps

1. Install Docker Desktop if not already
2. Run the Docker containers: `docker compose -f milvus-standalone-docker-compose.yml up -d`
3. See the status of Docker containers: `docker ps`
4. Connect to the attu website by opening local host in browser: http://localhost:8000
5. Click Connect button.
6. Get API Key from OpenAI https://platform.openai.com/api-keys
7. Add Credits to the OpenAI account to run this code. A small amount will suffice. https://platform.openai.com/settings/organization/billing/overview
8. Paste API Key In the code in `.env` file.

#### How to delete the docker containers
Run this command on Terminal: `docker compose -f milvus-standalone-docker-compose.yml down`