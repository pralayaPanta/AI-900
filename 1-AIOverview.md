- [Topic: Fundamental of AI Concepts](#topic-fundamental-of-ai-concepts)
    - [Key workloads](#key-workloads)
    - [Dataset](#dataset)
  - [Label vs Feature](#label-vs-feature)
      - [Machine learning in MS Azure](#machine-learning-in-ms-azure)
        - [Computer vision models](#computer-vision-models)
  - [Azure Cognitive Service](#azure-cognitive-service)
        - [Computer vision services in MS Azure](#computer-vision-services-in-ms-azure)
    - [Natural Language Processing NPL](#natural-language-processing-npl)
    - [Knowledge minning in Azure](#knowledge-minning-in-azure)
    - [Conversational AI](#conversational-ai)
    - [Generative AI in Azure](#generative-ai-in-azure)
    - [Azure AI Content Moderator](#azure-ai-content-moderator)
    - [Challenge or Risk of AI](#challenge-or-risk-of-ai)
    - [Responsible AI - Microsoft AI Principles](#responsible-ai---microsoft-ai-principles)

# Topic: Fundamental of AI Concepts
- **Artificial Intellgence** - machines that performs jobs that mimic human behaviour.
- **Machine learning -** foundation of AI, way of teaching computer model to make predictions
    - Machines learn from data, capturing the relationship between data
- **Deep Learning** - machine that have artificial neural network inspired by the human brain.

### Key workloads
- **Computer vision -** interpretting the world through cameras, video, and images

- **Natural language processing** - interpretting wrriten or spoken language and its response
      - determining whether a review is  positive or negative 
      - sentiment analysis
- **Document intelligence** - managing processing and using high volumes of data forms and documents
- **Knowledge mining** - extract information unstructured data to create knowledge store
- **Generative AI**- create original content in natural language, image, code and more

### Dataset
  - logical grouping of units of data that are closely related or share same data structure
  - examples
      - MNIST database
      - COCO dataset

## Label vs Feature
  - Identifying raw data and adding one or more meaningful and informative labes or context that can be learned by ML.
  - Labeling is the process of tagging data with known values.
  - Feature = Input. Label = Output.


#### Machine learning in MS Azure
- **Automated machine learning:** quickly create an effective machine learning model from data.
- **Azure Machine Learning designer**:no-code development of machine learning solutions.
- **Data metric visualization:** analyze and optimize your experiments with visualization.
- **Notebooks:** write and run your own code in managed Jupyter Notebook servers 

##### Computer vision models
- image classification - classify images based on contents
- object detection - classify individual objects within an image and and identify their location with a bounding box.
    - information 
        - bounding box
        - class name
        - probability score
- semantic segmentation - classify individual pixels
    - provides the ability to classify individual pixels in an image depending on the object that they represent.
- image analysis - model to extract information from images
- face detection and recognition - locates human faces in an image
- optioncal character recognition OCR - detect and read text in images

## Azure Cognitive Service
  - comprehensive family of AI services and cognitive APIs to help build intelligent apps
  - pretained models built with breakthrough AI research
  - unbrell AI service that enables customers to access multiple AI servies with an API key and API endpoint
  - Decision
      - anomaly detector
      - content moderator
      - personaliser
  - Language
      - langugage understanding
      - QnA Maker
      - Text analytics
      - Translator
  - Speech
      - speech to text
      - text to speech
      - speech translation
      - speaker recognition
  - Vision
      - computer vision
      - custom vision
  
##### Computer vision services in MS Azure
- Image Analysis
      - capabilities for analyzing images and video, and extracting descriptions, tags, objects, and text.
- Face recognition
      - capabilities that enable you to build face detection and facial recognition solutions.
- Optical character recognition OCR
      - capabilities for extracting printed or handwritten text from images, enabling access to a digital version of the scanned text.

### Natural Language Processing NPL
- analyze and interpret texts
- interpret and translate spoken or written language
- synthesize speech responses
- interpret commands and determine appropriate actions
- Azure offerings
    - text analytics
    - translator
    - speech
    - language understaind LUIS
- NPL services in Azure
    - Azure AI Language
    - Azure AI Speech
    - Azure Speech Studio featuers AI Language and AI Speech in azure.
  
### Knowledge minning in Azure
- **Azure AI Document Intelligence** - data collection from scanned documents
- **Azire AI Search** - search solution that has tools for building indexes

### Conversational AI
- participate in converstaions with human
- QnA maker
- Azure Bot service
  - chatbots
  - voice assistants
  - interactive voice recognition systems IVRS

### Generative AI in Azure
- Azure OpenAI Service - solution for deploying customising, and hosting generative AI models.

### Azure AI Content Moderator 
- an Azure AI Services service that is used to check text, image, and video content for material that is potentially offensive.

### Challenge or Risk of AI
- Bias can affect results
- Erros may cause harm
- Data could be exposed
- Soluton may not work for everyone
- Users must trust complex system
- Who's liable for AI driven decisions

### Responsible AI - Microsoft AI Principles
- Fairness
    - Example: The system must not discriminate based on gender and race
- Reliability and safety
    - AI software must be rigorous tested
- Privacy and security 
    - Example: Personal data must be visible only to approved
- Inclusiveness
- Transparency
    - AI system should be understandable
    - Example: When you design an AI system to assess whether loans should be approved, the factors used to make the decision should be explainable.
- Accountability
    - people should be accountable for AI
  
  [Human AI interaction AI DEMOS](https://www.microsoft.com/en-us/haxtoolkit/library/)