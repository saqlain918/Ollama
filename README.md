## Ollama Learning Project

This project documents my learning and hands-on implementation of Ollama — a tool for running AI models locally on your laptop. It includes practical examples and code for working with both base and customized models.

## What I Learned

- Understanding what Ollama is and how it runs AI models locally
- Implementation and testing of Ollama models using HTTP API and Python SDK
- Difference between base models and customized models in Ollama
- Creating customized models and comparing outputs with base models
- Local AI model deployment and management

## Features

- Local AI model execution without cloud dependencies
- HTTP API integration for model interaction
- Python SDK implementation examples
- Custom model creation and configuration
- Model comparison capabilities
- Resource management and optimization

## Installation (Windows)

1. Download Ollama:
   - Visit: https://ollama.com/download
   - Download the Windows installer and complete the setup

2. Verify installation:
   ```
   ollama --version
   ```
   If not recognized, add Ollama's installation folder to your Windows PATH environment variable

3. Run a model (example with Llama 2):
   ```
   ollama run llama2
   ```
4. Ollama differnet models link you can see all ollama models below both links:
    ```
   https://github.com/ollama/ollama
   https://ollama.com/search
   ```
## How to use

Since project files (Python scripts) are already uploaded to GitHub:

1. Clone/download the repository
2. Make sure Ollama server is running in the background
3. Ensure Python is installed with proper environment setup (recommended: PyCharm or venv)
4. Install required dependencies:
   ```
   pip install requests ollama
   ```
5. Run existing Python scripts:
   ```
   python filename.py
   ```
6. To stop Ollama service, close the CMD window or stop the service manually

## Creating Customized Models

1. Create a Modelfile (text file) with custom instructions:
   ```
   FROM llama2
   SYSTEM "You are a helpful tutor that explains in very simple words."
   ```

2. Build the customized model:
   ```
   ollama create my-tutor -f Modelfile
   ```

3. Run and compare outputs:
   ```
   ollama run llama2
   ollama run my-tutor
   ```

## Project Structure

```
ollama-learning-project/
├── sample_request.py        # HTTP API implementation examples
├── package.py               # Python SDK usage examples
├── Modelfile                # Example custom model definition
└── README.md                # Project documentation
```

## Dependencies

- requests
- ollama

## Requirements

- Windows OS (installation guide provided for Windows)
- Python 3.10+
- Ollama installed and configured
- Sufficient local storage for AI models
- RAM for model execution (varies by model size)

## Key Concepts

**Base Models:** Standard pre-trained models available through Ollama

**Customized Models:** Modified versions with specific instructions or behaviors

**HTTP API:** RESTful interface for model interaction

**Python SDK:** Native Python library for seamless integration

**Modelfile:** Configuration file defining custom model parameters

## Use Cases

- Local AI development and testing
- Privacy-focused AI applications
- Offline AI model deployment
- Custom AI assistant creation
- Educational AI experimentation
- Resource-controlled AI inference

## Notes

- Models run locally without internet dependency after download
- Resource usage varies by model size and complexity
- Custom models inherit base model capabilities with added instructions
- Ollama manages model lifecycle and resource allocation
- Supports multiple models running simultaneously

## Built with

- Python
- Ollama
- Local AI model infrastructure

## Summary

Ollama enables local AI model execution on laptops, supporting both HTTP API and Python SDK integration. The project demonstrates creating customized models and comparing them with base models, providing a complete local AI development environment.
