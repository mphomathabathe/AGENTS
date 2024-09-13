# Azure GPT-4 Functions and Assistants

## Overview

This project implements an AI-driven assistant powered by **Azure OpenAI’s GPT-4** and deployable via  **Azure Functions** . It uses Azure serverless architecture to invoke GPT-4 for tasks like answering queries, executing specific functions, and providing intelligent assistance through REST APIs.

## Features

* **GPT-4 Integration** : Leverage GPT-4 to handle a variety of AI-powered tasks.
* **Azure Functions** : Serverless function calls for on-demand execution of AI logic.
* **Function Calling** : Integrate function calling within the assistant to handle specific tasks based on user input.
* **Configuration Management** : Store API keys and other sensitive configurations securely.
* **Interactive Notebooks** : Use Jupyter notebooks for prototyping and experimentation.

## Project Structure

Here’s a breakdown of the key files in the project:
├── .gitignore                   # Git ignore file to exclude unnecessary files from version control
├── assistant_with_function_calling.ipynb  # Jupyter notebook for developing and testing assistants with function calling
├── assistants.py                # Python script defining assistant behaviors
├── config.json                  # Configuration file containing API keys and settings
├── config.py                    # Python script for loading and managing configurations
├── core.py                      # Core logic and functionality of the GPT-4 assistant
├── dark_sine.png                # A PNG image (possibly for documentation or UI purposes)
├── main.py                      # Main script to run and deploy the project
├── README.md                    # Project documentation (this file)
├── scratchpad                   # A file or directory for miscellaneous notes or temporary work

## File Details

* **`assistant_with_function_calling.ipynb`** : This Jupyter Notebook allows you to prototype and experiment with your assistant and test function-calling capabilities.
* **`assistants.py`** : This file defines the various assistants you are building using GPT-4. It may include logic for text generation, conversation flows, or specific assistant behaviors.
* **`config.json`** : The `config.json` holds sensitive data like API keys, endpoint URLs, and other configurations required to connect to Azure OpenAI and other Azure services.
* **`config.py`** : Python file responsible for loading and handling configurations from `config.json`, ensuring secure and flexible configuration management.
* **`core.py`** : Core functionality of the assistant and business logic resides in this file, possibly including the handling of requests and calling the GPT-4 API.
* **`main.py`** : The entry point of the project. This script could be used to initialize the Azure Functions or run the assistant service locally for testing.
* **`dark_sine.png`** : A supporting image, possibly used for the project’s documentation, branding, or UI.
* **`scratchpad`** : A file or directory used for temporary notes, code snippets, or experimental ideas during development.

## Installation and Setup

### Prerequisites

* **Azure Subscription** : Ensure you have access to Azure OpenAI and Azure Functions.
* **Python 3.x** : Install Python and necessary packages.
* **Jupyter Notebook** : Required for running the notebook files.

### Setup Steps

1. **Clone the Repository** :

```
git clone <repository_url>
cd azure-gpt4-assistants 
```

2. **Install Dependencies: Install the necessary Python packages using pip** :

```
pip install -r requirements.txt
```

3. **Configure API Keys: Update the config.json file with your Azure OpenAI API key and any other necessary configurations.**

```
pip install -r requirements.txt
```

4. **Run Locally: Run main.py to test the assistant locally before deploying it** :

```
python main.py
```

### Jupyter Notebook Usage

* Open the assistant_with_function_calling.ipynb file in Jupyter Notebook to interactively test and develop assistant functionality. This is useful for debugging and prototyping.

### Deployment

To deploy your assistants on  **Azure Functions** :

1. **Deploy to Azure** :
   Use the Azure CLI or Visual Studio Code to deploy the functions:

```
func azure functionapp publish <APP_NAME>
```

2. **Monitor Performance** : Use Azure Monitor to track usage, errors, and performance for your deployed functions.

### Usage

 Once deployed, you can access your assistant via an HTTP endpoint. For example, using curl:

```
curl -X POST https://`<your-function-url>`
-H "Content-Type: application/json"
-d '{"prompt": "Tell me about Azure GPT-4"}'
```

## License

This project is licensed under the MIT License.

---
