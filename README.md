# Useless-compliment-generator
A team effort by Kasinath R, Alen Alias Cheriyan, and Job Joseph, made as part of the Useless Competition event hosted by @tinkerhub on 20 August 2024. This program uses Computer Vision and compliments you in an overexaggerated way by identifying your distinct facial features, facial expression, and dressing. It uses OpenCV to process the image.

# Over-the-top Compliment Generator 🎯


Compliment cover.png


## Basic Details
### Team Name: Fake!?


### Team Members
- Team Lead: Alen Elias Cherian - Cochin University College Of Engineering,Kuttanad
- Member 2: Kashinath R - Cochin University College Of Engineering,Kuttanad
- Member 3: Job Joseph - Cochin University College Of Engineering,Kuttanad
### Project Description
This is a fun  AI integrated project which gives over -the-top compliments to any picture that is given as an input. This uses image processing to analyze the image, detecting features like smiles and dominant clothing colors, based on these the program generates personalized compliment using a language model.

### The Problem (that doesn't exist)
The lack of confidence  in modern era is reducing the creativity and all the related stuffs and is a major problem which affects the growth of universe(as if)
### The Solution (that nobody asked for)
Our program gives the user compliments like they have never heard before. That too personalized using AI. They will never get depressed without getting a compliment again.


## Technical Details

### Technologies/Components Used
Language used -python

Framework used - Gradio(for frontend development)

Libraries and tools  used -
    Gradio:
	• Framework for creating frontend.
	• Handles image inputs, text outputs
   Transformers:
	• A library from Hugging Face that has pre-trained GPT-2 which is used here for generating compliments.

   OpenCV:
	• Used for image processing - to detect smiles and to identify the colours.
	   PyTorch:
	• Provides backend support for models in the Transformers library
          


### Implementation
1. Image Processing using OpenCV
• Smile Detection: OpenCV uses CascadeClassifier with pre-trained Haar cascades for face detection and smile detection. First, the image is converted into grayscale, then faces are detected, and for every face, that region further scans for a smile.
• Colour detection: The KMeans function of Scikit-Learn was used to find the dominant color in some part of the chosen picture that is assumed to lie in the middle part if that contains clothing. Then it gets mapped to color classes of red, blue, or green for convenience.
2. Text generation using Hugging Face Transformers
• Language Model: This app uses a pre-trained GPT-2 model from Hugging Face Transformers for generating compliments. It is fine-tuned on text generation and forms the backbone of the language model in the app.
• Elaborate with Flattery: According to what the image analysis results come up with-the smile recognition and dominant color-a particular prompt is prepared that shall be fed into the GPT-2 model. The prompt will be of the sort: "You have a beautiful smile and gorgeous red attire." And, in a lighter-than-life, over-the-top mode, the model will then complete it.
3. Gradio Front-end Interaction
• User Interface: Gradio is used to develop the web interface in which user can upload an image and receive a generated compliment.
 • Input and Output: The Gradio interface will take the image as its input, and the output it would provide is the text developed by the model. Some of the easy-to-use components in Gradio include file upload and text display. This makes the application usable for the users.
• Deployment: Gradio can be run locally and, once published to Hugging Face Spaces, is available through a shareable link.
4. Development Environment Setup (Google Colab)
• Environment Setup: This prototype was developed in Google Colab so that all the dependencies required namely OpenCV, transformers and Gradio could be installed easily along with the ability to run the code without the hassle of having a local environment.
Integration testing: Google Colab accommodates step-by-step test and debug the functions and ensure that the image-analysis and text-generation functions works well together.

# Installation
!pip install gradio transformers torch opencv-python scikit-learn


# Diagrams
                     +-----------------------------+
                     |     Start                   |
                     +-----------------------------+
                               |
                               v
                     +-----------------------------+
                     |   Upload Image              |
                     | (via Gradio Interface)      |
                     +-----------------------------+
                               |
                               v
                     +-----------------------------+
                     |    Image Processing         |
                     |       using OpenCV          |
                     +-----------------------------+
                               |
                               |
                   +-----------+-------------+
                   |                         |
                   v                         v
         +-------------------+       +----------------------+
         | Smile Detection   |       | Color Detection      |
         | - Convert to      |       | - Extract center     |
         |   grayscale       |       |   region of image    |
         | - Detect face     |       | - Use KMeans to find |
         | - Detect smile    |       |   dominant color     |
         +-------------------+       +----------------------+
                   |                         |
                   v                         v
         +-------------------+       +----------------------+
         | Smile Detected?   |       | Identify Color       |
         | - Yes/No          |       | (Red, Green, Blue)   |
         +-------------------+       +----------------------+
                   |                         |
                   v                         v
      +---------------------------------------------+
      |          Prepare Prompt for GPT-2           |
      | - If smiling, add "You have a beautiful     |
      |   smile."                                   |
      | - Include outfit color (e.g., "Your red     |
      |   outfit looks stunning.")                  |
      +---------------------------------------------+
                               |
                               v
                     +-----------------------------+
                     |  Compliment Generation      |
                     |   using GPT-2 (Hugging Face)|
                     +-----------------------------+
                               |
                               v
                     +-----------------------------+
                     |   Display Compliment        |
                     | (via Gradio Interface)      |
                     +-----------------------------+
                               |
                               v
                     +-----------------------------+
                     |            End              |
                     +-----------------------------+




## Team Contributions
- Alen Elias Cherian : Made codes on smile detection. researched on the same and found out the necessary packages and things.
- Kashinath R : Coded for Colour detection. Researched tooooo much on the subject and found out the neccessities
- Job Joseph: Coded for compliment giving part. was successful in including GPT2 integration in the program
---
Made with ❤ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProject--24-24?link=https%3A%2F%2Fwww.tinkerhub.org%2Fevents%2FQ2Q1TQKX6Q%2FUseless%2520Projects)

