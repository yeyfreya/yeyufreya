# Freya (Ye) Yu

I build LLM systems end to end — orchestration, retrieval,
evaluation, and the tracing that tells you whether they actually worked.

### Currently building — [AI Compliance Gap Analyzer](https://github.com/yeyfreya/ai-compliance-gap-analyzer)

An open-source agent that maps regulatory territory, researches it against regulators'
own sources, and returns a reviewable gap report.
**Live, free, no login → [ai-compliance-gap-analyzer.streamlit.app](https://ai-compliance-gap-analyzer.streamlit.app/)**

Four-stage Python pipeline — scope → tiered research → analysis → report. Two Claude
calls with structured-JSON scoping, official-domain-first live retrieval via Tavily,
run-level tracing through Langfuse and OpenTelemetry, Supabase persistence.
No vector store: the corpus is the live web and regulations change, so retrieval
happens at search time by design.

I held the v0.6 release after a primary-source audit found 4 of 7 checked claims wrong
or misattributed, and rebuilt around scope-before-search rather than prompting the model
to sound more authoritative. Source-tier leakage and ranking instability are still open.
[The iteration notes](https://github.com/yeyfreya/ai-compliance-gap-analyzer/blob/main/docs/iterations/v0.7-research-scoping-and-source-tiering.md)
are where I write down what didn't work.

### Also

**NemoSafe** (NVIDIA Spark hackathon) — evaluation and orchestration lead. Built the
controller, staged scoring, and packaged harness for multi-turn safety evaluation across
71 conversations and 2,840 turns, preserving unparseable results as `insufficient_data`
rather than letting them read as passes.

**VoiceVibe** — real-time speech emotion recognition, TensorFlow with a custom Librosa
audio pipeline, deployed to Azure and Hugging Face.

### Stack

Python · Claude API · Tavily · Langfuse · OpenTelemetry · Supabase / Postgres ·
Streamlit · TensorFlow · TypeScript · Git

---

Joint inventor on a pending U.S. patent application.
Founder of **AI + Sun**, a Seattle gathering series for AI builders.
Community Steward, AIGovOps Foundation.

📍 Seattle · [LinkedIn](https://linkedin.com/in/yeyufreya)
