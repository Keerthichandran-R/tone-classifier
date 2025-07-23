# tone-classifier
Objective:
An AI-powered NLP application that detects and rewrites message tone across three variants — Formal, Neutral, and Friendly — ideal for customer support and chatbot personalization.

🚀 Features
🧠 Tone Classification – Classifies message tone using a hybrid rule-based + ML model.

✍️ Tone Rewriting Engine – Transforms input messages to match desired tone.

⚙️ FastAPI Interface – Simple RESTful API endpoints for integration with frontend or bots.

🤖 Applications – Useful in rewriting customer emails, chatbot replies, support tickets, etc.

🛠️ Tech Stack
Component	Technology
Backend	Python, FastAPI
NLP Processing	TextBlob, scikit-learn
Model	Rule-based + Machine Learning
Editor/IDE	Visual Studio Code

🧪 Process Overview
Tone Detection:

Extracted features like polarity, subjectivity, exclamation usage, and sentence length.

Applied rule-based heuristics + trained classifier (e.g., Logistic Regression or Naive Bayes).

Tone Rewriting:

Based on the classified tone, used curated transformation rules.

Incorporated synonyms, sentence restructuring, and tone modifiers (using TextBlob + custom logic).

API Development:

Built FastAPI endpoints:

/classify – Detects tone of input text.

/rewrite – Rewrites input to target tone.

Use Cases:

Personalized chatbot messages (tone-adaptive).

Rewrite customer emails in a professional tone.

Humanize robotic responses in automated support.

📦 Installation
bash
Copy
Edit
git clone https://github.com/yourusername/tone-classifier-rewriter.git
cd tone-classifier-rewriter
pip install -r requirements.txt
uvicorn main:app --reload
🔄 API Endpoints
Endpoint	Method	Description
/classify	POST	Returns detected tone of message
/rewrite	POST	Returns rewritten message in desired tone

Sample Request
json
Copy
Edit
POST /rewrite
{
  "text": "I need this done ASAP!",
  "target_tone": "formal"
}
Sample Response
json
Copy
Edit
{
  "rewritten_text": "Kindly ensure this is completed at your earliest convenience."
}
📊 Outcome
A lightweight yet powerful tone-modulation engine ready for integration into:

CRM tools

Customer support software

Chatbots

Email clients

🧠 Future Work
Fine-tuned transformer models (e.g., T5, BART) for advanced tone rewrites.

UI frontend integration.

Multilingual tone detection and rewriting.

