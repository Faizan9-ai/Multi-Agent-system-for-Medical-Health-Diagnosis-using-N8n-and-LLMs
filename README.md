AI-Powered Multi-Agent Medical Health Report Analyzer using n8n
📌 Project Overview

The AI-Powered Multi-Agent Medical Health Report Analyzer is an intelligent healthcare automation system built using n8n, Groq LLM, Tavily API, Gmail API, and JavaScript.

This system automates the process of analyzing patient medical reports, generating health insights, recommending doctors, providing personalized health recommendations, and sending automated emails and reminders.

The workflow demonstrates how multiple AI agents can collaborate inside a low-code automation platform to create a real-world healthcare assistant.

🚀 Features

1. Medical Report Analysis
Upload medical reports in PDF format
AI extracts symptoms and medical conditions
Generates summarized patient analysis

2.Structured JSON Processing
Cleans and converts AI output into structured JSON
Extracts:
Symptoms
Condition classification
Warnings
Recommended department

3. Doctor Recommendation Agent
Uses Tavily API to search nearby specialists
Suggests suitable doctors and hospitals
Generates appointment recommendation details


4. Personal Recommendation Agent
Provides:
Diet recommendations
Exercise suggestions
Daily routine improvements
Recovery tips

5. Automated Email System
Sends:
Appointment confirmation emails
Personal health recommendation emails
Reminder emails

6. Reminder Automation
Wait node automatically triggers reminder emails after a specified time interval


`  🧠 Multi-Agent Architecture

The project uses multiple AI agents working together:

Agent	Purpose

1. Medical Health Report Analyzer -  Analyzes uploaded medical reports
2. Clean Medical Report Agent - 	  Converts AI response into structured JSON
3. Doctor Recommendation Agent - 	  Finds suitable doctors and hospitals
4. Personal Recommendation Agent -  Generates health, diet, and exercise advice
5. Email Automation Agent -       	Sends confirmation and reminder emails


🛠️ Technologies Used
Technology	Purpose
1. n8n	Workflow automation platform
2. Groq LLM	AI-powered report analysis
3. Tavily API	Doctor and hospital search
4. Gmail API	Email automation
5. JavaScript	JSON parsing and data cleaning
6. HTTP Request Node	API integration
7. Wait Node	Reminder scheduling


📂 Workflow Architecture
Form Submission
      ↓
Medical Health Report Analyzer
      ↓
Clean Medical Report
      ├── Personal Recommendation Agent
      │         ↓
      │   Personal Health Recommendation Email
      │
      └── Doctor Recommendation Agent
                ↓
      Appointment Confirmation Email
                ↓
               Wait
                ↓
      Appointment Reminder Email



⚙️ Workflow Explanation
1️⃣ On Form Submission

The workflow starts when a patient uploads a medical report.

2️⃣ Medical Health Report Analyzer

The Groq LLM analyzes:

Symptoms
Medical conditions
Severity
Recommended department

Example:

ENT specialist
General physician
3️⃣ Clean Medical Report

A JavaScript node:

Cleans raw AI response
Removes escape characters
Converts response into structured JSON
4️⃣ Personal Recommendation Agent

Generates:

Healthy diet suggestions
Exercise plans
Sleep recommendations
Recovery tips
5️⃣ Doctor Recommendation Agent

Uses Tavily API to:

Search nearby specialists
Recommend hospitals/doctors
Generate appointment guidance
6️⃣ Email Automation

Sends:

Appointment confirmation email
Personal health recommendation email
7️⃣ Reminder Alert System

The Wait node pauses workflow execution for a specified interval and later sends reminder emails automatically.

📧 Example Outputs
Doctor Recommendation Email
Suggested doctors
Hospital details
Appointment guidance
Personal Recommendation Email
Diet plan
Exercise tips
Routine improvements
Health precautions
Reminder Email
Follow-up appointment reminder
Medication reminder
