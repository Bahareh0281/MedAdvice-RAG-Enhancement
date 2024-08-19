# Natural Language Processing: Final Project 1

## Project Overview

This repository contains the final project for the **Natural Language Processing** course at the Iran University of Science and Technology (IUST). The project focuses on implementing a **Retrieval-Augmented Generation (RAG)** system, with a specific task of building a **Medical Advisor** that utilizes large language models (LLMs) to provide accurate medical advice based on user queries.

The project is developed under the guidance of **Dr. Marzieh Davoodabadi Farahani** and with the assistance of **Erfan Moosavi Monazzah**.

## Project Objective

The main objective of this project is to familiarize students with the concept of RAG by combining retrieval techniques with generative models. The end goal is to create a system that can:
- Retrieve relevant medical information based on user input.
- Generate coherent and accurate medical advice using an LLM.
    
## Installation Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Bahareh0281/MedAdvice-RAG-Enhancement.git
   cd MedAdvice-RAG-Enhancement
   ```

2. **Set Up the Environment:**
   It's recommended to use a virtual environment:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: `env\Scripts\activate`
   ```

3. **Install Dependencies:**

4. **Download Necessary Models:**
   The project uses the Microsoft Phi-3 model. Ensure you have access to the Hugging Face models:
   ```python
   from transformers import AutoModelForCausalLM, AutoTokenizer
   
   model = AutoModelForCausalLM.from_pretrained("microsoft/Phi-3-mini-128k-instruct")
   tokenizer = AutoTokenizer.from_pretrained("microsoft/Phi-3-mini-128k-instruct")
   ```

5. **Run the Notebook:**
   Open and execute the Jupyter notebook provided in the `Code/` directory.

## Usage

1. **Running the RAG System:**
   The notebook demonstrates the process of using a RAG system to retrieve relevant medical information and generate responses. Follow the steps in the notebook to understand the implementation.

2. **Training and Evaluation:**
   The project includes splitting the dataset into training and test sets, implementing a retriever based on Jaccard similarity, and integrating an LLM for generating responses.

## Project Details

- **Corpus:** The corpus used for retrieval is sourced from the `medalpaca/medical_meadow_wikidoc` dataset on Hugging Face.
- **Retriever:** A simple retriever based on Jaccard similarity is implemented to match user queries with the most relevant documents in the corpus.
- **Generator:** Microsoft Phi-3 is used as the language model to generate coherent medical advice based on the retrieved documents.

## Contributing

Contributions to this project are welcome. Feel free to open an issue or submit a pull request with any improvements or suggestions.

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/Bahareh0281/MedAdvice-RAG-Enhancement/blob/main/LICENSE) file for details.

## Acknowledgments

Special thanks to **Dr. Marzieh Davoodabadi Farahani** for her guidance and **Erfan Moosavi Monazzah** for his assistance throughout the project.
