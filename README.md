# AnnRakshak-Your-Ai-Crop-Guardian
AnnRakshak: Your AI-Powered Crop Guardian

Demo Video Link : https://youtube.com/shorts/3o5YOUMAyEQ

AnnRakshak is an AI-powered Telegram bot designed to serve as a digital assistant for Indian farmers and distributors. It helps them monitor produce freshness, predict spoilage in real-time, and get actionable recommendations to reduce food waste and prevent financial loss. This project is a submission for the OpenAI NextWave Buildathon 2025.

1. Problem Statement

India faces a critical challenge with post-harvest losses, with up to 16% of fruits and 12% of vegetables perishing before they reach a consumer. For a small-scale farmer, this is a devastating financial blow. The primary cause is an information gap: a lack of accessible, real-time tools to monitor crop health and predict spoilage based on rapidly changing weather conditions. Farmers are left to guess, and a single spike in humidity can ruin an entire harvest.

2. Solution

AnnRakshak closes this information gap by putting an AI-powered crop expert directly into a farmer's pocket through Telegram, a platform they already know and trust. The bot acts as a friendly, conversational partner that analyzes a farmer's produce and provides immediate, personalized advice in their own regional language.

3. How It Works

The user experience is designed to be as simple as talking to a friend.

Step 1: The User Sends an Input
A farmer sends a photo, video, text description, or voice note of their produce to the AnnRakshak Telegram bot.

Step 2: The Bot Asks for Context
The bot immediately replies, asking for the user's city (for weather) and their preferred language for the response.

Step 3: AI Analysis in the Backend
Our N8N workflow takes all the inputs (the user's media, text, location, and language choice), fetches live weather data from OpenWeatherMap, and sends the complete package to the OpenAI API.

Step 4: Actionable Advice is Delivered
The bot sends back a simple, clear analysis and a step-by-step action plan in the user's chosen language.

4. Tech Stack:
   
Bot Framework: Telegram Bot API

Workflow Automation: N8N (as the central orchestrator)

AI Integration:
OpenAI GPT-4o: For multimodal analysis and generating recommendations.
OpenAI Whisper: For transcribing voice note inputs.

External Data: OpenWeatherMap API for real-time weather data.

6. Setup and Installation:
This project is built on N8N and can be easily reproduced.

1. Prerequisites: You need a running instance of N8N.
2. Import Workflow: Download the `AnnRakshak.json` file from this repository. In your N8N canvas, go to `File > Import from File` and select the downloaded JSON file.
3. Add Credentials: The workflow requires credentials for the following services. You will need to add your own API keys in the "Credentials" section of N8N:
    *   Telegram Bot API
    *   OpenAI API
    *   OpenWeatherMap API
4.  Activate Workflow: Once the credentials are in place, activate the workflow. Your bot is now live and ready to respond to messages on Telegram.
