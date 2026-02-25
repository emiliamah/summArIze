# Functional Requirements Document (FRD)

## Project: summArIze  
## Version: 1.0  
## Group Name: Asteroid Destroyers  

**Team Members:**  
- Novali Plascencia  
- Emilia Mahmoodi  
- Andy Moughalian  
- Roee Palmon  
- Christian Rusanovsky  

---

# 1. Introduction

## 1.1 Purpose

The purpose of this document is to define the functional requirements for **summArIze**, an AI-powered study assistant that helps students summarize lectures, generate quizzes, evaluate understanding, and improve retention using multiple AI agents.

## 1.2 Scope

summArIze allows students to:

- Upload lecture notes or transcripts  
- Generate structured summaries  
- Create quizzes from content  
- Receive AI-generated feedback on their answers  
- Track study progress  

The system uses multiple AI agents, each responsible for a specific functionality.

---

# 2. System Overview

summArIze is a web-based application that integrates:

- Authentication system  
- File upload system  
- AI processing layer (multi-agent architecture)  
- Study dashboard  
- Progress tracking system  

---

# 3. User Roles

| Role | Description |
|------|------------|
| Student | Primary user who uploads content and interacts with AI |
| Admin (Optional) | Manages system settings and monitors usage |

---

# 4. Functional Requirements

## 4.1 Authentication

- **FR-1:** The system shall allow users to create an account.  
- **FR-2:** The system shall allow users to log in securely.  
- **FR-3:** The system shall allow users to log out.  
- **FR-4:** The system shall store user data securely in the database.  

---

## 4.2 Upload & Content Management

- **FR-5:** The system shall allow users to upload text files (PDF, DOCX, TXT).  
- **FR-6:** The system shall allow users to paste lecture content manually.  
- **FR-7:** The system shall store uploaded content under the user’s account.  
- **FR-8:** The system shall allow users to delete previously uploaded content.  

---

## 4.3 AI Agent: Text Summarization Agent

- **FR-9:** The system shall generate a structured summary of uploaded content.  

- **FR-10:** The summary shall include:
  - Key concepts  
  - Definitions  
  - Important formulas  
  - Bullet-point highlights  

- **FR-11:** The user shall be able to regenerate the summary.  
- **FR-12:** The user shall be able to choose summary length (short, medium, detailed).  

---

## 4.4 AI Agent: Quiz Generation Agent

- **FR-13:** The system shall generate quiz questions based on uploaded content.  

- **FR-14:** The system shall support multiple question types:
  - Multiple choice  
  - True/False  
  - Short answer  

- **FR-15:** The user shall be able to select the number of questions.  
- **FR-16:** The system shall randomize question order.  

---

## 4.5 AI Agent: Evaluation / Feedback Agent

- **FR-17:** The system shall evaluate user answers.  

- **FR-18:** The system shall provide:
  - Correct/incorrect status  
  - Explanation for correct answers  
  - Suggestions for improvement  

- **FR-19:** The system shall calculate quiz score percentage.  

---

## 4.6 AI Agent: Lecture/Video Processing Agent (Optional Expansion)

- **FR-20:** The system shall accept lecture transcripts.  
- **FR-21:** The system shall convert transcripts into structured summaries.  
- **FR-22:** The system shall extract key timestamps (advanced feature if time permits).  

---

## 4.7 Dashboard & Progress Tracking

- **FR-23:** The system shall display user study sessions.  

- **FR-24:** The system shall show:
  - Number of summaries generated  
  - Quiz score history  
  - Improvement trends  

- **FR-25:** The system shall allow users to revisit past quizzes.  

---

# 5. Non-Functional Requirements

## 5.1 Performance

- AI response time should be under 10 seconds per request.  
- The system shall support concurrent users.  

## 5.2 Security

- User authentication must use secure protocols.  
- User data must not be shared across accounts.  
- API keys must be stored securely in environment variables.  

## 5.3 Usability

- Interface must be intuitive and student-friendly.  
- The system must work on both desktop and mobile devices.  

## 5.4 Scalability

- The system shall support integration with multiple AI APIs.  
- The architecture shall allow adding new AI agents in the future.  

---

# 6. System Architecture (High-Level)

User
↓
Frontend (Next.js UI)
↓
Backend API
↓
AI Agent Layer (Summarizer / Quiz / Evaluator / Video Agent)
↓
Database (User data, quizzes, summaries)

---

# 7. Future Enhancements

- Spaced repetition system  
- Flashcard generation  
- AI study plan generator  
- Collaborative study mode  
- LMS integration  

---

# 8. Acceptance Criteria

The system is considered complete when:

- Users can upload content  
- AI generates summaries  
- AI generates quizzes  
- AI evaluates answers  
- Dashboard displays study progress  
- All features work without critical errors  
