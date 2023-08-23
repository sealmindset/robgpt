# Conversational Retrieval Chain with LangChain and OpenAI

This Python script provides a framework to set up a conversational interface using `langchain` and `openai`. The program ensures that all required modules are installed and then uses the OpenAI API key to access the service.

## Requirements

- Python 3.x
- The required libraries:
    - langchain
    - openai
    - chromadb
    - tiktoken
    - unstructured
    - constants

### Installing Libraries

You can manually install the required libraries using `pip3`:

```
pip3 install langchain openai chromadb tiktoken unstructured constants "unstructured[pdf]"
```

## Features
- Automatic Module Installation: Before execution, the script checks for the required modules and installs missing ones.
- Vectorstore Indexing: Depending on the PERSIST flag, the script either reuses an existing index from the disk or creates a new one from the data/ directory.
- Conversational Interface: Users can engage in a continuous conversational loop with the system. They can enter queries and receive answers based on the data indexed. The conversation can be ended using keywords like quit, q, or exit.

## Usage
- Ensure you have all the required libraries installed.
- Make sure you have your OpenAI API key set in the constants.py file.
- Place your text data in a directory named data/ in the same directory as this script.
- Run the script using:


```
python3 your_script_name.py
```

Or, if you have a specific query to start with:

```
python3 your_script_name.py "Your initial query here"
```

When running the script, you'll be prompted to enter a query. Type in your questions and receive answers based on the indexed data. You can exit the conversation anytime with commands like quit, q, or exit.

# Notes
Set the PERSIST flag to True if you want to save the model to disk and reuse it for repeated queries on the same data.
If you get an import error or any other error during the execution, ensure that all dependencies are correctly installed and the OpenAI API key is correctly set in constants.py.

# Future Enhancements
Expand the knowledge base by adding more data sources to the data/ directory.
Integrate other models or tools for richer conversational experiences.
