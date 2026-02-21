# LLM-Text-Preprocessing-Foundations-Embeddings-
Teller 4 de TDSE
# LLM Embeddings Lab

This project reproduces and explores the core concepts from Chapter 2 of *Build a Large Language Model (From Scratch)* by Sebastian Raschka. The notebook demonstrates how raw text is transformed into numerical representations suitable for training Large Language Models (LLMs). It covers tokenization, sliding window dataset creation, embedding layers in PyTorch, and a small experiment analyzing how `max_length` and `stride` affect dataset size and training efficiency.

---

# Getting Started

These instructions will help you set up the project locally for development and experimentation. The notebook runs entirely on your local machine using Python, PyTorch, and tiktoken.

See the Deployment section for notes on how this could scale in a production environment.

---

# Prerequisites

You need the following installed:

- Python 3.9+
- pip (Python package manager)
- Git (optional, for cloning the repository)

To check if Python is installed:
python --version

If not installed, download it from:

https://www.python.org/downloads/

---

# Installing

Follow these steps to get your development environment running.

---

### Step 1 – Clone the Repository
git clone <your-repository-url>
cd LLM-Embeddings-Lab

---

### Step 2 – Create a Virtual Environment (Recommended)

Say what the step will be:  
Create an isolated environment to manage dependencies.

Example:
python -m venv venv
Activate it:

Windows:
venv\Scripts\activate

---

### Step 3 – Install Dependencies

Say what the step will be:  
Install required libraries for running the notebook.

Example:
pip install torch tiktoken notebook

---

### Step 4 – Launch Jupyter Notebook

Say what the step will be:  
Start the interactive notebook environment.

Example:
jupyter notebook

Open `embeddings.ipynb` and run all cells.

---

### Step 5 – Run the Full Pipeline

Run:

Kernel → Restart & Run All

You should see:

- Total number of tokens
- Number of generated training samples
- Tensor shapes
- Embedding tensor shape:  
  `[num_samples, max_length, embedding_dim]`

This confirms the system is working correctly.

---

# Demo

Example output after running the notebook:

- Tokenized dataset size: 20,000+ tokens (depends on text)
- Samples with stride = 1: large number of overlapping training examples
- Samples with stride = max_length: significantly fewer samples
- Embedding tensor shape: `[N, max_length, embedding_dim]`

This demonstrates how LLMs transform text into structured numerical representations.

---

# Running the Tests

This project does not include automated test scripts, but validation is performed through notebook execution.

## End-to-End Tests

End-to-end validation consists of:

1. Loading text successfully
2. Tokenizing without errors
3. Generating sliding window datasets
4. Converting to PyTorch tensors
5. Passing data through the embedding layer


If no errors occur and shapes are printed correctly, the system passes.

These tests ensure:
- Data pipeline integrity
- Correct tensor dimensions
- Functional embedding layer

---

## Coding Style Tests

While no automated style checker is included, good practices followed:

- Clear variable naming
- Logical cell ordering
- Markdown explanations for conceptual clarity
- Reproducible execution from a clean kernel


This ensures consistent Python formatting.

---

# Deployment

This notebook is designed for educational and local experimentation purposes.

To deploy in a production or research environment:

- Package preprocessing into reusable Python modules
- Replace notebook logic with scripts
- Integrate into a model training pipeline
- Run on GPU-enabled infrastructure (e.g., cloud instances)

For large-scale training, embedding and dataset preparation would be integrated into a distributed training framework.

---

# Built With

- Python
- PyTorch
- tiktoken
- Jupyter Notebook

---

# Contributing

Please read `CONTRIBUTING.md` for details on our code of conduct and the process for submitting pull requests.

---

# Versioning

This project follows Semantic Versioning (SemVer).

For available versions, see the repository tags.

---

# Authors

Digo Rozo – Initial work

Inspired by:
Sebastian Raschka – *Build a Large Language Model (From Scratch)*

---

# License

This project is licensed under the MIT License – see the LICENSE.md file for details.

---

# Acknowledgments

- Sebastian Raschka for the original educational material
- The PyTorch community
- OpenAI for the GPT-2 tokenizer design
- Inspiration from modern Large Language Model research
