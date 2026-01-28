

# In-Context Learning and Prompt Templates for Advanced AI

<img src="prmpt engineering.png" alt="description" style="width:100%; height:auto;" />
This Jupyter notebook provides a comprehensive tutorial on **prompt engineering techniques** using IBM watsonx.ai and LangChain. Learn foundational concepts, advanced in-context learning methods, and practical applications.

## ✨ **What You'll Learn**

- **Prompt Engineering Basics**: Zero-shot, one-shot, few-shot, Chain-of-Thought (CoT), Self-consistency
- **LangChain Integration**: Structured prompt templates & LLM chains
- **Real-world Applications**: QA bots, text summarization, classification, code generation, role-playing
- **Hands-on Exercises**: Parameter tuning & advanced prompting techniques

##  **Quick Start**

# Clone & Install
git clone <your-repo-url>
cd In-Context-Learning-and-Prompt-Templates-for-Advanced-AI

# Install dependencies (pinned versions for compatibility)
pip install --user ibm-watsonx-ai==0.2.6
pip install --user langchain==0.1.16  
pip install --user langchain-ibm==0.1.4

# Restart kernel & run notebook
jupyter notebook In-Context-Learning-and-Prompt-Templates-for-Advanced-AI.ipynb
📋 Table of Contents
text
1. [Setup](#setup) - Environment & IBM Granite model
2. [Prompt Engineering](#prompt-engineering) - Zero/Few-shot, CoT, Self-consistency
3. [LangChain Applications](#applications) - 5 practical agents
4. [Exercises](#exercises) - Hands-on challenges
5. [Customization](#customization) - Local deployment
🛠 Setup
Prerequisites
Python 3.8+ (Jupyter, Colab, VS Code)

IBM watsonx.ai account (demo credentials included)

LLM Initialization
python
def llm_model(prompt, params=None, model_id="ibm/granite-3-2-8b-instruct"):
    # Uses watsonx.ai Granite model with custom parameters
    # temperature=0.5, max_new_tokens=256, top_p=0.2
    pass
🎯 Prompt Engineering Techniques
Technique	Example	Use Case
Zero-shot	Classify: "Eiffel Tower is in Berlin" → False	Fact checking
One-shot	English→French translation with 1 example	Language tasks
Few-shot	Emotion classification with 3 examples → Fear	Pattern recognition
Chain-of-Thought	Apple inventory math → Step-by-step reasoning	Complex math
Self-consistency	Age puzzle → 3 calculations converge on 67	Reasoning validation
🤖 LangChain Applications
1. Text Summarization
python
template = "Summarize the content in one sentence."
# Input: 5-paragraph tech article
# Output: "21st century tech revolutionized healthcare, education, transportation"
2. Question Answering
python
content = "Solar system inner planets: Mercury, Venus, Earth, Mars (rocky)"
question = "Which planets are rocky?"
# Output: "Mercury, Venus, Earth, Mars"
3. Text Classification
python
text = "Concert was exhilarating with great performances"
categories = ["Entertainment", "Music", "Technology"]
# Output: "Music"
4. SQL Code Generation
python
description = "Customers who purchased in last 30 days"
# Output: SELECT with JOIN + DATE_SUB(CURDATE(), INTERVAL 30 DAY)
5. Role-Playing Chatbot
python
role = "game master"
tone = "engaging and immersive"
# Interactive game master conversation loop
🏋️ Exercises
Parameter Tuning: Change temperature=1.0 vs 0.1 → Observe creativity

Verbose Mode: verbose=True → See LLM's thinking process

One-shot Classification: Upgrade zero-shot agent with examples

🔧 Customization
Local Deployment
python
# Replace demo credentials
credentials = {
    "url": "https://us-south.ml.cloud.ibm.com",
    "apikey": "YOUR_API_KEY"
}
project_id = "YOUR_PROJECT_ID"

# Switch models
model_id = "your-preferred-model"
Alternative LLMs
OpenAI GPT via LangChain

Local models (Ollama, Llama.cpp)

Hugging Face Transformers

 Key Parameters
Parameter	Range	Effect
temperature	0.1-1.0	Creativity vs determinism
max_new_tokens	50-1024	Response length
top_p	0.1-0.9	Diversity control
top_k	1-50	Token sampling


⭐ Star this repo if you found it helpful!
