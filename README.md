# ☁️ Azure AI Engineer Associate — AI-102

> **Designing and Implementing an Azure AI Solution**
> 📄 [Official Certification Page](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-engineer/)

![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![AI-102](https://img.shields.io/badge/AI--102-Certification-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)

---

## 📋 Table of Contents

- [Prerequisites](#-prerequisites)
- [Course Sections](#-course-sections)
- [Key Terms](#-key-terms)
- [Section 1 — Planning an Azure AI Solution](#-section-1--planning-an-azure-ai-solution)
- [Section 2 — Implement GenAI Solutions](#-section-2--implement-genai-solutions)
- [Hands-On Labs & Tasks](#-hands-on-labs--tasks)
- [Prompt Engineering](#-prompt-engineering)
- [Azure AI Services Reference](#-azure-ai-services-reference)
- [Responsible AI Principles](#-responsible-ai-principles)

---

## 🛠 Prerequisites

| Requirement | Details |
|---|---|
| **Azure Account** | Active subscription — Free Tier recommended |
| **Free Tier Credits** | $200 USD for 30 days (requires Credit/Debit card for verification) |
| **IDE** | VS Code |

---

## 📚 Course Sections

| # | Section |
|---|---|
| 1 | Planning an Azure AI Solution |
| 2 | Implement GenAI Solutions |
| 3 | Implement Computer Vision Solutions |
| 4 | Implement NLP Solutions |
| 5 | Implement Knowledge Mining and Information Extraction Solutions |

---

## 🔑 Key Terms

| Term | Full Form | Description |
|---|---|---|
| **AI** | Artificial Intelligence | Capability in machines to mimic human-like behaviour |
| **ML** | Machine Learning | Branch of AI — perform tasks without explicit instructions |
| **DL** | Deep Learning | Uses Neural Networks to recognize complex objects (images, sound) |
| **LLM** | Large Language Model | Mathematical model designed to predict the next piece of information |
| **FM** | Foundation Model | Broader category — Text, Image, Code, Video, etc. |
| **GenAI** | Generative AI | Branch of AI focused on creating content (text, image, audio, video) |
| **GPT** | Generative Pre-trained Transformer | Pre-trained model that breaks prompts into tokens and predicts output |

> **LLM vs FM:**
> - ✅ All LLMs are Foundation Models
> - ❌ Not all Foundation Models are LLMs

### LLM Breakdown

```
LLM = Large + Language + Model

  Large    → Billions of parameters, trained on millions of documents
  Language → Uses NLP, processed via vectors and embeddings
  Model    → Variety of models available for different use cases
```

---

## 📘 Section 1 — Planning an Azure AI Solution

### AI / ML / DL Hierarchy

```
Artificial Intelligence
└── Machine Learning
    └── Deep Learning
        └── Generative AI
```

| Type | What it does | Example Use Case |
|---|---|---|
| **ML** | Predicts / Classifies | Fraud detection, Weather forecast |
| **DL** | Extracts from complex data | Computer Vision, OCR on images/videos |
| **GenAI** | Creates new content | Text, Image, Audio, Video generation |

### IaaS vs PaaS vs SaaS

| Model | Example | Description |
|---|---|---|
| **SaaS** | ChatGPT | Ready-to-use AI interface |
| **PaaS** | OpenAI Platform / Azure Foundry | Build apps on top of models |
| **IaaS** | Azure VMs | Raw compute power / infrastructure |

---

### 🔄 ML Model Workflow

```
1. Define Business Use Case
        ↓
2. Prepare Data  (⚠️ ~70% of total effort)
        ↓
3. Select Algorithm
        ↓
4. Build & Train Model
        ↓
5. Evaluate Model
        ↓
6. Deploy Model  →  Endpoint + Auth Key created
        ↓
7. Monitor Model  (adapt to changing data)
```

#### Algorithm Types

| Type | Data | Purpose | Example |
|---|---|---|---|
| **Supervised** | Labelled | Predict future values | Fraud detection |
| **Unsupervised** | Unlabelled | Find patterns | Customer segmentation |
| **Reinforcement** | Reward/Punishment | Learn from actions | Self-driving cars (Tesla) |

#### Evaluation Metrics
`Accuracy` · `Precision` · `Recall` · `F1 Score`

---

### 🤖 Generative AI & GPT

**ChatGPT** was launched publicly in late 2022, but OpenAI began working on GPT models in 2017, inspired by the landmark Google Research paper:

> *"Attention Is All You Need"* (2017) — introduced the Transformer architecture

**Notable Models by Provider:**

| Provider | Model | Capability |
|---|---|---|
| OpenAI | GPT-4.1, GPT-5 | Text |
| OpenAI | DALL-E | Image Generation |
| OpenAI | Codex | Code Generation |
| Google | Gemini | Multimodal |
| Anthropic | Claude Opus | Text / Reasoning |

#### How GPT Works
1. User sends a prompt
2. GPT breaks it into **tokens**
3. Transformer processes tokens
4. Model predicts next word using **probability scores**
5. Response is returned

---

### 🖼 Multi-Modal LLMs

A **multimodal LLM** accepts multiple input types but typically returns text output:

```
Input  →  Text | Image | Audio | Video | PDF
                        ↓
                   LLM Model
                        ↓
Output →  Text
```

---

### ☁️ Azure Management Hierarchy

```
Root Management Group
└── Management Groups  (e.g. US, UK, India, Australia)
    └── Subscriptions  (e.g. Dev, QA, Prod, HR)
        └── Resource Groups
            └── Resources  (VMs, DBs, Storage etc.)
```

> **Least-Privilege Principle** — grant only the permissions required, nothing more.

---

## 📗 Section 2 — Implement GenAI Solutions

### Azure OpenAI vs Microsoft Foundry

| Feature | OpenAI Platform | Microsoft Foundry (Azure AI Foundry) |
|---|---|---|
| Models | GPT models only | GPT, Claude, Llama, DeepSeek + more |
| Playgrounds | Chat | Chat, Image, Audio, Video |
| Payment | Pre-paid credits | Azure Subscription (monthly invoice) |
| Cognitive Services | ❌ | ✅ Vision, Speech, NLP, Video Indexer |
| Flexibility | Limited | High |

**Azure AI Foundry** is a unified platform to streamline development and deployment of AI-based applications.

### Model Parameters

| Parameter | Description |
|---|---|
| **Temperature** | Controls randomness. `0` = consistent/predictable. `1` = creative/varied |
| **Top P** | Alternative to Temperature. Limits token selection to top P% probability |
| **Max Tokens** | Sets the maximum length of the model's response |

> ⚠️ Best practice: Tweak **either** Temperature **or** Top P — not both simultaneously.

### System Prompts

System prompts set the **tone, persona, and constraints** for the model before any user interaction.

```
Default system message: "You are an AI system that helps people find information."
```

You can override this to create specialized assistants — travel bots, DevOps assistants, code reviewers, etc.

---

## 🧪 Hands-On Labs & Tasks

### ✅ Task 1 — Create an Azure Free Tier Account

**Subscription types:**
- **Pay-as-you-go** — Invoice generated after month end
- **Free Tier** — $200 USD credits for 30 days

**Verification:**
1. You'll receive a confirmation email with credit expiry date
2. An **Upgrade** button appears on the portal homepage (Free Tier only)

---

### ✅ Task 2 — Create a Microsoft Foundry Resource

1. Select your Subscription
2. Create a new Resource Group (e.g. `ajit-rg`)
3. Give the resource a name (e.g. `ajitdemofoundry`)
4. Region → **East US 2**
5. Keep remaining options as default
6. Click **Review + Create**

> A Foundry resource and project will be created together. Open the resource and click on the portal to proceed.

---

### ✅ Task 3 — Deploy a GPT-4.1-mini Model

1. Go to Microsoft Foundry Portal → `https://ai.azure.com/foundryProject/overview`
2. Navigate to **Model Catalog** → select `gpt-4.1-mini`
3. Click **"Use this Model"**
4. Deployment type → **Global Standard** (keep rest as default)
5. Click **Deploy**
6. Verify under **Models + Endpoints** section

---

### ✅ Task 4 — User Prompt & System Prompt in OpenAI Playground

**System Message:**
```
Act as Tony Stark from the Avengers movie. Use his persona and the way he interacts.
```

**User Prompt:**
```
What is the difference between the OpenAI GPT and Anthropic Claude's model implementation?
```

---

### ✅ Task 5 — Azure AI Foundry Playground

**Prompt:**
```
I have to create a learning path for coding with Python. This needs to start from the basics.
The main aim of the learning path is to be able to develop Python code that can interact
with Large Language Models. Generate a learning path, clearly breaking it down into modules.
```

---

### ✅ Task 6 — Experimenting with Model Parameters

**Prompt:**
```
Tell me a short story about a cat who wants to learn to code
```
> Try this prompt with different Temperature and Top P values and observe how the responses change.

---

### ✅ Task 7 — System Prompt for LinkedIn Post Review

**System Prompt:**
```
Your role is to review my LinkedIn posts and provide constructive feedback to make them more
impactful, professional, and engaging for my target audience, which consists mainly of students
and professionals preparing for cloud and AI certifications. When reviewing a post, please:
- Identify any unclear or awkward sentences and suggest clearer alternatives.
- Check grammar, spelling, and tone for professionalism and inspiration.
- Ensure the post is engaging and encourages interaction.
- Make sure the post stays authentic and aligned with my voice: approachable, professional, and motivational.
```

---

### ✅ Task 8 — Image Generation via Playground

> ⚠️ Use `gpt-image-1.5` model (not a text LLM). Deploy it the same way as `gpt-4.1-mini`.

**Prompt:**
```
Cats playing to the beat of the drums
```

---

### ✅ Task 9 — REST API Call to GPT-4.1-mini

```bash
curl -X POST "https://ajitdemofoundry.cognitiveservices.azure.com/openai/deployments/gpt-4.1-mini/chat/completions?api-version=2025-01-01-preview" \
    -H "Content-Type: application/json" \
    -H "Authorization: Bearer <<api-key>>" \
    -d '{
        "messages": [
            {
                "role": "user",
                "content": "I am going to Paris, what should I see?"
            }
        ],
        "max_completion_tokens": 13107,
        "temperature": 1,
        "top_p": 1,
        "frequency_penalty": 0,
        "presence_penalty": 0,
        "model": "gpt-4.1-mini"
    }'
```

> 📎 Reference: [OpenAI API Docs](https://developers.openai.com/api/docs)

---

### ✅ Task 10 — Python: Chat Completion API

```python
from openai import AzureOpenAI

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

response = client.chat.completions.create(
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Please give me an introduction onto Large Language Models"}
    ],
    max_tokens=16384,
    temperature=1.0,
    top_p=1.0,
    model="gpt-4.1-mini",
)

print(response.choices[0].message.content)
```

---

### ✅ Task 11 — Python: Using System Messages as Context

```python
from openai import AzureOpenAI

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

response = client.chat.completions.create(
    messages=[
        {"role": "system", "content": "You are an assistant helping students to learn about Large Language Models."},
        {"role": "user", "content": "What is the temperature setting"}
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

print(response.choices[0].message.content)
```

---

### ✅ Task 12 — Python: Full Response in JSON Format

```python
from openai import AzureOpenAI
import json

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

response = client.chat.completions.create(
    messages=[
        {"role": "system", "content": "You are an assistant helping students to learn about Large Language Models."},
        {"role": "user", "content": "What is the temperature setting"}
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

dumped_response = response.model_dump()
print(json.dumps(dumped_response, indent=2))
```

---

### ✅ Task 13 — Python: Multimodal Capabilities with Image Input

```python
from openai import AzureOpenAI
import base64

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

with open("img1.png", "rb") as image_file:
    image_details = base64.b64encode(image_file.read()).decode("utf-8")

response = client.chat.completions.create(
    messages=[
        {"role": "system", "content": "You are an assistant who helps to describe images."},
        {
            "role": "user",
            "content": [
                {"type": "text", "text": "Give me a description of what the image is trying to explain"},
                {"type": "image_url", "image_url": {"url": f"data:image/png;base64,{image_details}"}}
            ]
        }
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

print(response.choices[0].message.content)
```

---

### ✅ Task 14 — Python: Ask Model to Explain Code

```python
from openai import AzureOpenAI

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

with open("code.py", "r", encoding="utf-8") as code_file:
    code_content = code_file.read()

response = client.chat.completions.create(
    messages=[
        {"role": "system", "content": "You are an assistant who helps teach how to code."},
        {"role": "user", "content": f"Explain clearly what the following Python code does:\n\n{code_content}"}
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

print(response.choices[0].message.content)
```

---

### ✅ Task 15 — REST API: Generate Image with GPT-Image-1.5

```bash
curl.exe -X POST "https://ajit-mq724wa6-swedencentral.cognitiveservices.azure.com/openai/deployments/gpt-image-1.5/images/generations?api-version=2024-02-01" `
  -H "Content-Type: application/json" `
  -H "api-key: <<api-key-value>>" `
  -d '{
     "prompt": "A photograph of a red fox in an autumn forest",
     "size": "1024x1024",
     "quality": "medium",
     "output_compression": 100,
     "output_format": "png",
     "n": 1
    }' | jq -r '.data[0].b64_json' | base64 --decode > generated_image.png
```

---

### ✅ Task 16 — Python: Generate an Image using GPT-Image-1.5

```python
from openai import AzureOpenAI
import base64

client = AzureOpenAI(
    api_version="2024-02-01",
    azure_endpoint="https://ajit-mq724wa6-swedencentral.cognitiveservices.azure.com/",
    api_key="",
)

response = client.images.generate(
    model="gpt-image-1.5",
    prompt="A futuristic cat dwelling in the sunset, highly detailed, digital art",
    n=1,
    size="1024x1024",
    quality="medium"
)

image_b64 = response.data[0].b64_json
image_bytes = base64.b64decode(image_b64)

with open("img2.png", "wb") as handler:
    handler.write(image_bytes)

print("Finished generating the image")
```

---

## 🧠 Prompt Engineering

> The skill of designing clear, structured prompts to get better, more useful responses from AI models.

### 1. Zero-Shot Prompting
Ask a question directly — no examples provided.

```
Prompt: How do I find the LCM of a number?
```

### 2. Few-Shot Prompting
Provide examples to guide the model's response format.

```
Translate the following English sentences to Spanish:

"Good morning" → "Buen día"
"I am really pleased with the course" → "Estoy muy contento con el curso"
"I hope you would be able to provide online training as well" → ?
```

### 3. Chain-of-Thought Prompting
Guide the model to reason step-by-step for complex problems.

```
Seven years ago, Alan's age was three times John's age.
Three years since, Alan's age is two times John's age.
What are Alan's and John's current ages? Solve step by step.
```

### 4. Role-Based Prompting
Assign the model a specific expert persona.

```
You are a Solution Architect in Azure. You need to build a highly scalable and
highly available e-commerce application. Design the architecture.
```

---

## 🔧 Azure AI Services Reference

<details>
<summary><strong>👁 Azure AI Vision Service</strong></summary>

| Feature | Description |
|---|---|
| **OCR** | Extract printed and handwritten text from photos and documents |
| **Image Analysis** | Extract visual features — objects, faces, etc. |
| **Face** | Detect, recognize, and analyze human faces in images |

</details>

<details>
<summary><strong>💬 Azure AI Language Service</strong></summary>

| Feature | Description |
|---|---|
| **Named Entity Recognition** | Identify and categorize entities in text |
| **Language Detection** | Detect a wide range of languages from text |
| **Sentiment Analysis** | Identify positive or negative sentiment in text |
| **Key Phrase Extraction** | Extract main concepts from unstructured text |

</details>

<details>
<summary><strong>🎙 Azure Speech Service</strong></summary>

- Speech → Text
- Text → Speech (Synthesis)
- Speech Translation

</details>

<details>
<summary><strong>🌐 Azure Translator Service</strong></summary>

- Translate text between languages
- Create tailored/custom translation models
- Auto-detect source language

</details>

<details>
<summary><strong>🎥 Azure AI Video Indexer</strong></summary>

Built on top of: **Translator + Vision + Speech**

- Extract insights from video and audio content
- Use cases: Deep search, Content creation

</details>

<details>
<summary><strong>📄 Azure Document Intelligence</strong></summary>

- Extract data from documents and forms at scale
- Pre-built models for Financial and Legal services
- Supports custom model training

</details>

---

## 🛡 Responsible AI Principles

Microsoft's core principles for building AI responsibly:

| Principle | Description |
|---|---|
| **Fairness** | AI systems must treat all people fairly regardless of gender, ethnicity, or other factors |
| **Privacy & Security** | Protect PII (Personally Identifiable Information); mask sensitive data in training sets |
| **Inclusiveness** | AI should empower everyone — not just a specific group or domain |
| **Transparency** | Clearly communicate what the AI can and cannot do; display appropriate disclaimers |
| **Accountability** | Organizations building AI models are accountable for their behaviour and outcomes |

> ⚠️ AI models can **hallucinate** and produce **biased results**. Never trust AI output 100% without verification.

---

## 📎 Useful Links

| Resource | URL |
|---|---|
| Azure AI Engineer Certification | [learn.microsoft.com](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-engineer/) |
| OpenAI API Docs | [developers.openai.com](https://developers.openai.com/api/docs) |
| Microsoft Foundry Portal | [ai.azure.com](https://ai.azure.com) |

---

*Course notes structured for AI-102 exam preparation. Always refer to official Microsoft documentation for the latest updates.*
