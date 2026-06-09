# Azure_AI-102_8th_June

Azure AI Engineer Associate 

AI-102 (Designing and Implementing an Azure AI Solution)
(https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-engineer/)

5 Sections :

Section 1 : Planning an Azure AI Solutions

Section 2 : Implement GenAI Solutions 

Section 3: Implement Computer Vision Solutions

Section 4 : Implement NLP Solutions 

Section 5 : Implemnet Knowledge Mining and Information Extractions Solutions



( Azure Account (Active subscription)  -- Free tier  +   VS Code (IDE) )

200 USD credits for 30 days ..  (Verficiation -- CRedit/Debit card)



ML, AI, LLM, FM, GPT, Llama, CLaude  --  Key terms used in Course ..


LLM  -- Large Language Models -- NLP  -- System understands Binary (  0 and 1 )

Input -- Hello , how are you ?   ----   Embeddings (Vectord db -- mathematical rep.)  -- output

LLM -- Chatgpt ( Interafec -- OpenAI models)

GPT-5.5 , GPt - 4.1  (Text)

DALL-E  >> Image generation

Codex  -- Code generation


FM  -- Foundation Models  -- Broader category -- Text, Image, Code, Video etc 

(LLM vs FM) --- 


-- all LLMs are Foundation models

-- all FMs are not LLMs


LLM -- large language Models

 Large -- Billions of parameters , millions of docs used in training ...
 Language -- NLP (Use natural language) processed via vectors and embeddings
 Models -- Variety of Models Available ...
 
 
====================================================================================================================================================================================================================================== 
 Section 1 : Planning an Azure AI Solutions


>> Machine Learning 

