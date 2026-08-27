# PDR Digital Assistant Prototype

A Streamlit-based conversational assistant prototype built with Google's Generative AI SDK.

## What is in this repository

The current application lives under `PDR/` and contains:

- `app.py` — Streamlit UI and chatbot flow
- `requirements.txt` — Python dependencies
- `test.py` — small test/support script

## Current implementation

The application:

- uses **Streamlit** for the user interface
- uses `google.generativeai` for model access
- supports API-key input through Streamlit secrets or a password field
- stores chat messages in `st.session_state`
- defines a fixed guidance prompt covering psychology/PDR theory and career-guidance topics
- includes a light custom UI theme

## Important scope note

This repository is a **software prototype / learning project**. The code uses Çukurova University and PDR-related branding/content in the interface, but this GitHub repository should not be interpreted as an official university service, clinical system or medical/psychological diagnostic tool.

The assistant prompt explicitly instructs the model not to make diagnoses. Any real-world deployment in a student-support or psychological-guidance context would require institutional approval, professional review, privacy controls, safety evaluation and a maintained source-of-truth knowledge base.

## Run locally

```bash
cd PDR
pip install -r requirements.txt
streamlit run app.py
```

The app expects a Google API key either through Streamlit secrets as `GOOGLE_API_KEY` or through the UI input field.

## Tech stack

- Python
- Streamlit
- Google Generative AI SDK

## Status

Prototype / experimental project. The current knowledge content is embedded directly in the Python source rather than retrieved from an externally maintained, cited knowledge base.
