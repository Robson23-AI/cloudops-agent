# cloudops-agent
AI-driven IT automation platform using ServiceNow, AWS Bedrock, Lambda and Teams. Delivers KB suggestions, RCA, insights, and automated incident workflows with full security, anonymization and guardrails.
# CloudOps Agent – AI-Powered IT Support Automation

CloudOps Agent is an AI-driven automation platform designed to enhance enterprise IT support operations.  
It integrates ServiceNow, AWS Bedrock, AWS Lambda, and Microsoft Teams to deliver:

- Intelligent KB suggestions  
- Automated root cause analysis (RCA)  
- AI-generated test incidents (Ticket Generator)  
- Recurring issue detection (Insight Engine)  
- Real-time notifications to Microsoft Teams  
- Secure prompt engineering with guardrails  
- Full anonymization and sanitization layer  

---

## Key Features

### Smart KB Finder  
Classifies incidents and recommends relevant knowledge base articles with confidence scoring.

### Root Cause Analyzer  
Uses structured reasoning to analyze issues step by step and provide actionable insights.

### User Insight Engine  
Identifies recurring issues by evaluating historical patterns across users, assets, or services.

### AI Ticket Generator  
Creates realistic ServiceNow incidents stored in S3 to support automated testing and demos.

### Microsoft Teams Integration  
Delivers concise and structured summaries directly to a Teams channel via webhook.

---

## Architecture Overview

The system uses a modular, serverless design.

High-level architecture:

ServiceNow
→ API Gateway
→ Lambda (sanitization, anonymization, module routing)
→ Amazon Bedrock (LLM inference + guardrails)
→ Lambda (post-processing)
→ Microsoft Teams Webhook


Detailed documentation:  
- docs/architecture.md  
- docs/security.md  

---

## Security and Responsible AI

The project implements:

- Input sanitization to block prompt injection patterns  
- Anonymization of all user-sensitive fields  
- AWS Bedrock Guardrails configuration  
- Confidence thresholds and validation gates  
- Explainability trace for AI-generated responses  
- Bias and variance control mechanisms  
- GDPR-safe handling of ServiceNow data  

---

## Tech Stack

- AWS Lambda  
- Amazon Bedrock (Claude, Mistral)  
- Amazon S3  
- Amazon DynamoDB  
- API Gateway  
- Microsoft Teams Webhooks  
- Python 3.12  
- ServiceNow REST API  

---

## License

This project is licensed under the MIT License.

---

## Author

Robert A. Łukowski  
2025  