(Branch of AI  ... Perform Tasks without giving specific instructions ..

 Programming -- Program to detect fraud transactions in Banking  -- (execute program)
 
 Creating ML Models -- ( Data + Algorithm )
 
 Artifical Intelligence   -- capability in machines to mimic human-like behaviour
 
 Make decisions on their own   >>> Intelligent Machines  (AI)
 
 
 Air conditioner ( room temp -- 24 degree , ouside - 40 degree)
 
 Shut-down and start itself ... (AI features)
 Adjust settings as per temp.
 
 
 >> Deep Learning 
 
 >> Where complex objects such pictures, sound etc  -- recognize - Neural Networks 
 
 ML --  ( Banking industry --  Fraud or not , (txn amount -- user - via which method)
 
          (Weather forecast -- Cloudy, Rainy etc)
          
          (Custom Model -- Data + Algo)
          

DL  --  ( Computer vision  --  Extract Text from Images and Videos )

Advt -- CLick a pic  (product  -- search -- amazon buy it)


Azure -- Pre-trained Models  --  SaaS 

IaaS vs PaaS vs SaaS 

ChatGPT  ---  SaaS

Select our choice models  -- Pro (20 Usd per motnth)

OpenAI  Platform   -- PaaS

IaaS  --  (Compute power -- infra)


===================================================================================================================


ML Models  Workflow  --

1. Business Use Case 

Fraud or Not 

(Data + algo)


(Feeding the data  -- 1 year of transcations record --   CSV file  -- columns

Fraud  -- yes or no   (Training data)   


          
2.   Prepare Data   --

(Clean data  -- 70% time goes in this step)

( multiple sources  -- db, s3 bucket, on-prem servers .. different format .. inconsistencies  

    missing values  -- null , average values 


3. Algorithm

Supervised  -- Labelled data   (predicting futuristic values)

Unsupervised    -- Unlabelled data  (patterns)

Reinforcement Learning  -- (Reward and Punishment)

 (( Tesla  -- sensors ()  -- self driving cars  ))


4. Build the model

(Training model  ---    Compute power (GPUs)  ==

OpenAI, Anthropic like  Orgs  spend billions of USD to train/ use computer power of GPUs )


5. Evaluation

(Accuracy - 95% ,   satisfied)

(Evaluation Metrics like Accuracy, Precision, Recall, f1 score etc can be used)


6. Deploy Model

(Once it's deployed .. an endpoint is created .. which can be used to invoke it via authenticated key ...)


7. Monitor Model    

(amazon -- Trending items in electronics 

1. Iphone 16
2. Laptop Asus
3. Boat earpod 


Do you see same order after 6 months  -- No


ML model -- detect  what are recommendation to user

Mobile phone --  Charger + mobile cover 

(GPT - 5.5, 5.4. 5.0)

fixed knowledge cutoff-date 

(Fix bugs --- adapt to changing env)


===================================================================================================================


GenAI  -- Generative AI  

ML -- Predicting something -- yes or not, classification
DL -- Extract something from image, videos

GenAI is a branch of artificial intelligence that is focused around creating content.

GenAI  -- Generate data (text, image,audio, video etc)

Transformers -- Neural Networks  

ChatGPT  -- introduced in late  2022  in public  by OpenAI  

But OpenAI team started working on GPT models in 2017 --  Inspired by 

(A paper was published in 2017  -- by Google Researchers on transformers named   -- " Attention is all you need "


 Google  --  Gemini 

Anthropic  -- Claude opus 


LLM vs FM 

LLM  -- 

>>  a mathematical model  designed to predict the next piece of information ..

>> it will take that text and try to understand or predict the next word in the text.

>> it generates a list of words along with their probability and then it tries to understand

how to give the next word in the sentence in the output text based on the probability.

Chatgpt -- Tech , their own domain

AI - developers -- 

Kiro, Claude Code  --  Coding Assistants

Application -- 

Spec driven developement,  Vibe Coding

requirements - design - test cases - tasks -- implememation -- deployment


Vibe coding -- Prompt --  (simple tasks)

Spec driven Dev = Structured Output -- .md  files generated  -- Complex tasks

===================================================================================================================


Chatgpt -- 2022  (first launched -- 1 million users in few days)

Assisting partner --- 

(Responsible AI)  -- can't trust 100% AI models , hallucination, bias results could be there .. need to follow certain principles


ChatGPT  -- friendly user interface  

input prompt --

output -- 100 words max (tokens)  -- 500 tokens


Azure  -- free tier  (200 USD for 30 days)

Microsoft Foundry  -- OpenAI Platform  


ChatGPT  -- It is just the web interface that allows us to easily query the underlying model, the GPT model.

                  >>   the underlying brains of the entire operation is the underlying GPT model.

===================================================================================================================

GPT  --  Generative Pre-trained Transformer

>> When we send our query in a prompt, the underlying GPT model will actually break our prompt into something known as tokens.

     and then the GPT model will take the underlying tokens, do its magic, and then give us back a response.
     

>> the transformer actually takes in the instructions, breaks it down into tokens and then gives the response back.


>> We have pre-trained GPT in the end is a model that has been pre-trained on a lot of existing data.


>>  it has the ability to predict the next word in the text output.

===================================================================================================================

OpenAI Models --

https://developers.openai.com/api/docs/models


OpenAI Platform  --  You can work with  only GPT models but text, image,audio, video generation models available

>> It works with pre-paid mode (Need to add credits first to make API calls to model) 

Microsoft Foundry  -- List of Model  (Model Catalog -- You can work with GPT, Claude, Llama, Deepseek models)
                                         
                                    (More Flexibility to select your choice of model)  --  (Chat, Image, Audio, Video Playgrounds available too)

                                  >> Cognitive Services  (Vision, Speech, NLP, Video Indexer etc)
                                  
                                    Endpoint  and   KEY  --- Foundry Project
  
(Cost is associated with Azure Subscription -- Invoice generated once month ends)

===================================================================================================================

Multi-Modal LLM --

>>  what exactly are multimodal large language models?


a multimodal LLM can accept text as input.

It can accept images.

It can accept other artifacts like audio files, video files, etc.


Text to Text,   Image to Text,   Audio , PDF to  Text 

Input -- Text, Image, Audio, PDf etc 

LLM model  -- Output  (Text Only)

===================================================================================================================

Task 1  --   Create an Azure Free Tier Account 

Subscription  >> 1. Pay-as-you-go       (Invoice generated after month end -- 1st june (pay for consumption during may1 - may31 )

                           2.  Free tier (200 USD) for 30 days 
                            
      
      To verify :      1. You will receive an  E-mail  -- sub. is active and 18k credits expire on -- 7th july
                             2. You will see (upgrade) button on portal homepage  (in free tier only)
                            

Azure AI Foundry  -- Microsoft Foundry  (new name)

(Platform  Layer  --- OpenAI, Cognitive Services , Azure AI Search etc)


Resource Group  -- A container to put all resources together and isolate from other resource groups ..


Develoepr team -- 5 Devs  (Dev-Sub)

Azure Account  -- Resource Groups

Dev1 - Rg     (VM, 2 DBs, 1 storage account etc)
Dev2 - Rg      (----------------------)


==================================================================================================================


Task 2  --   Create a Microsoft Foundry Resource in Azure

1. Select your Subscription

2. Create a new resource group (ex. -- ajit-rg)

3. Give resource name  --  ajitdemofoundry 

4. Region -- East US 2

5. Rest of the options -- keep default values ..

6. Review + Create ... 

(It will create a Foundry resource + project as well .. once created open foundry resource and click on portal ...)


================================================================================================================

Azure AI Services :
    
    >> Over the years Azure has built their own set of services based on Artificial Intelligence
    
    >> Instead of developers developing these AI services from scratch, they can make use of various services already available .
    
    
    Using these Services , you can infuse AI into your applications ...
    
    
    << Azure AI Vision Service>>
    
    This service allows you to process images.
    
    1. Optical Character Recognition
  >>  This service allows you to extract text from images. You can extract printed and handwritten text from photos and documents.
    
    2. Image Analysis  
  >>  Here you can extract visual features from images such as the objects and faces from within images.
  
    3.  Face  
  >>  Here you can detect, recognize and analyze human faces in images

      
      << Azure AI Language Service >>
      
      This service provides Natural Language Processing features that allows you to understand and analyze text.
      
      >> NLP  -- analyze text
      
      1. Named Entity Recognition
      >> This helps to identify different entities in text and categorize them.
      
      2. Language Detection
      >> This helps to evaluate text and detect a wide range of languages.
      
      3. Sentiment Analysis
      >> Here you can analyze text and identify positive or negative sentiments.
      
      4. Key Phrase Extraction
      >> This can take in your unstructured text and return the main concepts.
         
         
        << Azure Speech Service >>
      
        This service provides various capabilities.
        
       >> Convert Speech to text 
       >> Synthesize text to speech 
       >> Translate Speech 
       
        
        << Azure Translator Service >>
        
        This service provides text translation capabilities
        
        >> Translate text from one language to another
        >> Create tailored translation models
        >> Detect the source text language.
        
        
        << Azure AI Video Indexer >>
        
        Extract insights from videos
        
        >> This service is built on top of existing Azure AI services that includes the Translator service, Azure AI Vision, Speech.
         (Translator + Vision + Speech)
         
         >> This service then extracts insights based on the video and audio content
         
         >> This service can be used in scenarios such as Deep search, Content creation etc.
         
       
       << Azure Document Intelligence >>
       
       Extract data from documents
       
       >> You can feed in your documents and forms onto the service. You can give it massive amounts of data.
       
       >> This service can extract data from the documents based on many pre-built models which include Financial and Legal services.
       
       >> You can also train your own custom models as well.
     
    
 =================================================================================================================                         
 

Task 3  --  Deploy a Gpt-4.1-mini Model from Model Catalog

    1. First, go to Microsoft Foudry Portal, click on it ..
    
    2. It will take you to a new page with URL something like    "https://ai.azure.com/foundryProject/overview......."
    
    3. In model catalog -- select "gpt-4.1-mini" model ..
    
    4. Click on "Use this Model" ...
    
    5. Keep deploymnt type -- Global Standard , rest options as default 
    
    6. Click on Deploy ... Once Deployed successfully, you can check it under "Models + Endpoints" Section ..


=================================================================================================================


AI Safety and Responsibility  :
    
    
>>     Microsoft use principles  --

 1.  Fairness  -- 
 
 >> If you are building an AI system, for example, to generate images, you have to be certain that if the images contain people, 
      then they should not disregard the people based on gender, ethnicity or other factors.
 
 >> System need to treat all people fairly ..
 
 Generate images   ---       HouseKeeping,   CEO etc (should not target just one race, group etc)
 
 
 2. Privacy and Security  --

   PII  --  Personal Identifiable Info 
   
   (Large training  -- Large data  -- (PII) -- mask data ... DEvOps assistant  (API Key -- gpt 4.1)
   
   Assistant  -- which ai model you are using right now ?
   
   
3. Principle of Inclusiveness  --

 It should not just cater to a particular section of people, but it should be there to empower everyone.
 
 Use cases are widespread across all domains ..
 
 
 4. Transparency --
 
 (What AI system can do and what are limitations)
 
 (Chatgpt first time  --- Finace decision (accepting)  
 
 Disclaimer/Warning  --- AI model doesn't generate 100% accurate results, it can make mistakes .. (sources) -- links
 
 
 5.  Accountability --
 
 (Humanoid  -- Robot + AI mind)
 
 dEstructive --
 
 Anthropic creating MOdel  -- accountable for misconduct
 
 (Governance and principles defined by org)
 
 
===============================================================================================================


Section 2 : Implement GenAI Solutions 


Azure OpenAI and Azure AI Foundry

> From a developer perspective, we can make use of the Open API platform.

> If we are using the open API platform, we can create applications.

> We can write an application in Python. We can write an application in dotnet.

> These applications can then make API calls.

> They can send prompts to the OpenAI models and we can get the responses back.

> Now we can also make use of the OpenAI models on the Azure platform.

> Here we get access to the latest models that OpenAI has to offer.


**** Now, what's the benefit of using the open AI models on the Azure platform?

> Well, within Azure we know that as a cloud platform we can build much more.

>  We can build applications on Azure, and these applications can use the various services that Azure has to offer.

> So everything is within that same ecosystem.

Azure AI foundry service -- This is a unified platform that is meant to streamline the development and deployment of AI based applications.

> We can use or create applications that can consume these models within Azure AI foundry.

> We can make use of the playground, experiment with models, and we can develop enterprise ready AI based applications.


===============================================================================================================


Task 4  --  User Prompt and System Prompt in OpenAI Playground 

User Prompt -  


 I am planning on hosting an ecommerce application on Microsoft Azure. The ecommerce application would be built around React.js, Node.js and Python for any background data engineering tasks. The backend data needs to reside in a SQL-based database. I have to build an initial design plan. I want to know the following 
 1. What services I should consider using for hosting the ecommerce application. 
 2. All aspects that I need to consider when it comes to monitoring and security 
 3. What would be the initial costs for hosting my solution Please generate an architecture diagram as well to highlight all services being used.
 
 
 System Message: 
     
     Prompt --  Act as Tony Stark from the Avengers movie. Use his persona and the way he interacts. 
     
    User  Prompt:  What is the difference between the OpenAI GPT and Anthropic Claude's model Implementation



============================================================================================================


Task 5  --   Azure AI Foundry - Using the playground 

Prompt:  I have to create a learning path for coding with Python. This needs to start from the basics. 
                The main aim of the learning path is to be able to develop Python code that can interact with Large Language Models. 
                Generate a learning path, clearing breaking down the path into multiple modules. 

=================================================================================================================

Model parameters  :
    
    >> We have these different model parameters when working with large language models.
    
    >> We have settings such as the temperature setting, the max completion tokens, top P.
    
    Temperature -- controls the randomness of the output that is generated by the AI model.
    
    A setting of zero will make the model give more predictable results. Here the responses will be more consistent in nature.
    If you put the other side of the setting of one here, the model will be more creative in its responses.
    It'll be more varied and diverse when giving responses itself.
    
    
    Top P is just another alternative to the temperature setting.
    
    When you set this setting, it changes the way that the model chooses the next token when it comes onto large language models.
    When it gives you the response, it basically chooses the next token in the sequence or in the sentence and then returns the entire response to you.
    And it has various beaches of probabilities for each of those tokens.

    If you need to change the way that it considers the next token, you can change the top p setting.

    So, for example, if you set the top P has, let's say 0.1, the model will only consider the top ten percentage when it comes on to the next tokens.
    It's a good practice to just tweak either the temperature setting or the top P setting within the Azure
    
    
    Max tokens -- This can set the limit on how long the model response can be.
    
=================================================================================================================


Task 6 -- Azure AI Foundry - Model parameters 

Prompt -- Tell me a short story about a cat who wants to learn to code

(Try to use different parameters on this prompt and see model responses)

==================================================================================================================

System Prompt :
    
    >> It allow us to set the tone and style of the responses coming in from the underlying AI models.
    
    >> They essentially guide the model on how to behave when it processes the input.
    
    >> By default the model instructions are  --  you are an AI system that helps people to find information.
    
    
    If I want the model to be able to review my LinkedIn post.  Follow the next LAB for this ..
    
==================================================================================================================

Task 7 -- Azure AI Foundry - System Prompt

System Prompt -- 

Your role is to review my LinkedIn posts and provide constructive feedback to make them more impactful, professional, and engaging for my target audience, which consists mainly of students and professionals preparing for cloud and AI certifications When reviewing a post, please: Identify any unclear or awkward sentences and suggest clearer alternatives. Check grammar, spelling, and tone for professionalism and inspiration. Ensure the post is engaging and encourages interaction. Make sure the post stays authentic and aligned with my voice: approachable, professional, and motivational.

User Prompt  --

Review the below LinkedIn Post I'm thrilled to announce the launch of our comprehensive 𝘼𝙒𝙎 𝘾𝙚𝙧𝙩𝙞𝙛𝙞𝙚𝙙 𝘼𝙄 𝙋𝙧𝙖𝙘𝙩𝙞𝙩𝙞𝙤𝙣𝙚𝙧 course, designed to prepare you for success in one of technology's most in-demand certification exams. 𝗧𝗿𝗮𝗻𝘀𝗳𝗼𝗿𝗺 𝗬𝗼𝘂𝗿 𝗖𝗮𝗿𝗲𝗲𝗿 𝘄𝗶𝘁𝗵 𝗔𝗜 𝗦𝗸𝗶𝗹𝗹𝘀 This course offers an immersive learning experience that goes beyond exam preparation. You'll gain: 𝟭. 𝗣𝗿𝗮𝗰𝘁𝗶𝗰𝗮𝗹 𝗔𝗜 𝗞𝗻𝗼𝘄𝗹𝗲𝗱𝗴𝗲 : Understand the fundamental concepts of Artificial Intelligence, Machine Learning, and Deep learning that power today's technological innovations 𝟮. 𝗛𝗮𝗻𝗱𝘀-𝗼𝗻 𝗔𝗪𝗦 𝗘𝘅𝗽𝗲𝗿𝗶𝗲𝗻𝗰𝗲 : Work directly with AWS AI services including Amazon SageMaker, Comprehend, Rekognition, and more. 𝟯. 𝗜𝗻𝗱𝘂𝘀𝘁𝗿𝘆-𝗿𝗲𝗹𝗲𝘃𝗮𝗻𝘁 𝗦𝗸𝗶𝗹𝗹𝘀 : Develop capabilities that employers are actively seeking in today's job market  

===================================================================================================================



Task 8  --  Azure AI Foundry - Image Generation -- Using Playground

(To complete this task... LLM won't work .. we need to select a model which can give image as output ..)

(We are going to select gpt-image-1.5 model and deploy the same way as gpt-4.1-mini)

Prompt -- Cats playing to the beat of the drums


===================================================================================================================


Prompt Engineering :

>> skill to design proper and clear prompts  ---- send to model  >> better/structured responnse back

(Context Engineering)  -- System messages  - Instructions / Context

Travel Assistants, DevOps Assistants 


1. Zero Shot Prompting :
    
    (A simple question -- ask from model .. without any context)
    
    Prompt -- How to find the LCM of a no.
    
    Prompt --  I am building a course on teaching Generative AI, what do you suggest as the most suitable title for the course 
    
    
2. Few Shot Prompting :
    
    Prompt :
        
        "Translate the following English sentences to Spanish" 
        
        “Good morning” → “Buen día” 
        
        “I am really pleased with the course” → “Estoy muy contento con el curso" 
        
        “I hope you would be able to provide online training as well” 
    

3. Chain-of-thought Prompting :
    
    Prompt -- 
    
    Seven years ago , Alan's age was three times John's age. 
    Three years since, Alan's age is two times John's age. What is Alan's and John's age?  

(In complex scenario, asking to write a program --- mention the comments, breakpoints -- explain)


4.  Role-base Prompting :
    
    Prompt :
        
        ( You are a Solution Architect in Azure.. You need to build a highly scalable and highly available e-cmmerce application, design it ..)
        

==============================================================================================================


Task 9 -- REST API Call to GPT-4.1-mini Model

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


==========================================================================================================
(important link  -- https://developers.openai.com/api/docs)
==========================================================================================================


Monitoring the Model Usage 

>> application like makemytrip  (travel assistant)

end of day -- requests -- cost associate (usage)


(Microsoft Foundry  -- Deployments  List  -- Click on gpt-4.1   (Metrics)  -- Usage statistics ...)


Next morning -- notification out 200 USD -- 195.45 remaining

Pay-as-you-go  ---    Cost (minimum)


Account -- Org  --  Root Management Group -- techlanders.org

Multiple Management GRoups  --  US, UK, INdia, Australia

Subscriptions  -- Dev, QA, PRod, HR etc

Dev team -- 500 USD budget

(4 developers -- Resource Groups) -- Resources


QA -- 400 USD budget


Hierarachy on which Azure PLatform work :
    
    (top-down inheritance)
    
ROOT Mgmt GRoup  --- Mgmt GRoups  -- Subscriptions  -- RGs --- Resources 

Least-Privilege Principle :
    
===============================================================================================================
    
    
Task 10 -- Python -- Chat Completion API 

from openai import AzureOpenAI

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

response = client.chat.completions.create(
    messages=[
        {
            "role": "system",
            "content": "You are a helpful assistant.",
        },
        {
            "role": "user",
            "content": "Please give me an introduction onto Large Language Models",
        }
    ],
    max_tokens=16384,
    temperature=1.0,
    top_p=1.0,
    model="gpt-4.1-mini",
)

print(response.choices[0].message.content)

==============================================================================================================


Task 11 -- Python -- Using System Messages as Context

from openai import AzureOpenAI

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

response = client.chat.completions.create(
    messages=[
        {
            "role": "system",
            "content": "You are an assistant helping students to learn about Large Language Models.",
        },
        {
            "role": "user",
            "content": "What is the temperature setting",
        }
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

print(response.choices[0].message.content)

===============================================================================================================


Task 12 -- Python -- Getting the Full Response in JSON Format

from openai import AzureOpenAI
import json

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

response = client.chat.completions.create(
    messages=[
        {
            "role": "system",
            "content": "You are an assistant helping students to learn about Large Language Models.",
        },
        {
            "role": "user",
            "content": "What is the temperature setting",
        }
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

dumped_response=response.model_dump()

print(json.dumps(dumped_response,indent=2))


================================================================================================================


Task 13 -- Python -- Multimodal Capabilities with Image Inputs

from openai import AzureOpenAI
import base64

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

with open("img1.png","rb") as image_file:
    image_details=base64.b64encode(image_file.read()).decode("utf-8")

response = client.chat.completions.create(
    messages=[
        {
            "role": "system",
            "content": "You are an assistant who helps to describe images.",
        },
        {
            "role": "user",
            "content": 
            [
                {
            "type":"text",
            "text":"Give me a description of the what the image is trying to explain"
                },
                {
                    "type":"image_url",
                     "image_url" :{
                        "url":f"data:image/png;base64,{image_details}"
                    }
                }
            ]
        }
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

print(response.choices[0].message.content)


==============================================================================================================


Task 14 -- Python -- Asking Model to Explain the Code

from openai import AzureOpenAI
import base64

client = AzureOpenAI(
    api_version="2025-01-01-preview",
    azure_endpoint="https://ajitdemofoundry.cognitiveservices.azure.com/",
    api_key="",
)

with open("code.py","r",encoding="utf-8") as code_file:
    code_content=code_file.read()

response = client.chat.completions.create(
    messages=[
        {
            "role": "system",
            "content": "You are an assistant who helps teach how to code.",
        },
        {
            "role": "user",
            "content":f"Explain clearly what the following Python code does:\n\n{code_content}"     
        }
    ],
    max_tokens=16384,
    temperature=0.7,
    top_p=1.0,
    model="gpt-4.1-mini"
)

print(response.choices[0].message.content)


==============================================================================================================


Task 15 -- Using REST API to Generate an Image with Azure Foundry's GPT-Image-1.5 Model

curl.exe -X POST "https://ajit-mq724wa6-swedencentral.cognitiveservices.azure.com/openai/deployments/gpt-image-1.5/images/generations?api-version=2024-02-01" `
  -H "Content-Type: application/json" `
  -H "api-key: <<api--key--value>>" `
  -d '{
     "prompt" : "A photograph of a red fox in an autumn forest",
     "size" : "1024x1024",
     "quality" : "medium",
     "output_compression" : 100,
     "output_format" : "png",
     "n" : 1
    }' | jq -r '.data[0].b64_json' | base64 --decode > generated_image.png


================================================================================================================


Task 16 -- Python -- Generate an image using GPT-Image-1.5

from openai import AzureOpenAI
import requests
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

with open("img2.png","wb") as handler:
    handler.write(image_bytes)

print("Finished generating the image")


===============================================================================================================
