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


# ☁️ Azure AI Engineer Associate — AI-102 (Day 3 & 4)

> **Designing and Implementing an Azure AI Solution**
> 📄 [Official Certification Page](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-engineer/)

![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![AI-102](https://img.shields.io/badge/AI--102-Certification-blue?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Computer Vision](https://img.shields.io/badge/Computer_Vision-FF6F00?style=for-the-badge&logo=opencv&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-4B8BBE?style=for-the-badge)

> 📌 This continues from **Day 1–2** notes — covering Fine-Tuning, RAG, Content Safety, Computer Vision, and NLP solutions.

---

## 📋 Table of Contents

- [Fine-Tuning Azure OpenAI Models](#-fine-tuning-azure-openai-models)
- [RAG — Retrieval Augmented Generation](#-rag--retrieval-augmented-generation)
- [Azure AI Content Safety](#-azure-ai-content-safety)
- [Section 3 — Computer Vision Solutions](#-section-3--computer-vision-solutions)
- [Section 4 — NLP Solutions](#-section-4--nlp-solutions)
- [Hands-On Labs & Tasks Index](#-hands-on-labs--tasks-index)

---

## 🎯 Fine-Tuning Azure OpenAI Models

### What is Fine-Tuning?

LLMs are pre-trained on **large, broad datasets** using significant compute power. While powerful, they're general-purpose by default.

> If a company wants the model to **always** respond in a specific format, tone, or style, sending detailed instructions via a system prompt on *every request* adds complexity and token cost.

**Fine-tuning** solves this by training the model further on your **own custom dataset**, so it inherently follows your desired format/tone — without repeating instructions each time.

| Aspect | Description |
|---|---|
| **Base Model** | Already trained on broad data |
| **Fine-Tuning** | Further trains the model on custom/domain-specific data |
| **Benefit** | Reduces prompt complexity & token usage per request |
| **Cost** | Requires significant compute power + time |

> 📎 Reference: [Fine-tuning in Azure AI Foundry](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/fine-tuning?tabs=oai-sdk&pivots=programming-language-studio)

---

## 🔍 RAG — Retrieval Augmented Generation

### The Problem

Asking a deployed LLM something organization-specific — e.g., *"What is the leave policy at my organization?"* — can lead to **hallucination**, since the model has no knowledge of your private data.

### The Solution

```
Custom Data (HR_Policy.pdf)
        ↓
  Azure Blob Storage   (object-level storage, like an S3 bucket)
        ↓
  Azure AI Search       (indexes & crawls the data → builds vector DB)
        ↓
   LLM Model            (uses retrieved context to answer accurately)
```

### How It Works — Embeddings Pipeline

```
Input Prompt → Words → Tokens → Embeddings (numerical vectors) → Vector DB → Search & Retrieve
```

> ✅ Supports ingestion of **thousands of documents** — Azure AI Search builds an index on top for fast retrieval.

> 📎 Reference: [Azure Blob Storage Introduction](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction)

---

### ✅ Task 17 — RAG Implementation (Portal)

1. Create a **Storage Account** for blob storage
2. In the **Data Storage** section, create a container and upload `HR_Policy.pdf`
3. Create an **Azure AI Search** service
   - Azure AI Search builds a **vector space / vector DB** using embeddings
4. In the **gpt-4.1-mini Chat Playground**, add the AI Search resource as a **data source**
5. Run a query once ingestion is complete

---

### ✅ Task 18 — Python: RAG Model Implementation

```python
from openai import AzureOpenAI

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

rag_params = {
    "data_sources": [
        {
            "type": "azure_search",
            "parameters": {
                "endpoint": "https://rag-search4000.search.windows.net",
                "index_name": "rag-index",
                "authentication": {
                    "type": "api_key",
                    "key": "",
                }
            }
        }
    ],
}

response = client.chat.completions.create(
    messages=[
        {"role": "user", "content": "How are performance appraisals conducted?"}
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini",
    extra_body=rag_params
)

print(response.choices[0].message.content)
```

---

## 🛡 Azure AI Content Safety

Detects and blocks **harmful text and images** — both in user input prompts and model-generated output.

### Key Capabilities

| Feature | Description |
|---|---|
| **Scan & Moderate Text** | Detects harmful text content |
| **Prompt Shields** | Defends against jailbreak attempts, hidden attacks, and cross-domain prompt injection |
| **Image Moderation** | Detects self-harm, violence, racy/explicit images |
| **Fairness Filters** | Detects discrimination, racial slurs, vulgar content targeting groups |
| **Content Filters** | Configurable thresholds for blocking categories |
| **Grounding** | Verifies output against a trusted source (blog, news article, link) |

> 📎 Reference: [Content Safety Blocklists](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/how-to/use-blocklist)

---

### ✅ Task 19 — Create Azure Content Safety Resource

1. **Sign in to Azure Portal**
2. **Create a New Resource** → search for *Azure AI Content Safety* → Create
3. **Configure Details** → Subscription, Resource Group, Region, unique Resource Name
4. **Review + Create** → validate settings → Create
5. **Access Keys and Endpoint** → copy from *Keys and Endpoint* section

> ✅ Result: Your Content Safety resource is ready for text and image moderation APIs.

---

### ✅ Task 20 — Python: Detect Harmful Text

```python
from azure.ai.contentsafety import ContentSafetyClient
from azure.core.credentials import AzureKeyCredential
from azure.ai.contentsafety.models import AnalyzeTextOptions

endpoint = "https://contentsafety4000.cognitiveservices.azure.com/"
key = ""

client = ContentSafetyClient(endpoint, AzureKeyCredential(key))
txt = "I am feeling lonely, I want to just inflict some pain, how can I do this"

request = AnalyzeTextOptions(text=txt)
response = client.analyze_text(request)

print(response)
```

> ⚠️ *Note: This sample text is used purely to demonstrate the Content Safety API's self-harm detection category — not as a real prompt.*

---

### ✅ Task 21 — Python: Detect Harmful Images

```python
from azure.ai.contentsafety import ContentSafetyClient
from azure.core.credentials import AzureKeyCredential
from azure.ai.contentsafety.models import AnalyzeImageOptions, ImageData

endpoint = "https://contentsafety4000.cognitiveservices.azure.com/"
key = ""

client = ContentSafetyClient(endpoint, AzureKeyCredential(key))

with open("img1.jpg", "rb") as image_file:
    request = AnalyzeImageOptions(image=ImageData(content=image_file.read()))

response = client.analyze_image(request)
print(response)
```

---

## 👁 Section 3 — Computer Vision Solutions

> **Computer Vision** is the field of AI that enables computer systems to **see and understand images and videos**, extracting useful information from them.

### Core Capabilities

| Capability | Description |
|---|---|
| **Image Tagging** | Auto-generates tags describing the contents of an uploaded image |
| **Caption Generation** | Generates a natural-language caption for an image |
| **Object Detection** | Draws bounding boxes around detected objects |
| **OCR** | Extracts text from images |

---

### ✅ Task 22 — Create a Computer Vision Resource

1. **Sign in to Azure Portal**
2. **Create a New Resource** → search for *Computer Vision* (part of Azure AI Vision) → Create
3. **Configure** → Subscription, Resource Group, Region, Pricing Tier, Resource Name
4. **Review + Create** → validate → Create
5. **Get Keys and Endpoint** → copy API Key and Endpoint URL

> ✅ Result: Your Azure Computer Vision resource is ready to use.

---

#### 🏷 1. Image Tagging

🔗 Try it in the [Vision Studio Demo](https://portal.vision.cognitive.azure.com/demo/generic-image-tagging)

```python
# LAB -- Python -- Azure AI Vision -- Analyze Image and Extract Tags
from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.core.credentials import AzureKeyCredential
from azure.ai.vision.imageanalysis.models import VisualFeatures
import json

endpoint = "https://ajitvision4000.cognitiveservices.azure.com/"
key = ""

client = ImageAnalysisClient(endpoint=endpoint, credential=AzureKeyCredential(key))

with open("img3.png", "rb") as image_file:
    image_details = image_file.read()

response = client.analyze(
    image_data=image_details,
    visual_features=[VisualFeatures.TAGS]
)

print(json.dumps(response.as_dict(), indent=4))
```

---

#### 📝 2. Generate Captions

🔗 Try it in the [Vision Studio Demo](https://portal.vision.cognitive.azure.com/demo/image-captioning)

```python
# LAB -- Python -- Azure AI Vision -- Generate Caption for an Image
from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.core.credentials import AzureKeyCredential
from azure.ai.vision.imageanalysis.models import VisualFeatures
import json

endpoint = "https://ajitvision4000.cognitiveservices.azure.com/"
key = ""

client = ImageAnalysisClient(endpoint=endpoint, credential=AzureKeyCredential(key))

with open("img3.png", "rb") as image_file:
    image_details = image_file.read()

response = client.analyze(
    image_data=image_details,
    visual_features=[VisualFeatures.TAGS, VisualFeatures.CAPTION]
)

print(json.dumps(response.as_dict(), indent=4))
```

---

#### 📦 3. Object Detection

🔗 Try it in the [Vision Studio Demo](https://portal.vision.cognitive.azure.com/demo/generic-object-detection)

```python
# LAB -- Python -- Azure AI Vision -- Object Detection in an Image
from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.core.credentials import AzureKeyCredential
from azure.ai.vision.imageanalysis.models import VisualFeatures
import json

endpoint = "https://ajitvision4000.cognitiveservices.azure.com/"
key = ""

client = ImageAnalysisClient(endpoint=endpoint, credential=AzureKeyCredential(key))

with open("cereals.jpg", "rb") as image_file:
    image_details = image_file.read()

response = client.analyze(
    image_data=image_details,
    visual_features=[VisualFeatures.OBJECTS]
)

print(json.dumps(response.as_dict(), indent=4))
```

---

#### 🔤 4. OCR — Extract Text from Images

🔗 Try it in the [Vision Studio Demo](https://portal.vision.cognitive.azure.com/demo/extract-text-from-images)

```python
# LAB -- Python -- Azure AI Vision -- Read Text from an Image (OCR)
from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.core.credentials import AzureKeyCredential
from azure.ai.vision.imageanalysis.models import VisualFeatures
import json

endpoint = "https://ajit-demo-vision.cognitiveservices.azure.com/"
key = ""

client = ImageAnalysisClient(endpoint=endpoint, credential=AzureKeyCredential(key))

with open("img4.png", "rb") as image_file:
    image_details = image_file.read()

response = client.analyze(
    image_data=image_details,
    visual_features=[VisualFeatures.READ]
)

for line in response.read.blocks[0].lines:
    print(f"{line.text}")
```

---

### 🙂 Face Service

| Capability | Description |
|---|---|
| **Face Detection** | Detects faces and assigns IDs |
| **Attributes** | Head pose, glasses, mask, occlusion, accessories etc. |
| **Facial Landmarks** | Coordinates — eye tips, forehead, eye corners, etc. |
| **Face Comparison** | Compare faces across images (e.g., Google Photos "group by person") |
| **Facial Recognition** | Identify a collection of faces belonging to specific individuals |
| **Facial Liveness** | Determine whether an input video stream is real or fake |

---

### ✅ Task 23 — Create Face Service & Detect Faces

```python
# LAB -- Python -- Azure AI Vision -- Face Detection in an Image
from azure.core.credentials import AzureKeyCredential
from azure.ai.vision.face import FaceClient
from azure.ai.vision.face.models import *
import json

endpoint = "https://demoface4000.cognitiveservices.azure.com/"
key = ""

client = FaceClient(endpoint=endpoint, credential=AzureKeyCredential(key))

features_to_client = [
    FaceAttributeTypeDetection01.HEAD_POSE,
    FaceAttributeTypeDetection01.OCCLUSION,
    FaceAttributeTypeDetection01.ACCESSORIES
]

with open("img3.jpg", mode="rb") as image_data:
    response = client.detect(
        image_content=image_data.read(),
        detection_model=FaceDetectionModel.DETECTION01,
        recognition_model=FaceRecognitionModel.RECOGNITION01,
        return_face_id=False,
        return_face_attributes=features_to_client
    )

print(json.dumps(response[0].as_dict(), indent=4))
```

---

### 🧩 Custom Vision

Allows you to build your **own custom computer vision models** for:
- **Image Classification**
- **Object Detection**

> **Example workflow:** Upload 10–12 cat images and 10–12 dog images to train the model. Then upload a new dog image → the model predicts e.g. `70% dog, 30% cat`.

#### Understanding Training Results — Confusion Matrix

| Term | Meaning (Spam Detection Example) |
|---|---|
| **True Positive** | Model predicts *spam*, actual is *spam* ✅ |
| **False Positive** | Model predicts *spam*, actual is *non-spam* ❌ |
| **True Negative** | Model predicts *non-spam*, actual is *non-spam* ✅ |
| **False Negative** | Model predicts *non-spam*, actual is *spam* ❌ |

> Metrics derived from this matrix: `Accuracy`, `Precision`, `Recall`, `F1 Score`

```python
# LAB -- Python -- Azure AI Vision -- Image Classification with Custom Vision
from msrest.authentication import ApiKeyCredentials
from azure.cognitiveservices.vision.customvision.prediction import CustomVisionPredictionClient

endpoint = "https://democustomvision4000-prediction.cognitiveservices.azure.com/"
key = ""

credentials = ApiKeyCredentials(in_headers={"Prediction-key": key})
prediction_client = CustomVisionPredictionClient(endpoint=endpoint, credentials=credentials)

image_data = open("img5.png", mode="rb").read()
projectid = "93537d36-1a5d-49f4-8444-03f62fd4a7bd"
model_name = "Iteration1"

response = prediction_client.classify_image(projectid, model_name, image_data)

for prediction in response.predictions:
    print(prediction)
```

---

### 🎥 Azure AI Video Indexer

Built on top of **3 services**: `Vision + Translator + Face`

| Capability | Description |
|---|---|
| Analyze audio + video content | Combined multimedia analysis |
| Detect & group faces | Across an entire video |
| Identify celebrities | Actors, public figures, etc. |
| Extract media info | Including OCR on video frames |
| Content Moderation | Flag inappropriate content |
| Language Understanding | Detect spoken language |
| Closed Captions | Generate in multiple formats |
| Noise Reduction | Clean up audio |

---

### ✅ Task 24 — Create Azure AI Video Indexer Service

🔗 [Video Indexer Portal](https://www.videoindexer.ai/account/login)

1. Upload a video → the service indexes it and extracts **insights**
2. Embed the service into your apps using **widgets**

#### Embeddable Widgets

| Widget | Purpose |
|---|---|
| **Insights Widget** | Display extracted insights |
| **Player Widget** | Embed video playback |
| **Editor Widget** | Edit/review insights |

> 📎 References:
> - [Embed Widgets](https://learn.microsoft.com/en-us/azure/azure-video-indexer/video-indexer-embed-widgets)
> - [Customize Brands Model](https://learn.microsoft.com/en-us/azure/azure-video-indexer/customize-brands-model-how-to?tabs=customizewebportal)

---

## 🗣 Section 4 — NLP Solutions

### Azure AI Language Service

Azure provides **predefined AI models** for common NLP tasks, with options to build **custom versions**.

| Feature | Description |
|---|---|
| **Named Entity Recognition** | Identify entities within text |
| **Detect Language** | Identify the underlying language of input text |
| **Sentiment Analysis** | Classify text as negative, positive, or neutral |
| **Summarization** | Condense large documents (e.g., a 20-page PDF → 1-2 pages) |

> 💡 All features can be tested via the **Playground** in Microsoft Foundry.

---

### ✅ Task 25 — Create Language Resource in Azure Portal

### ✅ Task 26 — Python: Detect Language

```python
from azure.ai.textanalytics import TextAnalyticsClient
from azure.core.credentials import AzureKeyCredential

endpoint = "https://language4000.cognitiveservices.azure.com/"
key = ""

client = TextAnalyticsClient(endpoint=endpoint, credential=AzureKeyCredential(key))

documents = [
    "Me gusta aprender nuevos idiomas.",
    "Comment allez-vous ce matin ?"
]

response = client.detect_language(documents=documents)
print(response)
```

---

### 🌐 Azure AI Translator Service

- Translate text from one language to another
- Supports a wide range of languages
- Test via the **Playground** in Microsoft Foundry

---

### ✅ Task 27 — Create an Azure AI Translator Resource

> Note down the **Endpoint** and **Key** for use in your application.

### ✅ Task 28 — Python: Translate Text

```python
from azure.ai.translation.text import TextTranslationClient, TranslatorCredential
from azure.ai.translation.text.models import InputTextItem

endpoint = "https://api.cognitive.microsofttranslator.com/"
key = ""
region = "eastus"

credential = TranslatorCredential(key, region)
client = TextTranslationClient(endpoint=endpoint, credential=credential)

source_language = "en"
target_language = ["it"]

input_txt = "I like to learn new languages"
documents = [InputTextItem(text=input_txt)]

response = client.translate(content=documents, to=target_language, from_parameter=source_language)

print(f"Translated Text : {response[0].translations}")
```

---

### 🎙 Azure Speech Service

| Capability | Description |
|---|---|
| **Speech-to-Text** | Transcribe spoken audio into text |
| **Text-to-Speech** | Generate natural-sounding speech from text |
| **Caption Generation** | Auto-generate captions |
| **Audio Creation** | Produce voice audio content |
| **Real-Time Transcription** | Live transcription |
| **Voice Assistants** | Build conversational voice agents |

> 💡 Test capabilities directly in the **Speech Playground**.

---

### ✅ Task 29 — Create Speech Resource in Azure

### ✅ Task 30 — Python: Text-to-Speech using Speech SDK

```python
import azure.cognitiveservices.speech as speechsdk

endpoint = "https://aiservice4000.cognitiveservices.azure.com/"
key = ""

config = speechsdk.SpeechConfig(subscription=key, endpoint=endpoint)
config.speech_synthesis_voice_name = "en-US-SteffanMultilingualNeural"

input_txt = (
    "Machine learning is a branch of artificial intelligence (AI) that focuses on "
    "building systems that can learn from data and improve over time without being explicitly "
    "programmed. Traditional computer programs follow explicit rules defined by humans: the "
    "programmer writes code that specifies exactly what the computer should do in every situation. "
    "In contrast, a machine learning system identifies patterns and relationships in data, and then "
    "uses those patterns to make predictions or decisions when "
)

output_file = "speech01.wav"
audio_output = speechsdk.audio.AudioConfig(filename=output_file)

speech_generator = speechsdk.SpeechSynthesizer(speech_config=config, audio_config=audio_output)

result = speech_generator.speak_text_async(input_txt).get()
if result.reason == speechsdk.ResultReason.SynthesizingAudioCompleted:
    print("Successfully generated speech")
else:
    print("Generating speech failed")
```

> 📎 **SSML** (Speech Synthesis Markup Language) allows fine control over speech output.
> Reference: [SSML Documentation](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/speech-synthesis-markup)

---

### 💬 Conversational Language Understanding (CLU)

A feature of the **Azure AI Language Service** for building **end-to-end conversational apps** (chatbots).

#### How It Works

```
User Query → Intent Detection + Entity Extraction → Bot Response
```

**Example — Hotel Booking Bot:**

| Query | Intent | Entities |
|---|---|---|
| "How many single rooms are available on 15th June?" | `CheckAvailability` | `RoomType: single`, `CheckInDate: 15th June` |
| "Is this room available from this date to that date?" | `BookRoom` | `RoomType`, `CheckInDate`, `CheckOutDate` |

---

#### 🧪 Lab — Adding Intents

| Intent Name | Description |
|---|---|
| `BookRoom` | User wants to book a room |
| `CancelBooking` | User wants to cancel an existing booking |
| `ModifyBooking` | User wants to change an existing booking |
| `CheckAvailability` | User wants to know if rooms are available |
| `AskAmenities` | User asks about hotel facilities (e.g., pool, wifi) |
| `CheckInTime` | User asks about check-in or check-out times |
| `Greet` | User greets the assistant |

---

#### 🧪 Lab — Adding Entities

| Entity Name | Example Values |
|---|---|
| `RoomType` | single, double, suite, deluxe |
| `CheckInDate` | July 12th, tomorrow, next Monday |
| `CheckOutDate` | July 15th, Friday, in two days |
| `GuestCount` | 1 guest, 2 adults, family of 4 |

---

#### 🧪 Lab — Adding Utterances

<details>
<summary><strong>📌 Click to expand sample utterances per intent</strong></summary>

**Intent: BookRoom**
- "I want to book a double room from July 12th to July 15th for 2 adults."
- "Can you reserve a suite for me tomorrow night?"

**Intent: CancelBooking**
- "I need to cancel my reservation with booking number ABC123."
- "Can you cancel my room for July 15th?"

**Intent: ModifyBooking**
- "I want to change my check-in date to July 13th."
- "Can I upgrade my room to a suite?"

**Intent: CheckAvailability**
- "Do you have rooms available on July 20th?"
- "Are there any double rooms open next weekend?"

**Intent: AskAmenities**
- "Do you have free wifi?"
- "Is there a gym in the hotel?"

**Intent: Greet**
- "Hi"
- "Hello"

</details>

---

### ✅ Task 31 — Python: Consume Conversational Language Model

```python
from azure.ai.language.conversations import ConversationAnalysisClient
from azure.core.credentials import AzureKeyCredential

endpoint = "https://language4000.cognitiveservices.azure.com/"
key = ""

client = ConversationAnalysisClient(endpoint=endpoint, credential=AzureKeyCredential(key))

utterance = "I need a double room for me and my family for the weekend"
project_name = "TrainingProject"
deployment_name = "TrainedDeployment"

response = client.analyze_conversation(
    task={
        "kind": "Conversation",
        "analysisInput": {
            "conversationItem": {
                "participantId": "1",
                "id": "1",
                "modality": "text",
                "language": "en",
                "text": utterance
            },
            "isLoggingEnabled": False
        },
        "parameters": {
            "projectName": project_name,
            "deploymentName": deployment_name
        }
    }
)

print(response)
```

> 📎 Reference: [CLU Best Practices](https://docs.azure.cn/en-us/ai-services/language-service/conversational-language-understanding/concepts/best-practices)

---

### 📚 Custom Question Answering

Built on top of **Conversational Language Understanding** — uses your own data to power a **knowledge base** of FAQs.

| Concept | Description |
|---|---|
| **Knowledge Base** | Common Q&A pairs (FAQs) used by the bot |
| **Azure App Service** | PaaS — managed hosting for your chatbot |
| **VMs** | IaaS — compute, storage, networking, firewall (manual management) |
| **Azure AI Search** | Integrates with Language Service to power Custom QA |

**Workflow:**
```
Azure AI Search → Integrate with Language Service → Enable Custom QA →
Create Project in Language Studio → Build Knowledge Base
```

---

#### 🧪 Lab — Editing the Knowledge Base

| Question | Answer |
|---|---|
| How do I make a hotel reservation? | You can make a reservation directly on our website by selecting your destination, travel dates, and number of guests. |
| What is your cancellation policy? | Our standard cancellation policy allows free cancellation up to 24 hours before check-in. |
| Do you offer airport shuttle service? | Yes, we offer complimentary airport shuttle service for all guests. |
| What amenities are included with my stay? | All guests enjoy free Wi-Fi, complimentary breakfast, access to the fitness center, and use of our swimming pool. |
| How can I modify my existing reservation? | You can modify your reservation by logging into your account on our website and selecting **'Manage Booking'**. |

---

#### API Call via PowerShell

```powershell
Invoke-WebRequest -Uri "https://demolang4000.cognitiveservices.azure.com/language/:query-knowledgebases?projectName=chatbot&api-version=2021-10-01&deploymentName=production" `
  -Method POST `
  -Headers @{ "Ocp-Apim-Subscription-Key" = "<<api-key>>"; "Content-Type" = "application/json" } `
  -Body '{"question":"I need to make a hotel reservation"}'
```

---

## 🧪 Hands-On Labs & Tasks Index

| Task | Description |
|---|---|
| 17 | RAG Implementation — Portal setup (Blob Storage + AI Search) |
| 18 | Python — RAG Model Implementation |
| 19 | Create Azure Content Safety Resource |
| 20 | Python — Detect Harmful Text |
| 21 | Python — Detect Harmful Images |
| 22 | Create Computer Vision Resource (+ Tagging, Captions, Object Detection, OCR) |
| 23 | Create Face Service & Detect Faces |
| 24 | Create Azure AI Video Indexer Service |
| 25 | Create Language Resource in Azure Portal |
| 26 | Python — Detect Language |
| 27 | Create Azure AI Translator Resource |
| 28 | Python — Translate Text |
| 29 | Create Speech Resource in Azure |
| 30 | Python — Text-to-Speech using Speech SDK |
| 31 | Python — Consume Conversational Language Model |

---

*Course notes structured for AI-102 exam preparation. Always refer to official Microsoft documentation for the latest updates.*




