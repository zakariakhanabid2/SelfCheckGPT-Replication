# SelfCheckGPT Replication & Cross-Domain Evaluation

## Overview
This repository contains the codebase and datasets for evaluating zero-resource hallucination detection in Large Language Models (LLMs). Building upon the [SelfCheckGPT](https://arxiv.org/abs/2303.08896) methodology, this project replicates the original NLI-based evaluation on the XSum dataset and extends the framework to evaluate a newly constructed, manually annotated custom dataset.

The core objective is to demonstrate how effectively the SelfCheckGPT-NLI approach generalizes across different domains using stochastic sampling, without relying on external databases or ground-truth references during the evaluation phase.

## Repository Structure

- `extended_SelfCheckGPT.ipynb`: The primary Jupyter Notebook containing the full pipeline. Includes XSum evaluation, custom dataset evaluation, and comparative visualizations (ROC and PR curves).
- `constructed_dataset_annotated.json`: The custom domain dataset containing LLM-generated sentences, stochastic samples, and manual ground-truth annotations (0 for factual, 1 for hallucination).
- `requirements.txt`: (Optional) List of required Python packages to run the environment.

## Key Features

1. **SelfCheckGPT-NLI Implementation**: Uses Natural Language Inference to detect contradictions between a primary LLM response and stochastically generated samples.
2. **Original Dataset Replication (XSum)**: Computes baseline performance metrics (ROC-AUC, PR-AUC) for hallucination detection on news summarization.
3. **Custom Domain Extension**: Evaluates the methodology on a custom dataset, proving cross-domain adaptability.
4. **Comparative Visualizations**: Generates side-by-side ROC and Precision-Recall curves, alongside random guessing baselines, for rigorous academic analysis.

## Setup & Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies:**
   Ensure you have Python 3.8+ installed. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
   *(Core dependencies include: `numpy`, `matplotlib`, `scikit-learn`, `tqdm`, and the required transformers/NLP libraries for SelfCheckGPT).*

## Usage

1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook extended_SelfCheckGPT.ipynb
   ```
2. Run the cells sequentially. The notebook is divided into:
   - Environment setup and model initialization.
   - XSum dataset processing and baseline evaluation.
   - Loading and evaluating `constructed_dataset_annotated.json`.
   - Plotting the final comparative analysis charts.

## Results Summary
The comparative analysis yields ROC-AUC and PR-AUC scores for both the XSum baseline and the custom domain. Detailed side-by-side graphical comparisons are generated at the end of the notebook, illustrating the robustness of the zero-resource methodology. *(Refer to the final project report for in-depth discussion and original vs. custom snippet comparisons).*

## Acknowledgments
- **Original Paper:** [SelfCheckGPT: Zero-Resource Black-Box Hallucination Detection for Generative Large Language Models](https://arxiv.org/abs/2303.08896) by Manakul et al.
- Developed as part of [Insert Course/Program Name, e.g., COMP8220 Data Science Assessment].