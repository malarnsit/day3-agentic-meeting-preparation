# Agentic AI Meeting Preparation Assistant

## Overview

The Agentic AI Meeting Preparation Assistant helps a manager prepare for an upcoming client meeting.

Instead of manually searching through client documents, previous meeting notes, action items, and historical information, the agent retrieves relevant information and generates a concise meeting preparation brief.

## Objective

The project demonstrates:

- Retrieval-Augmented Generation (RAG)
- Vector search using FAISS
- Short-term memory
- Long-term memory
- Agentic workflow
- Tool usage
- LLM-based reasoning

## Scenario

A manager has a meeting with Acme Corp.

The manager asks:

> Prepare me for my meeting with Acme Corp.

The agent:

1. Identifies the client.
2. Searches client documents.
3. Retrieves previous meeting notes.
4. Retrieves open action items.
5. Retrieves long-term memory.
6. Combines the retrieved context.
7. Generates a meeting preparation brief.
8. Updates short-term and long-term memory.

## Architecture

```text
User
 |
 v
Agent
 |
 +-------------------+
 |                   |
 v                   v
FAISS RAG       Memory Retrieval
 |                   |
 v                   v
Client Docs      SQLite Memory
 |
 +-------------------+
 |
 v
Meeting Notes
 |
 v
Action Items
 |
 v
Context Builder
 |
 v
LLM
 |
 v
Meeting Brief