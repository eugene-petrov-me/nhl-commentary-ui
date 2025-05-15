# 🏒 nhl-commentary-ui

This repository contains the **user interface** and demo app for generating real-time NHL commentary using the `nhl-commentary-core` engine. Built for rapid testing and prototyping with Streamlit.

---

## 🎯 Purpose

- Showcase AI-generated hockey commentary
- Input NHL game IDs or dates
- Select commentary style (e.g. broadcast, casual, analyst)
- Display and (optionally) voice the commentary
- Allow real-time or on-demand generation using the `nhl-commentary-core`

---

## 🧱 Tech Stack

- **Python + Streamlit** – simple web interface
- **OpenAI API** – for language generation
- **NHL API** – for game and play-by-play data
- **gTTS / ElevenLabs (optional)** – for text-to-speech

---

## 📁 Folder Structure

| Folder / File        | Description |
|----------------------|-------------|
| `pages/`             | Optional Streamlit multi-page layout |
| `static/`            | Assets, images, styling |
| `app.py`             | Main Streamlit app |
| `commentary_client.py` | Interface to `nhl-commentary-core` (e.g. via subprocess or HTTP) |
| `.env.example`       | Environment variable template |
| `requirements.txt`   | Python dependencies |
| `README.md`          | This file |

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/nhl-commentary-ui.git
cd nhl-commentary-ui
```

### 2. Create your .env file
```bash
cp .env.example .env
```
Populate it with:
```bash
OPENAI_API_KEY=your-openai-key
NHL_API_BASE=https://api.nhle.com/stats/rest/
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit app
```bash
streamlit run app.py
```

