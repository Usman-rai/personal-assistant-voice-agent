# personal-assistant-voice-agent
A personal assistant voice agent using ElevenLabs + n8n. It can answer user questions, schedule meetings, send appointment notifications, provide personal or business information, and act as a voice receptionist on any website. Connected via webhook with AI-powered responses.
# Personal Assistant Voice Agent – 11Labs + n8n (AI Voice Receptionist)

This project is an **AI-powered personal assistant voice agent** built using **ElevenLabs**, integrated with **n8n**, and connected through a **Webhook**.  
It acts as a **professional voice receptionist** for websites or platforms, helping users:

- Get information about you or your company  
- Ask questions through voice  
- Request meetings or appointments  
- Receive instant voice replies  
- Trigger follow-up workflows such as email alerts  

When a user asks to **book a meeting**, the system automatically sends an email to you (or your team), informing you that someone wants an appointment. You can then confirm or respond manually.

This voice agent works like your own **AI Secretary**, available 24/7.

---

## 🎤 Key Features

- 🔊 Real-time AI voice assistant using **ElevenLabs Voice Agent**
- 🌐 Works on any website via **Webhook → n8n**
- 🧠 Answers questions using **AI (OpenAI)**  
- 📅 Handles **meeting / appointment requests**
- 📧 Sends email notifications to you when someone wants to meet  
- ℹ️ Provides platform info, personal details, service info  
- 🗣️ Responds with natural, human-like voice  
- 🔄 Fully customizable workflow in n8n  
- 🧩 Can be used as:
  - Personal mission helper  
  - Customer support assistant  
  - Lead qualification tool  
  - Voice chatbot for business websites  

---

## 🧠 Tools & Technologies

- **ElevenLabs Voice Agent API** – voice interaction  
- **n8n** – workflow automation  
- **Webhook Trigger** – receives voice events  
- **OpenAI Node** – processes user intent + generates answers  
- **Send Email Node** – sends appointment notifications  
- **IF / Switch Nodes** – detect when user wants a meeting  
- **Website Widget** – for embedding the voice agent  

---

## 📂 Repository Structure

---

## 🚀 How It Works (Workflow Logic)

### 1. User Speaks to the Voice Agent
- User clicks mic on your website  
- Speaks their question or request (e.g., “I want to book a meeting”)

### 2. ElevenLabs Converts Voice → Text  
- The text is sent to your **n8n webhook**

### 3. n8n Receives the Webhook Event  
The webhook contains:
- User message  
- Session ID  
- User metadata  
- Intent data  

### 4. AI Processes Intent  
The **OpenAI node**:
- Understands if the user wants:
  - Information
  - Appointment booking
  - Personal details
  - Business details  

- Generates a smart assistant-style reply  

### 5. Send Back to ElevenLabs  
- n8n returns the AI response  
- ElevenLabs converts text → voice  
- User hears the answer immediately  

### 6. Appointment Handling (Important)  
If user says:
- “I want a meeting”
- “Book an appointment”
- “I want to talk to Usman”

Then:

- n8n triggers **appointment workflow**  
- Sends an email to YOU (admin)  

Email includes:
- User’s name (if available)  
- Requested meeting time (if mentioned)  
- Their message  
- A note: “Someone wants to book a meeting with you.”  

### 7. You Confirm the Meeting  
You receive the email and respond manually.

---

## 🛠️ Setup Instructions

### 1. Import Workflow Into n8n

1. Open n8n  
2. Go to **Workflows → Import from file**  
3. Upload `assistant-voice-agent-workflow.json`  
4. Click **Import**

---

### 2. Configure Webhook URL

1. Open **Webhook node** in n8n  
2. Copy the URL  
3. Go to **ElevenLabs Voice Agent Dashboard**  
4. Add the webhook under **Actions → Webhook**  
5. Select events like:
   - `agent_message`
   - `user_message`
   - `session_start`
   - `session_end`

---

### 3. Setup OpenAI Node

- Add your OpenAI key in n8n Credentials  
- Customize the system prompt, example:

> "You are a personal voice assistant for Rai Usman.  
> You answer questions professionally, provide details about his profile,  
> and help book appointments when requested."

---

### 4. Setup Email Notifications

1. Open **Send Email** node  
2. Add Gmail/SMTP credentials  
3. Set:
   - To: your email  
   - Subject: “New Meeting Request (Voice Agent)”  
   - Body: include user message, intent, etc.  

---

### 5. Embed Voice Agent on Website

From ElevenLabs:

- Get your embed script  
- Paste into your website HTML  
- The voice assistant appears and is ready  

---

## ✨ Use Cases

- Personal assistant on your website  
- Appointment booking bot  
- Lead qualification via voice  
- Customer support chatbot  
- Business information voice guide  
- Mission assistant for personal productivity  

---

## 🎓 Why This Project Is Valuable

This project showcases high-level skills:

- AI voice tech (ElevenLabs)
- Workflow automation (n8n)
- Intelligent intent detection (OpenAI)
- Real business automation (meeting requests)
- Webhook integrations
- Email routing and notifications
- Live conversational agents

This looks **excellent** on your GitHub and for **university applications**.

---

## 👤 Author

**Rai Usman**  
GitHub: [@Usman-rai](https://github.com/Usman-rai)


