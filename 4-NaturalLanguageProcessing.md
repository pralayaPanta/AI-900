- [Fundamentals of Text Analysis with the Language Service](#fundamentals-of-text-analysis-with-the-language-service)
    - [Tokenization](#tokenization)
    - [Frequency analysis](#frequency-analysis)
    - [Machine learning for text classification](#machine-learning-for-text-classification)
    - [Semantic language models](#semantic-language-models)
    - [Azure AI Language Features](#azure-ai-language-features)
- [Fundamentals of question answering with the Language Service](#fundamentals-of-question-answering-with-the-language-service)
    - [Create custom question answering](#create-custom-question-answering)
- [Fundamentals of conversational language understanding](#fundamentals-of-conversational-language-understanding)
    - [Azure resource for converstaional language understanding](#azure-resource-for-converstaional-language-understanding)
- [Fundamentals of Azure AI Speech](#fundamentals-of-azure-ai-speech)
    - [Azure AI Translator](#azure-ai-translator)
    - [Azure resources for Azure AI Speech](#azure-resources-for-azure-ai-speech)
- [Common NLP tasks supported by language models include:](#common-nlp-tasks-supported-by-language-models-include)


# Fundamentals of Text Analysis with the Language Service
- Text analysis describes NLP processes that extract information from unstructured text.

### Tokenization
  - break down body of text into tokens
    - uses techniques like
        - text normalisation
        - stop word removal
        - n-grams muti-term phrases
          - extends frequency analysis to include mlti term phrases
        - *stemming* is a technique in which algorithm are applied to consolidate words before counting them
          - Lemmatization or stemming, normalises words before counting them

### Frequency analysis
  - counting the number of occurrences of each token
  - types
    - simple frequency analysis
    - Term frequency - inverse document frequency TF-IDF
  
### Machine learning for text classification
  - use of a classification algorithm like logistic regression
    - logistric regression trains a machine learning model that classifies text based set of categorisation
    - to train a model that classifies a text as positive or negative in order to perform sentiment analysis or opinion mining

### Semantic language models
  - Encoding of language tokens as vectors (multi valued arrays of numbers) is known as embedding
    - ***Vectorization*** captures semantic relationships between words by assigning them to locations in n-dimensional space.


### Azure AI Language Features
- ***Named entity recognition*** - identifies people, places, events, and more.
- ***Entity linking*** - identifies known entities together with a link to Wikipedia.
- ***Personal identifying information (PII) detection*** - identifies personally sensitive information, including personal health information (PHI).
- ***Language detection***-  identifies the language of the text and returns a language code such as "en" for English.
- ***Sentiment analysis and opinion mining*** - identifies whether text is positive or negative.
      - evaluates text and returns sentiment scores and labels for each sentence
- ***Summarization*** - summarizes text by identifying the most important information.
- ***Key phrase extraction*** - lists the main concepts from unstructured text.

# Fundamentals of question answering with the Language Service
- ***Question answering*** supports natural language AI workloads that require an automated conversational element.
- Two Core Services:
  -  **Azure AI Language:** includes a custom question answering feature that enables you to create a knowledge base of question and answer pairs that can be queried using natural language input.
  -  **Azure AI Bot Service:** provides a framework for developing, publishing, and managing bots on Azure.

### Create custom question answering
  - can use Azure AI Language Studio to create, train, publish, and manage question answering projects
  - first provision a Language resource in Azure
  - Define questions and answers
  - Test the projects
  
# Fundamentals of conversational language understanding

  - Utterances, Entities and Intent
      - An utterance is an example of something a user might say, and which your application must interpret. 
      - An entity is an item to which an utterance refers.
      - An intent represents the purpose, or goal, expressed in a user's utterance.

### Azure resource for converstaional language understanding
  - ***Azure AI Language:*** A resource that enables you to build apps with industry-leading natural language understanding capabilities without machine learning expertise. You can use a language resource for authoring and prediction.
  - ***Azure AI services:*** A general resource that includes conversational language understanding along with many other Azure AI services. You can only use this type of resource for prediction.


# Fundamentals of Azure AI Speech
-  Speech recognition - the ability to detect and interpret spoken input
      -  takes the spoken word and converts it into data that can be processed - often by transcribing it into text.
      -  models
            -  An acoustic model that converts the audio signal into phonemes (representations of specific sounds).
            -  A language model that maps phonemes to words, usually using a statistical algorithm that predicts the most probable sequence of words based on the phonemes.
-  Speech synthesis - the ability to generate spoken output
      -  To synthesize speech, the system typically tokenizes the text to break it down into individual words, and assigns phonetic sounds to each word. 
      -  It then breaks the phonetic transcription into prosodic units (such as phrases, clauses, or sentences) to create phonemes that will be converted to audio format. 
      -  These phonemes are then synthesized as audio and can be assigned a particular voice, speaking rate, pitch, and volume.
-  ***Azure AI Speech*** provides speech to text and text to speech capabilities through speech recognition and synthesis. 
   -  includes following:
         -  The Speech to text API
               -  convert audio to text from a range of sources, including microphones, audio files, and blob storage. 
               -  types: real-time transcription and batch transcription
               -  real-time transcription allows to transcribe text in audio streams
               -  batch transcription transcribe to text from stored on a file share, a remote server, or even on Azure Storage.
         -  The Text to speech API
               -  convert input text into human like synthesized speech
               -  neural voice powered by deep neural networks
                     -  prebuilt neural voice
                     -  custom neural voice
         -  Speaker recognition
         -  Speech translation         -  
         -  Pronunciation assessment
         -  Intent recognition

### Use speech in application
   - Speech Studio
       - UI based tools for building and integrating features from Azure AI speech service.
       - no code approach
   - SPeech CLI
       - command line tools for using Speech serivce
       - most feature in SDK are available in CLI
   - Speech SDK
       - available in many programming languages and across all platforms
       - if cant use SDK, use REST APIs


### Azure AI Translator
   - cloud based service that uses AI to reliably translate text and documents between languages in near real time.
   - 90 languages and dialects
   - uses Neural Machine Translation
   - can be personalised using Custom glossaries and Custom translation to increase fluency and readability
   - services and features
       - text to text translation
       - document translation
       - custom translation
       - automatic langauge detection
       - transliteration
       - dictionaries
       - profanity filters
   - Translator's text translation service uses a JSON-based Web API with text sent as strings.

### Azure resources for Azure AI Speech
- A Speech resource - choose this resource type if you only plan to use Azure AI Speech, or if you want to manage access and billing for the resource separately from other services.
- An Azure AI services resource - choose this resource type if you plan to use Azure AI Speech in combination with other Azure AI services, and you want to manage access and billing for these services together.

# Common NLP tasks supported by language models include:
- _Text analysis_, such as extracting key terms or identifying named entities in text.
- _Sentiment analysis_ and opinion mining to categorize text as positive or negative.
- _Machine translation_, in which text is automatically translated from one language to another.
- _Summarization_, in which the main points of a large body of text are summarized.
- _Conversational AI solutions_ such as bots or digital assistants in which the language model can interpret natural language input and return an appropriate response.