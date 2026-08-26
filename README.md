summArIze

summArIze is an AI-powered study platform designed to help students transform educational content into easier-to-understand study materials. The application supports text and video-based summarization along with interactive study tools to make reviewing course material more efficient.

This project was developed as a collaborative software engineering project at California State University, Northridge.

Features

* YouTube Video Summarization — Submit a YouTube URL and generate an AI-powered summary of the video’s content.
* Text Summarization — Transform large amounts of text into concise, structured summaries.
* Document Processing — Process educational content from supported document formats such as PDF and DOCX.
* AI-Generated Study Tools — Generate interactive study materials based on submitted content.
* Student Dashboard — Provides a centralized interface for accessing study tools and content.
* Multi-Model AI Integration — Integrates AI services from OpenAI and Anthropic.

My Contribution

My primary contribution to summArIze was the YouTube video summarization feature.

I worked on the functionality that allows users to provide a YouTube URL and receive an AI-generated summary of the video’s content. This involved connecting the video input and transcript-processing workflow with the application’s AI summarization functionality and displaying the generated results within the application.

Through this feature, I gained hands-on experience working with AI APIs, processing external content, integrating frontend and backend functionality, and developing an LLM-powered feature within a larger collaborative application.

Tech Stack

Frontend

* Next.js 16
* React 19
* TypeScript
* Tailwind CSS

AI

* OpenAI API
* Anthropic Claude API

Backend & Services

* Next.js API Routes
* Firebase

Content Processing

* YouTube Transcript
* FFmpeg
* PDF Parse
* Mammoth

Getting Started

1. Clone the repository

git clone <repository-url>
cd summArIze

2. Install dependencies

npm install

3. Configure environment variables

Create a .env.local file and add the API keys and Firebase configuration required by the application.

Do not commit API keys or other secrets to GitHub.

4. Start the development server

npm run dev

Open http://localhost:3000 in your browser.

Project Purpose

summArIze was created to explore how generative AI can improve the way students interact with educational content. Instead of manually reviewing long videos, documents, or blocks of text, students can use AI-powered tools to extract key information and create more manageable study materials.

Team

Developed as a collaborative student project at California State University, Northridge (CSUN).

Disclaimer

This project was developed for educational purposes. AI-generated content may contain inaccuracies and should be reviewed against the original source material.
