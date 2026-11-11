# Hi, I'm Bibekananda Nayak 👋

**Software Engineer · Applied AI · Bengaluru**

I build AI agents end to end: real-time voice agents, autonomous browser agents, and long-term memory for LLMs. I care about the parts that make agents work in production, such as low-latency streaming, typed tool calling, context engineering, retrieval, and cost tracking. By day I ship consumer apps at **Swiggy**, and I write about what I learn almost daily.

🌐 [bibekananda.in](https://www.bibekananda.in/) · ✍️ [188 posts on AI](https://www.bibekananda.in/blog/) · 💼 [LinkedIn](https://www.linkedin.com/in/bibekanandan892/) · 📬 [Email](mailto:bibekanandan892@gmail.com)

## 🤖 AI projects

### [VyaparPay Voice Support Agent](https://github.com/bibekanandan892/vyaparpay-voice-agent)

Asha, a voice AI support agent that can see the user's screen, so it opens a support call already knowing what went wrong.

- **Streaming voice loop:** Deepgram STT, Claude via OpenRouter, and sentence-chunked TTS, with Silero VAD and barge-in.
- **Screen-aware context:** an on-device compiler turns a ~4,000-token UI tree into a ≤300-token semantic snapshot, including API errors that were never drawn on screen.
- **Typed tool calling:** Pydantic in/out tools, where account facts are always fetched and the one mutating tool is gated on a spoken confirmation.
- **Memory and RAG:** rolling summarization, profile merge, and pgvector semantic memory, with per-call cost tracking.
- **Hand-rolled WebRTC:** two direct peers (libwebrtc and aiortc) with my own signaling protocol and self-hosted coturn, no managed voice platform.
- **Status:** confirmed working end to end as a live two-way call on a real device.

`Python` `FastAPI` `aiortc` `WebRTC` `pgvector` `Deepgram` `ElevenLabs` `OpenRouter`

### [AI Job Application Agent](https://github.com/bibekanandan892/ai-job-application-agent)

An autonomous, local-first agent that searches, ranks, and applies to roles, with a human in the loop.

- **LangGraph orchestrator:** scout → score → apply → verify, with a SQLite checkpointer.
- **Browser automation:** persistent Playwright sessions with platform adapters for LinkedIn Easy Apply and Greenhouse.
- **Resume tailoring:** an embedding-scored bullet picker, then an LLM rewrite with a "do-not-invent" guard, plus a cover letter agent.
- **LLM layer:** Anthropic client with prompt caching, retries, and cost tracking, behind a Groq/Anthropic provider abstraction.
- **Oversight:** FastAPI WebSocket API and a Next.js dashboard with live event streaming and supervisor controls.

`Python` `LangGraph` `Playwright` `FastAPI` `Next.js` `Anthropic SDK`

### [Memento + MemLayer](https://github.com/bibekanandan892/agentice-memory)

A personal AI assistant with real memory, built on a from-scratch Mem0-style memory library.

- **Two-phase write path:** an extractor call turns a conversation into candidate facts, and a reconciler call decides `ADD` / `UPDATE` / `DELETE` / `NONE` against existing memories.
- **Anti-hallucination id remap:** the model can never invent a plausible-looking memory id.
- **User-sharded vector store:** a search physically cannot see another user's rows.
- **Memory taxonomy:** every fact is tagged semantic, episodic, or procedural.
- **Front ends:** CLI, REST, and an MCP server, running on Gemini with local embeddings.

`Python` `Gemini` `sentence-transformers` `SQLite` `FastAPI` `MCP`

### 🔬 Currently researching

**Memory in LLMs:** comparing vector-similarity recall, rolling summarization, and structured episodic stores for agent memory across sessions.

## ✍️ Writing

Notes on what I'm learning, in my own words. 188 posts in 2026 so far, all on AI. A few by theme:

- **Agents:** [The agent loop](https://www.bibekananda.in/blog/agent-loop/) · [AI agent memory](https://www.bibekananda.in/blog/ai-agent-memory/) · [AI agent evaluation](https://www.bibekananda.in/blog/ai-agent-evaluation/) · [MCP](https://www.bibekananda.in/blog/mcp/) · [Context engineering](https://www.bibekananda.in/blog/context-engineering/)
- **Voice agents:** [Stopping speech the instant the user interrupts](https://www.bibekananda.in/blog/stopping-speech-on-interruption/) · [Barge-in in voice agents](https://www.bibekananda.in/blog/barge-in-in-voice-agents/) · [Endpointing in voice agents](https://www.bibekananda.in/blog/endpointing-in-voice-agents/) · [Backchannels in voice agents](https://www.bibekananda.in/blog/backchannels-in-voice-agents/)
- **RAG:** [Agentic RAG](https://www.bibekananda.in/blog/agentic-rag/) · [Chunking strategies for RAG](https://www.bibekananda.in/blog/chunking-strategies-for-rag/) · [Contextual retrieval](https://www.bibekananda.in/blog/contextual-retrieval/) · [Embeddings](https://www.bibekananda.in/blog/embeddings/)
- **LLM internals:** [Decoding the transformer architecture](https://www.bibekananda.in/blog/decoding-transformer-architecture/) · [KV cache in LLMs](https://www.bibekananda.in/blog/kv-cache-llm-inference/) · [Log probabilities (logprobs) in LLMs](https://www.bibekananda.in/blog/logprobs-in-llms/) · [Fine-tuning](https://www.bibekananda.in/blog/fine-tuning/)
- **Safety:** [Prompt Injection in LLMs](https://www.bibekananda.in/blog/prompt-injection/) · [Jailbreaking in LLMs](https://www.bibekananda.in/blog/jailbreaking-in-llms/)

More at [bibekananda.in/blog](https://www.bibekananda.in/blog/).

## 🛠️ What I reach for

- **Applied AI:** Anthropic SDK, OpenAI SDK, Gemini, LangGraph, MCP, tool calling, prompt caching, context engineering
- **Retrieval and memory:** embeddings, pgvector, RAG, rolling summarization, episodic memory stores
- **Voice:** WebRTC (aiortc, libwebrtc), Deepgram STT, ElevenLabs TTS, Silero VAD, barge-in
- **Agents and automation:** Playwright agents, human-in-the-loop dashboards
- **Backend:** Python, FastAPI, Ktor, Node / Next.js, PostgreSQL, MongoDB, REST + WebSocket
- **Platform:** AWS, Linux, Docker, GitHub Actions
- **Mobile:** Kotlin, Jetpack Compose, Compose Multiplatform, ML Kit / on-device

## 💼 Experience

**Software Engineer I · Swiggy** (Feb 2025 – Present)

- Consumer apps used by tens of millions of users every day.
- Feature work in a large monorepo, plus performance and startup-time investigations.

**Kotlin Android Developer · iServeU** (Jan 2022 – Feb 2025)

- Built and shipped financial-services apps for India's micro-banking and agent-banking networks.
- Owned modules end to end, from product spec to release, and drove modularisation, build-time reduction, and CI hardening.
- Mentored junior developers and ran code review culture.

## 🎓 Education

**Veer Surendra Sai University of Technology, Odisha**: B.Tech in Electronics and Telecommunication (2019 – 2022)

## 📬 Contact

- **Email:** [bibekanandan892@gmail.com](mailto:bibekanandan892@gmail.com)
- **LinkedIn:** [linkedin.com/in/bibekanandan892](https://www.linkedin.com/in/bibekanandan892/)
- **GitHub:** [github.com/bibekanandan892](https://github.com/bibekanandan892)
- **Website:** [bibekananda.in](https://www.bibekananda.in/)
