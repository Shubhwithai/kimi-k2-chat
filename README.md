# Chat With Kimi K2 (via Groq)

This is a simple web-based chatbot application built with Streamlit. It allows users to interact with the `moonshotai/kimi-k2-instruct` model, powered by the Groq LPU Inference Engine for fast responses.

## Features

- **Interactive Chat Interface**: A clean and simple UI for chatting with the AI.
- **API Key Management**: Securely enter your API key in the sidebar.
- **New Chat Session**: Easily start a new conversation with the click of a button.
- **View AI's Thought Process**: An expandable section shows the model's `thinking` process before it provides a final answer.
- **Built with**: Streamlit, LangChain, and Groq.

## How to Run

To run this application locally, follow these steps:

**1. Clone the Repository**

```bash
git clone <repository-url>
cd <repository-directory>
```

**2. Install Dependencies**

Make sure you have Python 3.8+ installed. Then, install the required packages:

```bash
pip install -r requirements.txt
```

**3. Get Your API Key**

You will need a Groq API key to use this application.
- Go to the [Groq Console](https://console.groq.com/keys).
- Sign up or log in.
- Create a new API key.

**4. Run the Streamlit App**

```bash
streamlit run app.py
```

**5. Start Chatting**

- Open your web browser to the local URL provided by Streamlit.
- Enter your Groq API key in the sidebar.
- Start asking questions!

## Configuration Note

This application is configured to use the `moonshotai/kimi-k2-instruct` model name with the Groq API endpoint. Please be aware that this specific model may not be available on Groq's platform.

To use a model that is officially supported by Groq (like `llama3-8b-8192` or `mixtral-8x7b-32768`), you will need to update the `model` parameter in the `app.py` file accordingly:

```python
# In app.py, find this line:
chat = ChatOpenAI(
    model="moonshotai/kimi-k2-instruct", # <-- Change this to a Groq model
    openai_api_key=groq_api_key,
    openai_api_base="https://api.groq.com/openai/v1"
)
```
