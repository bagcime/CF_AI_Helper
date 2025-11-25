# CF AI Helper – “Mr. Knows More Than You”

An AI-powered chat application built on Cloudflare’s edge platform.

**Mr. Knows More Than You** is a playful but helpful AI mentor that:

- responds through a clean web chat interface,
- remembers the ongoing conversation (per browser tab),
- runs on a stateful Cloudflare Agent (Durable Object),
- calls a large language model (Llama 3.3) via Workers AI.

This project is designed to meet the requirements of the Cloudflare AI optional assignment:
LLM, workflow/coordination, user input, and memory/state.

---

## Demo – First Page

> Main chat interface served directly from the Worker at `/`.

![CF AI Helper – first page](docs/landing.png)

*(Place a screenshot of the first page at `docs/landing.png` in the repo to see this image on GitHub.)*

---

## Features

### 1. LLM

- Uses **Llama 3.3** via **Cloudflare Workers AI**.
- The model id is configured via `MODEL_ID` in `wrangler.jsonc`:
  ```jsonc
  "vars": {
    "MODEL_ID": "@cf/meta/llama-3.3-70b-instruct-fp8-fast"
  }
