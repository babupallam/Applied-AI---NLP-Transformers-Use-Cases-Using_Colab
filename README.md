# Transformers Use Cases in Google Colab

This repository provides a Google Colab notebook demonstrating three key use cases using the Hugging Face `transformers` library:

1. **Question Answering**
2. **Text Summarization**
3. **Text Generation**

The notebook also includes evaluation metrics for each task to measure the performance of the models.

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Usage](#usage)
  - [Question Answering](#question-answering)
  - [Text Summarization](#text-summarization)
  - [Text Generation](#text-generation)
- [Evaluation](#evaluation)
- [License](#license)

## Overview

The Colab notebook showcases how to leverage the `transformers` library for various natural language processing (NLP) tasks. It uses pre-trained models from Hugging Face to:

1. **Answer questions** based on a given context.
2. **Summarize** long pieces of text.
3. **Generate** coherent and contextually relevant text based on prompts.

## Requirements

To run the notebook, ensure you have the following:

- Google Colab environment
- Internet connection (for downloading models)

The `transformers` library is the primary dependency. It will be automatically installed in the Colab environment.

## Usage

### Question Answering

In this section, the notebook demonstrates how to use a pre-trained model to answer questions based on a given context. The model processes the context and the question to generate an accurate answer.

#### Example
```python
from transformers import pipeline

qa_pipeline = pipeline("question-answering")

result = qa_pipeline({
    'context': "Hugging Face is a company based in New York City.",
    'question': "Where is Hugging Face based?"
})

print(result['answer'])
