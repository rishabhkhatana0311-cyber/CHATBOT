<!--- README for Zero2AgroBrain -->

<p align="center">
  <img src="assets/banner.png" alt="Zero2AgroBrain Banner" width="900"/>
</p>

<h1 align="center">Zero2AgroBrain</h1>

<p align="center">
  <a href="https://zero2agrobrain-d2qp95ropbccofvhmpwc9r.streamlit.app/"><img src="https://img.shields.io/badge/Launch-App-00A3E0?style=for-the-badge&logo=streamlit" alt="Launch App"></a>
  <img src="https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/Status-Prototype-yellow?style=for-the-badge" alt="Status">
</p>

---

## Overview

**Zero2AgroBrain** is a voice-first, AI-based assistant that provides actionable farming guidance—covering fertilizer recommendations, pest management, crop calendars, and other practical advisories for Indian agriculture. The application accepts both **spoken** and **typed** questions, grounds answers with curated knowledge, and delivers responses as **text and audio**.

---

## Live Demo
Open the app: **https://zero2agrobrain-d2qp95ropbccofvhmpwc9r.streamlit.app/**

---

## Features

- **Voice and text input** (Whisper Large V3 for ASR)  
- **Low-latency AI responses** using Groq + LLaMA-3.3 models  
- **Text-to-speech** output using gTTS for accessibility  
- **Streamlit-based web UI** for an easy, responsive interface  
- Curated agricultural knowledge base for region-specific guidance  
- Simple file-based storage for uploaded audio and generated replies

---

## Example Questions

- What is the recommended nitrogen dose for wheat in Punjab?  
- How can I manage aphids naturally in mustard crops?  
- Which month is best for sowing rice?  
- How often should tomato plants be irrigated?  
- Suggest organic manure practices for vegetables.

---

## Architecture

<p align="center">
  <img src="![Uploading architecture_diagram.png…]()
" alt="Architecture Diagram" width="800"/>
</p>

**High-level flow:**  
User (voice/text) → Whisper ASR (if voice) → Preprocess → Semantic retrieval (RAG) → LLaMA-3.3 (Groq inference) → gTTS → User (text/audio)

---

## Assets (included in this repo)

- `assets/banner.png` — Project banner for README and website headers  
- `assets/logo.png` — Simple project logo  
- `assets/architecture_diagram.png` — E2E architecture visual

---

## Tech Stack

- Python 3.x  
- Groq API (LLaMA-3.3 models)  
- Whisper Large V3 (speech recognition)  
- gTTS (text-to-speech)  
- Streamlit (web UI)  

---

## Quickstart (development)

1. Clone the repo:  
```bash
git clone <your-repo-url>
cd Zero2AgroBrain
```

2. Create environment & install dependencies:  
```bash
python -m venv venv
source venv/bin/activate   # or `venv\Scripts\activate` on Windows
pip install -r requirements.txt
```

3. Set Streamlit secrets or environment variable for Groq API key:  
```bash
# streamlit secrets example (recommended)
# .streamlit/secrets.toml
# GROQ_API_KEY = "your_key_here"

# or use environment variable
export GROQ_API_KEY="your_key_here"
```

4. Run the app locally:  
```bash
streamlit run app.py
```

---

## Contribution

Contributions, fixes, and ideas are welcome. To contribute, please open an issue or submit a pull request with a clear description of the changes.

---

## License

This project is released under the **MIT License**. See `LICENSE` for details.

---

## Contact

**Gurpinder Singh** — developer of Zero2AgroBrain  
- GitHub: [gurpinder7473](https://github.com/gurpinder7473)  
- Project: Zero2AgroBrain

---

<p align="center">If this project helped you, a star ⭐ on the repository is appreciated!</p>
