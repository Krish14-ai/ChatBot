# ChatBot

ChatBot is a lightweight conversational application built with Streamlit and LangChain. It uses a Gemini model from Google to generate responses and keeps the current chat history in the browser session so the model can respond with context during the same conversation.

## Features

- Simple chat interface powered by Streamlit
- Context-aware responses using chat history
- Easy local setup with Python and a Google AI key
- No database or backend service required

## Tech Stack

- Python
- Streamlit
- LangChain
- Google Gemini via `langchain-google-genai`
- `python-dotenv` for environment management

## Prerequisites

- Python 3.9 or newer
- A Google AI API key with access to the Gemini model you want to use

## Installation

1. Clone or download this repository.
2. Open a terminal in the project folder.
3. Create and activate a virtual environment:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

4. Install the dependencies:

   ```powershell
   python -m pip install streamlit langchain-google-genai python-dotenv
   ```

5. Create a `.env` file in the project root and add your Google API key:

   ```dotenv
   GOOGLE_API_KEY=your_google_ai_api_key
   ```

   Keep this file private and do not commit it to version control.

## Running the App

Start the application from the repository root:

```powershell
python -m streamlit run Bot\ChatBot.py
```

This opens a local Streamlit page in your browser. Type a message in the chat box to begin the conversation.

## Project Structure

```text
ChatBot/
├── Bot/
│   └── ChatBot.py
├── .env
├── README.md
└── .venv/
```

## Notes

- Chat history is stored in the current Streamlit session and is not persisted after the session ends.
- The app sends the current conversation history to the model on each turn so it can maintain context.
- If you want to change the model or its configuration, update the relevant settings in `Bot/ChatBot.py`.
