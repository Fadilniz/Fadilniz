# n8n projects — Demo, AIRA, no paying clients

- Descriptions only, no raw JSON published
- Raw exports contain real emails and credential references — descriptions first, files only after a full redaction pass

## Appointment booking lifecycle — 20 nodes
- Flow: webhook in, availability and routing checks, Google Sheets and Google Calendar writes, Gmail confirmations, webhook response
- Covered: book, availability check, update, cancel, delete
- Known demo limits: booking-confirmation timeouts, wrong-row Sheet updates

## Multi-tenant call concurrency — 25 nodes
- Tools: n8n, Twilio, HTTP calls
- Flow: webhook in, tenant routing, concurrency checks, overflow path when capacity hit, webhook responses
- Purpose: route and overflow instead of dropping calls when busy

## Call intake and emergency triage — 11 nodes
- Flow: webhook, code, Gmail, Google Calendar, AI agent, branching by case type
- Standalone Emergency Triage file: 2 nodes only, routing piece inside intake, not a full system on its own

## RAG knowledge base — 13 nodes, plus memory workflow
- Tools: Google Drive, OpenAI embeddings, Pinecone vector store, AI agent
- Flow: Drive trigger, document loading, text splitting, embeddings, Pinecone storage, AI agent retrieval
- Retrieval-first answering, not a chatbot prompt alone
