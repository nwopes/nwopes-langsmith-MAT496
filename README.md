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

Module 1 - Conversational Threads:
    -> Learned how to use LangSmith's Threads feature to group multiple traces into coherent conversations using session_id, thread_id, or conversation_id metadata keys with UUID values. This enables tracking multi-turn conversations and maintaining context across related interactions in chatbot-like applications.
    -> Converted the programming tutor examples into hilarious college student meme-style conversations with relatable existential crises, internet slang, and chaotic good energy while preserving the threading functionality.

Module 2 - Dataset Upload:
    -> Learned how to programmatically create and upload datasets to LangSmith using the LangSmith SDK Client, including preparing input-output pairs and using the create_examples() method for bulk dataset creation. This enables automated dataset management and integration with existing data pipelines for testing and evaluation workflows.
    -> Replaced the LangSmith technical Q&A examples with entertaining random fun facts about animals, space, human body, and nature, creating a more engaging trivia-style dataset while maintaining the same upload functionality.

Module 2 - Evaluators (Auto Evaluators):
    -> Learned about LangSmith's auto evaluators including custom evaluators, LLM-as-judge evaluators, and semantic similarity evaluators. Auto evaluators enable automated assessment of LLM outputs through various scoring methods like semantic similarity (using embedding vectors), LLM-based judgment (using another LLM to score responses), and custom scoring functions with structured outputs using Pydantic models.
    -> Key concepts covered: evaluate() function for running evaluators on datasets, compare_semantic_similarity for embedding-based evaluation, LLM-as-judge with scoring criteria and reasoning, structured evaluation outputs with score/reasoning pairs, and automated evaluation workflows for continuous model assessment.
    -> Converted the LangSmith technical Q&A evaluation examples into fun animal fact scenarios (koala sleep habits, octopus hearts) while preserving the core evaluation methodologies and scoring mechanisms, making the learning process more engaging and memorable.

Module 2 - Experiments:
    -> Learned how to run systematic experiments in LangSmith using the evaluate() function with various parameters including dataset versions (as_of), dataset splits, specific example IDs, repetitions for consistency, concurrency for performance, and metadata for organization. Experiments enable A/B testing different models, comparing performance across dataset subsets, and tracking experiment results with proper categorization.
    -> Updated the TODO comment by adding specific example IDs for running experiments on individual data points, enabling targeted testing of specific examples rather than entire datasets.

Module 2 - Lesson 4:
    -> Learned how to analyze experiment results in the LangSmith website interface at smith.langchain.com, including viewing experiment comparisons, performance metrics, and detailed result breakdowns to understand model behavior and make data-driven decisions for model improvements.

Module 2 - Pairwise Experiments:
    -> Learned how to compare two different experiments head-to-head using pairwise evaluation with LLM-as-judge methodology, enabling direct comparison of different prompts or models without requiring ground truth reference outputs. This approach uses structured evaluation criteria to determine which experiment performs better on a given task.
    https://smith.langchain.com/o/7c0013ad-db6b-4270-a51d-fd50bff1aee4/datasets/a56c3d7b-42a6-4f1d-b621-1edfdc1e7cf3/compare?selectedSessions=f001cf8e-9758-48d1-8fc4-edca2e642ed3%2C5a032600-ed36-4785-b2da-340ffb8eba5a&comparativeExperiment=63bb8538-ab47-4c77-81b0-2185b2cb9ab3&baseline=undefined&compare-experiment-tab=0

Module 2 - Summary Evaluators:
    -> Learned how to create summary evaluators that compute aggregate metrics across entire datasets rather than individual examples, such as F1-score, precision, and recall for classification tasks. Summary evaluators analyze collections of outputs to provide overall performance statistics that can only be calculated at the dataset level.
    Made a toxicity analysis dataset.
    https://smith.langchain.com/o/7c0013ad-db6b-4270-a51d-fd50bff1aee4/datasets/7e92fece-dbe9-4db3-aaec-430dda4ce95b

Module 3 - Playground Experiments:
    -> Learned how to create datasets programmatically using the LangSmith Client and run experiments in the playground interface. This enables systematic testing of prompts and models by creating structured datasets with input-output pairs for evaluation and comparison purposes.
    -> Replaced generic color questions with Batman and Gotham City themed examples to create a more engaging superhero knowledge dataset.

Module 3 - Prompt Hub:
    -> Learned how to connect applications to LangSmith's Prompt Hub for centralized prompt management, including pulling prompts with client.pull_prompt(), testing different prompt versions, and programmatically uploading custom prompts using client.push_prompt() for collaborative prompt engineering workflows.
    -> Modified all example questions and prompts from generic themes to Monkey D. Luffy and One Piece themed content, creating pirate adventure scenarios while maintaining the core prompt management functionality.

Module 3 - Prompt Engineering Lifecycle:
    -> Learned the complete prompt engineering lifecycle using LangSmith, including creating datasets for evaluation, building RAG applications with tracing, and integrating Prompt Hub for centralized prompt management. This demonstrates how to iteratively improve prompts through systematic testing and evaluation workflows.
    -> Replaced technical LangSmith documentation questions with fascinating animal facts (cheetah speed, octopus hearts, elephant sleep patterns, penguin swimming, giraffe tongues) to create an engaging wildlife knowledge base.
```
