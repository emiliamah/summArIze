# Project Requirements Document (PRD)

## 1. Project Overview

**Project Name:**  
summArIze  

**Team Members:**  
- Novali Plascencia  
- Emilia Mahmoodi  
- Andy Moughalian  
- Roee Palmon  
- Christian Rusanovsky  

**Date:**  
February 17, 2026  

---

## 2. Problem Statement

Many students struggle to keep up with lectures, long readings, and study materials. College and high school students often feel overwhelmed and don’t have enough time to review everything before exams. Notes can be confusing, videos are long, and studying is not always effective.

summArIze solves this problem by using AI to summarize text, videos, and lectures, create quick study guides, and generate quizzes so students can learn faster, understand better, and study more efficiently.

---

## 3. Goals and Objectives

The main goal of summArIze is to help students take control of their academic success through intelligent AI-powered study support. The platform simplifies understanding lectures, organizing notes, generating practice quizzes, and tracking progress all in one place to improve learning efficiency and retention.

### Objectives

1. **Intelligent Summarization**  
   Provide AI-generated summaries that extract key concepts, definitions, and main ideas from text and video content, making complex material easier to understand.

2. **Automated Note Generation**  
   Convert raw lecture content into clean, organized notes with headings, bullet points, and highlighted key takeaways.

3. **Active Learning Support**  
   Generate quizzes (multiple choice, true/false, short answer) from uploaded content and provide instant feedback with explanations to reinforce understanding.

4. **Centralized Study Platform**  
   Allow users to upload notes, documents, or lecture materials and access all AI-generated summaries, quizzes, and notes within a single dashboard.

5. **Multi-AI Integration**  
   Implement a modular AI architecture that utilizes multiple cloud AI services to handle different tasks (summarization, quiz generation, feedback), demonstrating scalable and advanced AI system design.

6. **User-Friendly Experience**  
   Deliver a clean, intuitive interface that allows users to upload content, generate study materials, and review results quickly and seamlessly.

---

## 4. Features

### Required (Core Functionality)

These are must-have features for summArIze to function properly.

- **User Accounts**  
  Users must be able to sign up, log in, and securely store their data using Firebase Authentication and Firestore. User-generated summaries, notes, and quizzes will be saved to their account.

- **Text Upload & Input**  
  Users can paste text or upload documents (e.g., lecture notes, readings, PDFs) for AI processing.

- **AI Text Summarization**  
  The system generates concise summaries from uploaded or pasted content, extracting key concepts and main ideas.

- **Automated Note Generation**  
  AI converts raw content into structured notes with headings, bullet points, and highlighted key terms.

- **Quiz Generation**  
  The system generates practice quizzes (multiple choice, true/false, short answer) based on the summarized material.

- **Instant Feedback & Answer Evaluation**  
  AI evaluates user quiz responses and provides explanations for correct and incorrect answers.

- **Dashboard**  
  Displays saved summaries, generated quizzes, and past study sessions in a centralized, easy-to-navigate interface.

- **Database Integration**  
  Firestore stores user content, summaries, quizzes, quiz attempts, and progress history securely.

---

### Desired (Improves Usability & Appearance)

These features improve usability, engagement, and overall user experience but are not required for core functionality.

- **Progress Dashboard**  
  Visual charts displaying study activity, number of summaries generated, quiz performance over time, and study streaks.

- **Profile Customization**  
  Users can upload profile pictures and personalize study preferences such as learning style, difficulty level, and AI response format.

- **Responsive UI/UX Design**  
  A clean, distraction-free interface that works smoothly on desktop and mobile devices. Organized workflow structure: Upload → Summary → Quiz → Feedback.

- **Searchable Notes Library**  
  Users can search, filter, and revisit previously uploaded documents, summaries, and quizzes.

- **File Preview Before Processing**  
  Users can preview uploaded PDFs before generating summaries.

- **Notifications and Study Reminders**  
  Optional reminders to review notes, complete quizzes, or maintain study streaks.

- **Dark Mode**  
  Optional interface theme to reduce eye strain during extended study sessions.

---

### Aspirational (Stand-Out & Advanced Features)

