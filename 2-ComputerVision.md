
Table of Content
- [Fundamental of Computer Vision](#fundamental-of-computer-vision)
        - [Review Computer vision models](#review-computer-vision-models)
    - [Convolutional Neural Networks CNNs](#convolutional-neural-networks-cnns)
    - [Multi Modal Models](#multi-modal-models)
    - [Azure Resources for Azure AI Vision service](#azure-resources-for-azure-ai-vision-service)
- [Fundamental of Facial Recognition](#fundamental-of-facial-recognition)
    - [Face analysis](#face-analysis)
    - [Azure for Face Analysis](#azure-for-face-analysis)
- [Fundamental of Optical Character Recognition](#fundamental-of-optical-character-recognition)
    - [Azure AI Vision OCR Engine](#azure-ai-vision-ocr-engine)


# Fundamental of Computer Vision

Area of AI focusing on creating solutions that enable AI applications to see the world and make sense of it.
- Algorithms:
    - convolutional neural network CNN
    - recurrent neural network RNN

##### Review Computer vision models
- _image classification_ - classify images based on contents
- _object detection_ - classify individual objects within an image and and identify their location with a bounding box.
    - information 
        - bounding box
        - class name
        - probability score
- _semantic segmentation_ - classify individual pixels
    - provides the ability to classify individual pixels in an image depending on the object that they represent.
- _image analysis_ - model to extract information from images
      - example: an employee sitting at a desk in office
- _face detection and recognition_ - locates human faces in an image
- _optioncal character recognition OCR_ - detect and read text in images

### Convolutional Neural Networks CNNs
- CNNs user filters to extract numeric feature maps from images, and then feed the feature values into a deep learning model to generate a label prediction.
- How does CNN for an image classification model work:
    - Images with known label are fed into the network to train the model
    - One or more layers of filters is used to extract features from each image. It starts with random weights and generate arrays of numeric values called feature maps.
    - The feature maps are flattened into a single dimensional array of feature values.
    - The output layer of the neural network uses a softmax or similar function to produce a result that contains a probability value for each possible class.

- During the training process difference between predicted and actual class score called loss in model is calculated. To reduce the loss weights is optimised in each of the iteration. 

- **Object detection** models combine CNN feature extraction layers with the identification of regions of interest in images to locate multiple classes of object in the same image.
    - Object detection provides the ability to generate bounding boxes that identify the locations of different types of objects in an image, including the bounding box coordinates, designating the location of the object in the image.
    - _Image classification_ is a machine learning based form of computer vision in which a model is trained to categorize images based on the primary subject matter they contain. _Object detection_ goes further than this to classify individual objects within the image, and to return the coordinates of a bounding box that indicates the object's location.

### Multi Modal Models
- Model is trained using a large volume of captioned images with no fixed labels
- An image encoder extracts features from images based on prixel values and combines them with text embeddings created by a language encoder.
  
- **The Microsoft Florence Model** is trained with huge volumes of captioned images from the internet with both language encoder and an image encoder.
  - Florence is an example of foundation modal
  - Can be used in adaptive models like object detection, captioning, tagging, image classification

### Azure Resources for Azure AI Vision service

  - **Azure AI Vision**
      - specific resource for vision service
      - user this if you do not intend to use other azure AI service
      - supports the celebrities and landmarks specialized domain models.
  
  - **Azure AI Services**
      - general resources that includes other AI services as well
      - Use this resource type if you plan to use multiple AI services and want to simplify administration and development

  - Azure AI Vision support
      - OCR extracting text from images
      - Generating captions and descriptions of images
      - Detection of thousands of common objects in images
      - Tagging visual features in images
  - If the provided models do not meet the requirement, you can use the service to train a custom model for image classification or object detection
    - **Azure AI Custom Vision** is an image recognition service that allows you to build and deploy your own image models. 
  
# Fundamental of Facial Recognition

### Face analysis

- Face detection involves identifying regions of an image that contain a human face, typically by returning bounding box coordinates that form a rectangle around the face.
- can be used to train a machine learning model to identify known individuals from their facial features


### Azure for Face Analysis

- Azure AI Vision, offers face detection and some basic face analysis
- Azure AI Video Indexer, which you can use to detect and identify faces in a video
- Azure AI Face, which offers pre-built algorithms that can detect, recognise and analyse faces.

# Fundamental of Optical Character Recognition
- OCR is the capability of AI to process words in images into machine readable text.
- two API:
    - OCR API
        - older recognition model and supports only images
    - Read API
        - newer and supports images and PDFs
- OCR uses computer vision SDK

### Azure Form Recogniser
- specialise OCR service translates printed text into digital and editable content
- preserves structure and relationship of form like data
- key value pairs, selection marks, table structure
- models type
  - Form recogniser service - custom model
      - extract key value pairs, selection marks and table data
      - need five sample input forms to start
      - 2 learning options
          - train without labels
          - train with labels
  - Form recogniser service - prebuilt model
      - receipts
      - business cards
      - invoices
      - IDs
  

### Azure AI Vision OCR Engine

- It has ability to extract machine readable text from images
- _Read API_ is the OCR engine that powers text extraction from images, PDFs, and TIFF files
  - The engine takes in an image file and identifies bounding box where items are located within an image.
  - Calling the Read API returns results
      - Pages
      - Lines
      - Words
  - Each line and word includes bounding box coordinates indicating its position.
  
- Following resources can be used
    - Azure AI Vision
    - Azure AI Services

### Custom Vision
  -   fully managed no code service to quickly build own classification and object detection ML models
  -   domain customvision.ai
  -   upload images >> train >> evaluate
  -   project types
          -   classification: multi label, multi class
          -   object detection
  -   training model
          -   quick training
          -   advanced training