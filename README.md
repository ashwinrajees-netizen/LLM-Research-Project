# GSM8K-Scaffold: Automated Math Problem Classification for Synthetic Tutoring

## Abstract
The effectiveness of Large Language Models (LLMs) in mathematics education increasingly depends on their capacity to deliver adaptive, stepwise guidance. This study investigates the automated classification of problems within the GSM8K dataset as a foundational approach to supporting pedagogical scaffolding. Through the development of a taxonomy-based classification system, we delineate the cognitive requirements and logical frameworks inherent in elementary word problems. Such classification constitutes a necessary step for a dynamic prompt-engineering system aimed at breaking down complex queries into a sequence of scaffolded sub-questions. 

## Key Technical Features
- **4-Bit NF4 Quantization**: Optimized for Google Colab T4 GPUs, reducing the 7B model memory footprint from ~28GB to ~5.5GB using `bitsandbytes` and `transformers`.
- **Stateful Resume Logic**: A built-in 'check-and-resume' strategy that utilizes Google Drive persistence to prevent redundant inference calls.
- **Pedagogical Taxonomy**: Implements a custom refinement layer (`final_polish`) to align mathematical problems with cognitive load theories.

## Repository Structure
- `gsm8k_categorization.ipynb`: The core processing notebook with detailed research annotations.
- `gsm8k_categorized_final.csv`: Initial model classifications.
- `gsm8k_categorized_FINAL_V3.csv`: Refined dataset after pedagogical polishing.

## Installation
```bash
pip install bitsandbytes transformers accelerate datasets
```

## Usage
1. Mount Google Drive to preserve state.
2. Run the environment setup to initialize C-libraries for quantization.
3. Execute the Inference Loop to process the GSM8K dataset.
