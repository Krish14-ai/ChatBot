# ChatBot

A simple conversational chatbot built with Streamlit and LangChain. It uses Google's Gemini model and keeps the conversation history in the current Streamlit session so the model can respond with context.

## Requirements

- Python
- A Google AI API key with access to the configured Gemini model

## Setup

1. Clone or download this repository, then open a terminal in the project directory.
2. (Optional but recommended) Create and activate a virtual environment:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

3. Install the dependencies:

   ```powershell
   python -m pip install streamlit langchain-google-genai python-dotenv
   ```

4. Create a `.env` file in the project directory and add your API key:

   ```dotenv
   GOOGLE_API_KEY=your_google_ai_api_key
   ```

   Keep this key private and do not commit the `.env` file.

## Run the app

From the project directory, start Streamlit:

```powershell
python -m streamlit run Bot\ChatBot.py
```

Streamlit will print a local URL to open in your browser. Enter a message in the chat box to start a conversation.
