# Automated Website Crawling & AI Knowledge Base System (3 n8n Workflows)

This system is built using three connected n8n workflows that automatically collect client data, build an AI-powered knowledge base from their websites, and enable an intelligent chatbot to respond using that data.

# Workflow 1: Client Fetch & Scheduler
The first workflow acts as the automation trigger and client manager.

## How It Works:
  - Runs automatically every Monday at 1:00 AM.
  - Fetches all client records from a connected Google Sheet.
  - Iterates through each client entry.
  - Passes the client data to the second workflow for website crawling and processing.

## Purpose:
  - Fully automated weekly updates
  - Centralized client management
  - Hands-free data processing pipeline
This ensures every client website is regularly refreshed and synchronized with the system.

# Workflow 2: Website Crawling & Knowledge Base Creation
The second workflow is responsible for transforming a client’s website into a structured AI-ready knowledge base.

## What It Does:
Crawls the entire client website.
Extracts all relevant textual content.
Processes and cleans the content.
Converts the data into vector embeddings for semantic search.
Stores the embeddings inside Supabase as a structured knowledge base.

## Why Embeddings?
Embeddings allow the system to:
  - Understand context and meaning (not just keywords)
  - Perform semantic search
  - Deliver accurate AI-powered responses

## Result:
A fully searchable, AI-optimized knowledge base built directly from the client’s website content.

# Workflow 3: AI Chatbot (Knowledge-Based Assistant)
The third workflow powers the user-facing chatbot.

## How It Works:
  - Users interact with the chatbot through a chat interface.
  - The chatbot converts the user’s question into embeddings.
  - It performs a semantic search inside the Supabase knowledge base.
  - Retrieves the most relevant content.
  - Generates a context-aware response based strictly on the stored website data.

## Key Benefits:
  - Answers are based only on the client’s actual website content
  - Reduces hallucination
  - Improves accuracy and trust
  - Provides instant, automated customer support
