# 🚀 Automated Joiner (Onboarding) Process Using Copilot Studio & Power Platform

This project demonstrates an **automated employee onboarding process (Joiner Process)** built using **Microsoft Copilot Studio, Power Automate, SharePoint, and Azure Entra ID**. It was developed to optimize and automate the Joiners-Movers-Leavers (JML) workflow for a client’s HR and IT operations, reducing manual tasks and increasing process accuracy.

---

## 📋 Problem Statement

Manual onboarding processes involve repetitive tasks such as:
- Monitoring Zendesk Tickets for New Joiners
- Azure Entra ID account creation  
- Email setup & distribution list management  
- Hardware & application provisioning  
- Multi-step approvals with HR, Line Managers, and IT
- Filling Zendesk Ticket Forms for audit & tracking purposes

These manual processes are often:
- Time-consuming  
- Error-prone  
- Inefficient in scaling with company growth  

**Solution:** Automate the entire onboarding process using AI-powered agents and workflows to reduce manual effort, increase accuracy, and improve employee experience.

---

## 🏗️ Architecture Diagram

![Architecture Diagram](/Architecture_Diagram.jpg)

---

## 🔧 Tech Stack Used
- **Microsoft Copilot Studio:** Agent-based automation platform for conversational workflows  
- **Power Automate:** Backend process orchestration and approvals  
- **AI Hub (Power Automate):** Used for AI-based email parsing and prompt-based response formatting 
- **Zendesk Integration:** Ticket Monitoring for any new joiner request, utilized as trigger for the process 
- **SharePoint:** Used as a central data repository for storing onboarding details  
- **Azure Entra ID:** For user creation, security group management, and role assignments  
- **Microsoft Forms:** For collecting specific onboarding inputs  
- **Approvals (Power Automate):** Multi-step, role-based approval workflows  
- **Azure Runbook (Optional):** For advanced email distribution group automation


---

## 🔄 Process Overview

### 1. **Trigger Event - Zendesk**
The process begins automatically when an onboarding request ticket is received on Zendesk. AI Prompts parse the ticket information into structured JSON data and store it in SharePoint.

### 2. **Copilot Studio Agent Flow**
- The Onboarding steward greets the agent and initiates the onboarding flow.
- Now the agent fetches the details of the latest new joiner from SharePoint.
- Sends a Line Manager approval request, along with a form to specify hardware and application needs.

### 3. **Account & Group Setup (Azure Entra ID)**
- Creates Entra ID account for the new employee.
- Updates department, job title, and phone number.
- Assigns security groups and email distribution groups.

### 4. **US-Specific Processing (Conditional)**
- If the applicant is based in the US, additional approval is required to fetch and update the Employee ID on Entra & SharePoint.

### 5. **Zendesk Joiner Form Update**
- The agent triggers a Power Automate flow to complete a checklist on the Zendesk Ticket's form for the IT Team to track the progress on the onboarding.

### 6. **Hardware & Application Provisioning**
- Sends a summary to IT for provisioning hardware and software.
- Initiates approvals from IT and then from the new joiner to confirm successful onboarding.

### 7. **New Joiner Notification**
- Sends an email dynamically fetching the user details like the Applicant Name, Department, Role etc. to the organisation to welcome the new joiner.

## 🙋‍♂️ Author
Sarthak Sharma  
*Low-Code Developer | AI Automation/Innovation Engineer*
