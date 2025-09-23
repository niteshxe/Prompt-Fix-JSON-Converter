# Prompt Fix & JSON Converter

This is a simple, single-file web application that uses the Gemini API to take a raw, unstructured prompt and convert it into a clear, professionally rewritten prompt and a structured JSON object.

The application runs entirely on the frontend, storing your Gemini API key securely in your browser's local storage. This means no server is required to run the tool.

## ✨ Features

- **Prompt Optimization:** Rewrites your prompt into a concise and effective version for better AI responses.
- **JSON Conversion:** Structures the key components of your prompt into a neat JSON format.
- **Frontend Only:** No backend server required. Just open the `index.html` file in your browser.
- **Secure Key Storage:** Your API key is saved locally in your browser and is not sent anywhere else.
- **Easy to Use:** A simple, clean interface with a character counter and a `Ctrl+Enter` shortcut for quick generation.

## 🚀 Getting Started

To use this tool, follow these simple steps:

1.  **Get your Gemini API Key:**
    - Go to the [Google AI Studio](https://aistudio.google.com/app/apikey).
    - Log in with your Google account.
    - Click "Create API key" to generate a new key for your project.

2.  **Download and Run:**
    - Download the `index.html` file from this repository.
    - Open the file in your web browser (e.g., Chrome, Firefox).

3.  **Enter your API Key:**
    - Paste your API key into the input field at the top of the page.
    - Click the **"Save"** button to store the key securely in your browser's local storage.

4.  **Start Converting Prompts:**
    - Type or paste your raw prompt into the text area.
    - Click the **"FIX"** button or press `Ctrl + Enter` to generate the output.

## 💡 How It Works

The application works by sending your raw prompt to the Gemini API with a specific instruction prompt. The Gemini model then processes this request and returns a JSON object containing the `fixedPrompt` and `jsonPrompt` as instructed.

This is the core instruction prompt sent to the Gemini API:

```text
Take the following user prompt: "[user_prompt]"

1. Rewrite it into a clear, professional prompt easy for AI to understand.
2. Convert it to structured JSON format that breaks down the prompt into key components.
⚠️ Do NOT include markdown, backticks, or explanations.
Format:
{
  "fixedPrompt": "<string>",
  "jsonPrompt" : {
    "key": "value",
    ...
  }
}
