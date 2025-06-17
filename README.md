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

Setup Instructions
1. Fine-Tuning the Model
Format your dataset as a .jsonl file (see faq_dataset.jsonl)

Use OpenAI CLI to fine-tune GPT-4o:

bash
Copy
Edit
openai api fine_tunes.create -t "faq_dataset.jsonl" -m gpt-4o
2. Create Telegram Bot
Talk to @BotFather

Set bot name, username, and get the bot token

Use the token in your n8n workflow

3. Set Up n8n
Install or use n8n Cloud

Import the workflow (n8n_workflow.json)

Replace API key and bot token with your values

4. Run the Flow
Your Telegram bot will now respond to guest messages using the fine-tuned model

## Contact

**Prerana Somani**  
Final-year ICT student, PDEU | Incoming MS DS @ Stony Brook  
[LinkedIn](https://www.linkedin.com/in/prerana-somani-672241256/)  
[GitHub](https://github.com/PreranaSomani)
