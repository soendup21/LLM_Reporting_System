# LLM Reporting System

A Language Learning Model (LLM) based reporting system that uses Retrieval-Augmented Generation (RAG) to interact with MySQL databases. The system supports both Google's Gemini, OpenAI, and TinyLlama models for natural language query processing.

## Features

- Natural language to SQL query conversion
- Support for multiple LLM models:
  - Google Gemini Pro
  - TinyLlama (local deployment)
- MySQL database integration
- Interactive command-line interface
- Error handling and graceful response generation

## Prerequisites

- Python 3.x
- MySQL Server
- For TinyLlama: Local API endpoint running
- Required Python packages (see Installation section)

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd LLM_Reporting_System
```

2. Install required Python packages:

```bash
pip install mysql-connector-python google-generativeai requests
```

3. Configure your database credentials:

   - Open `gemini.py` or `tinyllama.py`
   - Update the MySQL connection parameters:
     - host
     - user
     - password
     - database

4. For Gemini:

   - Get a Google API key from the Google Cloud Console
   - Set your API key in `gemini.py`

5. For TinyLlama:
   - Ensure your local TinyLlama API is running at `http://localhost:11434/api/generate`

## Usage

### Using Gemini Model

```bash
python gemini.py
```

### Using TinyLlama Model

```bash
python tinyllama.py
```

Once running, you can:

- Type your questions in natural language
- The system will convert them to SQL queries when appropriate
- View the results directly in the terminal
- Type 'exit' to quit the program

## Structure

- `gemini.py`: Implementation using Google's Gemini Pro model
- `tinyllama.py`: Implementation using TinyLlama model
- `test.py`: Test configurations and database connectivity tests
- `README.md`: Project documentation

## Notes

- Both implementations follow similar patterns but use different LLM backends
- The system prefixes SQL queries with '####' for easy identification
- Make sure your MySQL server is running before using the system

## Error Handling

The system includes basic error handling for:

- LLM API connection issues
- Database connection problems
- Query execution errors

## Contributing

Feel free to submit issues and enhancement requests!
