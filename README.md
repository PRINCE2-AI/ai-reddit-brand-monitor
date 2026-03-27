# AI Reddit Brand Monitor

A Streamlit-based web app that monitors brand mentions on Reddit, analyzes sentiment, classifies topics, and detects urgency using a local Ollama AI model.

## Features

- Fetches Reddit posts mentioning your brand in real time
- Sentiment analysis (Positive / Negative / Neutral)
- Topic classification (Bug, Feature Request, Price Complaint, etc.)
- Urgency detection (High / Low)
- Auto-generated summaries for positive, negative, and suggestion feedback
- Interactive dashboard with charts

## Tech Stack

- **Frontend:** Streamlit
- **Reddit API:** PRAW (Python Reddit API Wrapper)
- **AI Model:** Ollama (`mistral:7b` running locally)
- **Database:** SQLite
- **Visualization:** Plotly

## Requirements

- Python 3.8+
- [Ollama](https://ollama.ai/) installed locally with `mistral:7b` model pulled
- Reddit API credentials (Client ID & Client Secret)

## Setup & Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Pull the Ollama model**
   ```bash
   ollama pull mistral:7b
   ```

4. **Run the app**
   ```bash
   streamlit run app.py
   ```

5. **Enter your Reddit API credentials** in the sidebar when prompted.

## Getting Reddit API Credentials

1. Go to [https://www.reddit.com/prefs/apps](https://www.reddit.com/prefs/apps)
2. Click "Create App" → select **script**
3. Copy the **Client ID** and **Client Secret**

## Project Structure

```
.
├── app.py              # Main Streamlit UI
├── backend_utils.py    # Database, Reddit API, Ollama logic
├── requirements.txt    # Python dependencies
└── README.md
```

## Note

The `brand_monitor.db` SQLite database is created locally at runtime and is excluded from version control via `.gitignore`.