These features differentiate summArIze as a next-generation AI learning assistant.

- **AI Study Coach**  
  A conversational AI agent that answers follow-up questions, explains difficult concepts, and provides interactive tutoring support.

- **Multi-Agent Architecture**  
  Separate AI agents for:
  - Text Summarization  
  - Video/Lecture Processing  
  - Quiz Generation  
  - Evaluation and Feedback  

  Each agent may be powered by different cloud AI APIs and orchestrated within a unified system.

- **Personalized Study Plans**  
  AI-generated weekly study schedules based on deadlines, exam dates, difficulty level, and past quiz performance.

- **LMS Integration**  
  Integration with platforms such as Canvas or Google Classroom.

- **Gamification**  
  Badges, streaks, study milestones, and optional leaderboards.

- **Voice-to-Notes Processing**  
  Upload lecture audio recordings that are automatically transcribed and summarized.

- **Premium AI Analytics**  
  Topic mastery analysis, weak concept detection, adaptive quiz difficulty, and exam-readiness prediction.

---

## 5. Target Audience

summArIze is designed for students and academic learners who want to improve study efficiency using AI-powered tools.

### Primary Audience

- College students (ages 18–25)
- Students balancing multiple courses
- Individuals preparing for midterms, finals, or competitive exams

### Common Challenges

- Overwhelming reading material
- Disorganized notes
- Inefficient study strategies
- Difficulty understanding complex concepts

summArIze provides structured AI-generated summaries, interactive quizzes, and personalized feedback to simplify studying and improve knowledge retention.

It is particularly valuable for:

- STEM students managing dense academic material
- Working students with limited study time
- Learners who benefit from adaptive and interactive studying

---

## 6. Technical Requirements

summArIze uses a multi-cloud, multi-agent architecture leveraging Google Cloud, Amazon Web Services (AWS), and Microsoft Azure.

---

### 1. Frontend Framework

- **Next.js (React Framework)**  
  Provides a fast, scalable, server-side rendered web application with a structured workflow:  
  Upload → Transcription → Summary → Quiz → Feedback.

---

### 2. Database and Storage (Google Cloud)

- **Google Firestore**
  - Stores user profiles
  - Uploaded document metadata
  - Audio transcription results
  - Generated summaries
  - Study guides
  - Quiz questions and results

- **Firebase Storage**
  - Stores uploaded PDFs and audio files before processing

---

### 3. AI Services (Multi-Cloud Architecture)

#### Google Cloud – Gemini API
Responsible for:
- Summarizing lecture notes and readings
- Extracting key concepts
- Generating structured study guides
- Creating quiz questions

#### Amazon Web Services – AWS Transcribe
Responsible for:
- Converting lecture audio/video to text
- Storing transcripts in Firestore
- Sending transcripts to the Summarization Agent

#### Microsoft Azure – Azure AI Foundry
Responsible for:
- Hosting and organizing separate AI agents
- Supporting evaluation workflows
- Connecting summarization, quiz generation, and feedback agents

---

### 4. Multi-Agent Architecture

- **Summarization Agent**
- **Quiz Generation Agent**
- **Evaluation Agent**
- **Transcription Agent**

Agents communicate via secure backend API routes.

---

### 5. Backend Logic

- Next.js API routes manage:
  - Secure communication with AI services
  - File validation and preprocessing
  - Agent-to-agent data transfer
  - Authentication and authorization

All AI requests are handled server-side.

---

### 6. Authentication and Security

- Firebase Authentication
- HTTPS encryption
- API keys stored in environment variables
- Firestore security rules enforce per-user data access

---

### 7. Hosting and Deployment

- **Vercel**

---

### 8. Performance Requirements

- AI response time under 10 seconds
- Efficient audio transcription
- Real-time dashboard updates
- Support for concurrent users

---

### 9. System Objective

To integrate:

- Google Cloud (Gemini API and Firestore)
- Amazon Web Services (AWS Transcribe)
- Microsoft Azure (Azure AI Foundry)

into a unified, intelligent, multi-agent AI study assistant that improves student learning efficiency and academic performance.
