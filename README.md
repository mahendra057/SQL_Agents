# SQL_agents

# AI-Powered SQL Query Agent Using LangChain Framework with Gemini-Pro Model

The **AI-Powered SQL Query Agent** leverages the LangChain framework and Gemini-Pro model to dynamically generate and execute SQL queries. This advanced agent connects to a database, reflects its schema, and uses contextual understanding to simplify SQL query generation and execution.

---

## 🚀 Features

### 1. **Database Connectivity**
- Connects to an AWS RDS instance (`database-1`) with credentials (`admin`, `admin123`).
- Uses the **classicmodels** database for all operations.

### 2. **Dynamic Schema Reflection**
- Utilizes SQLAlchemy to:
  - Reflect database schema dynamically.
  - Display tables and column details for better insights.
- Includes a `get_db_schema` function to fetch and display schema information programmatically.

### 3. **AI-Driven SQL Query Generation**
- Configured **HuggingFace Gemini Pro** model for generating contextually relevant SQL queries.
- Integrates semantic search via `sentence-transformers/all-MiniLM-L6-v2` to enhance question-to-query mapping.

### 4. **Semantic Search and Example Selection**
- Implements `FAISS` with `SemanticSimilarityExampleSelector` to:
  - Find the closest SQL query examples for user input.
  - Improve accuracy in query generation.

### 5. **Tool Integration**
- Employs various tools for SQL operations:
  - **QuerySQLDataBaseTool**: Executes SQL queries.
  - **InfoSQLDatabaseTool**: Retrieves database schema details.
  - **ListSQLDatabaseTool**: Lists all database tables.
  - **QuerySQLCheckerTool**: Validates SQL queries before execution.

### 6. **Dynamic Prompt Construction**
- Utilizes `FewShotPromptTemplate` to:
  - Dynamically create prompts based on user questions.
  - Ensure accurate SQL generation tailored to specific queries.

### 7. **Agent System**
- Builds an agent system using `SQLDatabaseToolkit`.
- Integrates an executor with `tool-calling agent` type for seamless operations.

---

## 🛠️ Core Components

1. **Database Connection**
   - AWS RDS instance: `database-1` with credentials (`admin`, `admin123`).
   - Database: `classicmodels`.

2. **Schema Reflection**
   - Fetch and display database schema using SQLAlchemy.
   - `get_db_schema` function for dynamic schema insights.

3. **Query Generation**
   - Leverages HuggingFace **Gemini Pro** for generating SQL queries.
   - Employs `sentence-transformers/all-MiniLM-L6-v2` for semantic embedding.

4. **Example Selection**
   - Uses FAISS for semantic similarity search.
   - Matches user input to the most relevant SQL query examples.

5. **SQL Tools**
   - `QuerySQLDataBaseTool`, `InfoSQLDatabaseTool`, `ListSQLDatabaseTool`, `QuerySQLCheckerTool`.

6. **LangChain Integration**
   - Builds dynamic prompts with `FewShotPromptTemplate`.
   - Employs `SQLDatabaseToolkit` and `tool-calling agent`.


