# 🦜 LangChain: Chat with SQL DB

This Streamlit-based application enables users to interact with an SQL database (SQLite or MySQL) using natural language queries powered by LangChain and a Groq-based Large Language Model (LLM). 

The application translates user inputs into SQL queries, executes them on the selected database, and returns the results in an intuitive chat-based interface.

---

## 🚀 Features

- **Natural Language Querying**: Use plain English to retrieve and manipulate database records.
- **Database Options**: 
  - SQLite (`student.db`)
  - MySQL (remote database connection)
- **Seamless Integration**: Combines LangChain’s SQL agent toolkit with a Groq-powered LLM.
- **Interactive UI**: Real-time response streaming and message history for a conversational experience.

---

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- Installed libraries (see `requirements.txt` for details)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/langchain-chat-sql-db.git
   cd langchain-chat-sql-db
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Add your SQLite database file (`student.db`) in the root directory (if using SQLite).

---

## 🗂️ Configuration

### Environment Setup
- Open `app.py` to configure:
  - **SQLite**: Ensure `student.db` exists in the root directory.
  - **MySQL**: Provide host, user, password, and database details in the sidebar when running the app.

### Groq API Key
- Obtain an API key for the Groq-powered LLM.
- Add the key through the sidebar input in the app.

---

## 🏃 Usage

1. Run the application:
   ```bash
   streamlit run app.py
   ```
2. Open the app in your browser (usually at `http://localhost:8501`).

3. Select a database from the sidebar:
   - SQLite: Use the default `student.db` file.
   - MySQL: Input connection details (host, username, password, database name).

4. Enter your Groq API key in the sidebar.

5. Start querying:
   - Example queries:
     - "Show all students in class 10."
     - "What is the average marks of students in section A?"

---

## 🧑‍💻 Code Overview

### Key Components

1. **Database Configuration**:
   - SQLite (`student.db`) is pre-configured.
   - MySQL requires user input for connection parameters.

2. **LangChain Integration**:
   - **`SQLDatabaseToolkit`**: Links the database to the LLM.
   - **`create_sql_agent`**: Converts natural language into SQL queries and executes them.

3. **Streamlit UI**:
   - Sidebar inputs for database selection and API key.
   - Chat interface for interaction.

4. **Session State**:
   - Maintains conversation history during a session.

---

## 🤝 Contributions

Contributions are welcome! Feel free to fork the repository, create a new branch, and submit a pull request.
