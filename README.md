# Intro to LangSmith

Welcome to Intro to LangSmith!

## Introduction
In this course we will walk through the fundamentals of LangSmith - exploring observability, prompt engineering, evaluations, feedback mechanisms, and production monitoring. Take a look at the setup instructions below so you can follow along with any of our notebook examples.

---

## Setup
Follow these instructions to make sure you have all the resources necessary for this course!

### Sign up for LangSmith
* Sign up [here](https://smith.langchain.com/) 
* Navigate to the Settings page, and generate an API key in LangSmith.
* Create a .env file that mimics the provided .env.example. Set `LANGCHAIN_API_KEY` in the .env file.

### Set OpenAI API key
* If you don't have an OpenAI API key, you can sign up [here](https://openai.com/index/openai-api/).
* Set `OPENAI_API_KEY` in the .env file.

### Create an environment and install dependencies
```
$ cd intro-to-langsmith
$ python3 -m venv intro-to-ls
$ source intro-to-ls/bin/activate
$ pip install -r requirements.txt
```

### Self-Hosted LangSmith
Note: If you are using a self-hosted version of LangSmith, you'll need to set this environment variable in addition to the others - see this [guide](https://docs.smith.langchain.com/self_hosting/usage) for more info
```
LANGSMITH_ENDPOINT = "<your-self-hosted-url>/api/v1"



Module 0:
    -> changed the promt a bit and learnt that langsmith first retrieves the information and then parces it to then send an output

Module 1 - Tracing Basics:
    -> Learned how to use @traceable decorators for automatic tracing and how to add metadata for better debugging and analysis. The @traceable decorator creates run trees that capture function inputs, outputs, and errors, making it easier to monitor and debug RAG applications.
    -> Modified examples with custom questions, enhanced metadata, increased temperature slightly, and renamed functions to create a personalized RAG system.

Module 1 - Types of Runs:
    -> Learned about different run types in LangSmith (LLM, Retriever, Tool, Chain, Prompt, Parser) and how to properly structure inputs/outputs for each type to get optimal trace visualization. Each run type has specific formatting requirements for metadata and data structures to enable proper rendering in LangSmith.
    -> Created educational-themed examples with programming tutor scenarios, custom tool functions for coding difficulty assessment, and enhanced metadata for better categorization and filtering.

Module 1 - Alternative Tracing Methods:
    -> Learned about different tracing approaches in LangSmith including LangGraph automatic tracing, @traceable decorators with context managers, wrap_openai for automatic OpenAI call tracing, and RunTree API for manual trace control. Each method offers different levels of control and automation for different use cases.
    -> Transformed all examples into naruto themed scenarios with ninja knowledge systems while maintaining the technical learning objectives of each tracing method.
```
