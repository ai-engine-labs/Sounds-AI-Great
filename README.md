# 🔊 Sounds-AI-Great

An audio intelligence product for speaker-aware transcription, diarization, and inference workflows — built on top of the AI-Engine platform.

---

## 🎯 Purpose

**Sounds-AI-Great** enables:
- Multi-speaker diarization
- Real-time or batch audio transcription
- Inference-ready outputs for NLP, call analysis, and UX insights

---

## 🧰 Core Features

- 🎙️ Audio file intake via CLI, mobile, or REST API
- 🧠 Automatic model selection (e.g. WhisperX vs AssemblyAI)
- 🧩 Configurable diarization strategies (local vs remote)
- 📦 Structured output (`.json`, `.txt`, `.srt`)
- 🔁 Queue-based processing with retries and timeouts
- 📊 Built-in metrics & structured logs

---

## 🛠️ Quickstart (Developer Setup)

```bash
cd products/sounds-ai-great/
cp config/example.local.yaml config/local.yaml
bash workflows/run_e2e_pipeline.sh
```

## 🗺️ Folder OveCrview
```bash
sounds-ai-great/
├── workflows/
│   ├── run_e2e_pipeline.sh      # Local orchestrator
│   ├── upload_audio.py          # CLI audio sender
│   └── benchmark_notes.md       # Model benchmarks
│
├── config/
│   └── local_pipeline.yaml      # Input, diarization, output strategies
│
├── assets/
│   └── sample.amr               # Sample call audio
│
└── README.md
```


## 🔗 Powered By

- AI-Engine-Core: our MLOps backend (not exposed here)
- whisperx, pyannote.audio: used via integration adapters
- queue.py, selector.py, inference_worker.py: part of backend pipeline (abstracted from this repo)

## 🚀 Developer Onboarding

- Clone this repo and the AI-Engine core
- Start local queue and engine via Docker
- Run CLI or script inside workflows/
- Inspect logs, outputs, and metrics
