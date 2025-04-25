# CMPSC 497 Final Project – Fine-Tuning an LLM for Cybersecurity Solutions

**Author:** Ali B. AlNaseeb  
**Course:** CMPSC 497 - Introduction to NLP  
**Semester:** Spring 2025  
**Instructor:** Dr. Wenpeng Yin

## Overview

This project focuses on fine-tuning a language model (LLM) to generate possible research approaches for various cybersecurity problems. The model takes a short research question as input and responds with one suggested method or idea to explore the topic.

The project was designed and implemented as part of the final deliverable for CMPSC 497 at Penn State.

## Task Description

- Input: A short cybersecurity problem or research question.
- Output: One useful research approach to address the problem.
- Example:
  - **Input:** "How to protect against phishing attacks?"
  - **Output:** "Train an AI model on phishing email datasets and use it to filter suspicious messages in real-time. Combine it with user training programs."

## Dataset

- Size: 10,000 examples
- Format: `.jsonl` (JSON Lines)
- Each entry contains a `problem` and an `approach`
- Topics include:
  - Malware and ransomware
  - Phishing and spam detection
  - Password safety and authentication
  - Insider threats and social engineering
  - AI in cybersecurity
  - USB threats and network security

## Model and Training

- Final Model Used: `distilgpt2` (Hugging Face)
- Fine-tuning method: Standard full-model fine-tuning (no PEFT/LoRA in final version)
- Training steps: ~3000 steps over 4 epochs
- Loss: Final average training loss ≈ 0.124
- Hardware: Google Colab (TPU initially, final model trained on GPU)
- Tools: Hugging Face Transformers, Datasets, Trainer, Gradio

## Testing

- Interface: Gradio UI for easy prompt-response interaction
- Evaluation: Manual testing on ~30 random prompts
- Result: ~85-90% of answers were relevant, clear, and on-topic

## Files

- `cmpsc497_final_cleaned.ipynb` – Final cleaned notebook for GitHub rendering
- `cybersecurity_dataset_10000_unique.jsonl` – Dataset used for fine-tuning
- `README.md` – This file

## Future Work

- Try models like Phi, LLaMA 2, or Mistral for deeper reasoning
- Add evaluation metrics like BLEU or ROUGE
- Include more advanced cybersecurity terms and research tools
- Deploy as a student tool for capstone projects or cyber awareness

## License

This project is for educational purposes under Penn State’s CMPSC 497 course. All data and code are student-generated unless stated otherwise.
