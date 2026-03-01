# AI Travel Memory Assistant  
AI-powered travel diary system built with n8n, OpenAI and Notion.

## Overview

This project implements a structured AI Agent capable of:

- Storing travel memories via form submission
- Persisting structured data into a Notion database
- Retrieving past trips using an AI agent with tool-based database querying
- Responding strictly based on stored data (no hallucinations)

## Architecture

The system consists of two main workflows:

### 1️⃣ Travel Memory Storage
Form → Data validation → Tag generation → Notion database entry

### 2️⃣ Travel Memory Retrieval
User message → AI Agent → HTTP Tool (Notion API) → Structured response

The AI agent:
- Extracts the destination
- Calls the Notion API via HTTP tool
- Waits for structured results
- Responds only with retrieved data

## Security

- API keys are NOT included in the repository
- Credentials are stored securely in n8n
- Tokens are never committed to Git

## Tech Stack

- n8n
- OpenAI (GPT-4.1-mini)
- Notion API
- HTTP Tool-based Agent architecture

## Setup

1. Import `workflow.json` into n8n
2. Create credentials:
   - OpenAI API key
   - Notion API token (Header Auth)
3. Share your Notion database with your integration
4. Run the workflow

---

This project demonstrates practical AI agent orchestration, secure API handling and structured data retrieval.
