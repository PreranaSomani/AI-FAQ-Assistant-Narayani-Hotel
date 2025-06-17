# AI-FAQ-Assistant-Narayani-Hotel

A fine-tuned GPT-4o conversational assistant for Narayani Heights Hotel, deployed via Telegram and automated with n8n. Answers hotel-specific FAQs with precision and rejects irrelevant queries.

## Project Overview

This project is an AI-powered FAQ assistant built for Narayani Heights Hotel using a fine-tuned GPT-4o model. It automatically responds to common guest queries via Telegram and runs fully automated using n8n.

## Problem

Hotels often receive repetitive guest queries about check-in time, room features, restaurant availability, etc. Manual handling or generic bots lead to delays and inconsistent information.

## Solution

A domain-specific FAQ assistant that:
- Responds to 50+ hotel-specific questions
- Rejects irrelevant queries (e.g., “What’s the capital of Italy?”)
- Can be accessed directly by guests via Telegram
- Operates fully automatically via n8n workflows

## Tech Stack

- Model: Fine-tuned GPT-4o (OpenAI)
- Frontend: Telegram Bot
- Automation: n8n workflow
- Prompt Design: Strict, deterministic, hallucination-free

## Key Features

- Short, accurate, hotel-specific responses
- Rejects off-topic questions with fallback replies
- Easy to update via re-fine-tuning on new datasets
- Fully automated Telegram → OpenAI → Telegram flow

## Technical Overview

1. Dataset Preparation: JSONL dataset of 50+ hotel FAQs with rephrased variants
2. Model Training: GPT-4o fine-tuned using OpenAI CLI
3. Query Handling: Prompt fallback to reject off-topic queries
4. Telegram Bot: Created via BotFather and integrated using Telegram API
5. n8n Workflow: Automates query-response loop without manual intervention

## Impact

- Reduces front-desk workload
- Improves guest experience with instant and reliable answers
- Easily scalable to other hotels—just change the dataset and re-train

## Contact

**Prerana Somani**  
Final-year ICT student, PDEU | Incoming MS DS @ Stony Brook  
[LinkedIn](https://www.linkedin.com/in/prerana-somani-672241256/)  
[GitHub](https://github.com/PreranaSomani)
