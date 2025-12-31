# RacoAI Junior AI Engineer Task: Fine-Tuning LLaMA 3.1-8B on Bengali Empathetic Conversations

## Overview
Fine-tuned Meta-Llama-3.1-8B-Instruct using Unsloth on Kaggle free GPU for Bengali empathetic conversations.

## Repository Structure
- `/notebooks`: Kaggle notebooks (preprocessing.ipynb, finetuning.ipynb, evaluation.ipynb)
- `/scripts`: Python classes (DatasetProcessor.py, LLAMAFineTuner.py, Evaluator.py, etc.)
- `/data`: Sample processed data or dataset previews
- `README.md`: Project documentation, choices, challenges, results

## Key Choices
- Used **Unsloth** for faster and memory-efficient training
- LoRA config: r=64, alpha=16, target_modules=["q_proj", "v_proj", ...]
- Max sequence length: 8192 (with gradient checkpointing and 4-bit quantization)
- Strategy pattern implemented for swapping LoRA/Unsloth

## Results
- [Will add metrics table after training]
- Sample responses: [Will add examples later]

## Challenges Faced
- Memory issues on Kaggle GPU → solved with 4-bit loading and gradient checkpointing
- Bengali text handling → used full-sequence tokenization

## How to Run
1. Import notebooks to Kaggle
2. Add the Bengali Empathetic Conversations dataset
3. Run notebooks in order
