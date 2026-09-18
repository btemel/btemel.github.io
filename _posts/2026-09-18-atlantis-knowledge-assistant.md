---
title: "Atlantis: turning documents into answers you can cite"
date: 2026-09-18
tags:
  - Atlantis
  - RAG
  - AWS
  - Amazon Bedrock
  - Claude
  - side project
---

[Atlantis](https://atlantis.baristemel.com/) is a hobby project I've been building on the side: a private, multi-tenant knowledge assistant that turns your own documents into grounded, cited answers. You upload your files, and instead of hunting through PDFs you just ask a question, and every reply comes back with its sources attached.

## The idea

Large language models are great at sounding confident and terrible at telling you where an answer came from. For a knowledge base you actually rely on, that's the wrong trade. So the whole design of Atlantis rests on one rule: **answers come only from your documents, each with its sources attached.** When the documents don't cover a question, Atlantis says so instead of guessing.

That single constraint shapes everything else: the citations, the "what's missing" report, even the cost tracking.

## A quick tour

**Ask your knowledge base.** Every session opens on a single question box. Curated starter prompts show newcomers what the knowledge base actually holds, and tag filters let you scope a question to just the documents that matter, like a CV, a dataset, or one product line.

**Replies you can trace to a source.** Answers render as rich text, with headings, bold, and lists rather than a wall of prose, and each one carries its sources as expandable citations. A thumbs-up or thumbs-down quietly feeds a knowledge-gap report in the background.

**A knowledge base you control.** You can upload PDFs, Word, PowerPoint, CSV, and text; tag them; re-sync on demand; and watch each file's token count and indexing status. Deleted files move to their own tab rather than vanishing, so nothing disappears silently.

**See what your documents don't cover.** When retrieval comes back empty, or a reader marks an answer unhelpful, the question lands in a knowledge-gaps view. Each row is a hint about a document worth adding, grouped by how often and by how many people it's been asked. Over time, your blind spots become a to-do list.

**Know the bill before it arrives.** There's a near-real-time Bedrock spend estimate, drawn from CloudWatch token metrics and broken down by generation and embedding tokens, so cost never arrives as a surprise.

## Under the hood

Atlantis is built entirely on AWS:

- **Amazon Bedrock Knowledge Bases** and **Claude** for retrieval and generation
- **Aurora Serverless v2** with **pgvector** as the vector store
- **Amazon Cognito** for authentication
- **AWS Lambda** for the backend
- **AWS Amplify** for hosting the front end

Two things I care about in the architecture. First, **privacy and multi-tenancy**: Cognito sign-in gates everything, and every query is scoped to your tenant server-side, derived from your token rather than trusted from the browser. Second, **cost discipline**: the stack is engineered to scale to zero and stay inside the AWS Free Tier, which is exactly what you want from a project you run for fun rather than for a budget.

## Try it

If you want to see it in action, it lives at **[atlantis.baristemel.com](https://atlantis.baristemel.com/)**. It's still an evolving side project, so I'll keep writing here as it grows.
