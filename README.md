# Generative AI Chatbot using Streamlit & Gemini

A real-time **Generative AI–powered chatbot** built with **Streamlit** and **Google Gemini (Generative AI API)**.
The application allows users to interact with Gemini in a conversational interface, maintaining chat history across interactions.

---

## Features

* Real-time conversational chatbot using **Google Gemini**
* Streaming responses for instant feedback
* Persistent chat history using Streamlit session state
* Clean and minimal UI
* Lightweight and easy to deploy

---

## Tech Stack

* **Python 3.9+**
* **Streamlit** – Frontend UI
* **Google Generative AI (Gemini)** – LLM backend

---

## Project Structure

```
.
├── app.py          # Main Streamlit application
├── README.md       # Project documentation
└── requirements.txt
```

---

## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/generative-ai-chatbot.git
cd generative-ai-chatbot
```

---

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

---

### 3. Install Dependencies

```bash
pip install streamlit google-generativeai
```

---

### 4. Configure Google Gemini API Key

⚠ **Important Security Note**
Do **NOT** hardcode your API key in production.

#### Recommended (Environment Variable)

```bash
export GOOGLE_API_KEY="your_api_key_here"   # macOS/Linux
set GOOGLE_API_KEY="your_api_key_here"      # Windows
```

Update your code accordingly:

```python
import os
GOOGLE_API_KEY = os.getenv("GOOGLE_API_KEY")
```

---

## Running the Application

```bash
streamlit run app.py
```

The app will be available at:

```
http://localhost:8501
```

---

## How It Works

1. User enters a query in the input box
2. The query is sent to the **Gemini Flash model**
3. Responses are streamed token-by-token
4. Chat history is stored using `st.session_state`
5. Previous messages remain visible throughout the session

---

## Model Used

* **gemini-2.5-flash**

  * Optimized for low-latency and fast responses
  * Ideal for conversational applications

---

## Sample Output

```
You: What is Generative AI?
Bot: Generative AI refers to models that can create new content such as text, images, or code...
```

---

## Limitations

* No user authentication
* Chat history resets on app reload
* API key rate limits apply

---

## Future Improvements

* Environment-based API configuration
* User authentication
* Conversation export (TXT / JSON)
* Multi-model selection
* UI enhancements

---

## Author

**Abhishek Jaiswal**
AI / Python Developer

---

## Disclaimer

This project is for **educational purposes only**.
Ensure compliance with Google Generative AI usage policies.

---

If you want, I can also:

* Create a `requirements.txt`
* Secure the API key fully
* Add screenshots for GitHub
* Convert this into a production-ready app

Just tell me.
