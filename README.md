<h1 align="center">Sergio Illescas</h1>

<p align="center">
  <strong>Full-Stack & AI Engineer | Builder of products that work</strong>
</p>

<p align="center">
  <a href="https://linkedin.com/in/sergio-illescas-cabiro/">
    <img src="https://img.shields.io/badge/LinkedIn-sergio--illescas--cabiro-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:sergioillescascabiro@gmail.com">
    <img src="https://img.shields.io/badge/Email-sergioillescascabiro-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>

---

## About

Computer & AI Engineer with a dual Master's (UPM Madrid + IIT Chicago). I spent years in telecom engineering and enterprise systems (Java/Spring Boot, OpenShift, Kubernetes at Minsait/Indra) trained to measure twice, plan three times, and move only when everything was certain. That mindset taught me rigor - but it also held me back from building.

Moving to the US changed that. The people I met here, the culture of just shipping things, the bias toward action over perfection - it rewired how I think about engineering. I stopped waiting for the perfect architecture and started building, breaking, learning, and rebuilding. In a world that moves this fast, the engineers who win are the ones who invest in learning something new every single day and treat every failure as a lesson, not a stop sign.

Today I design multi-agent voice systems, build RAG pipelines, and ship full-stack platforms end-to-end. My public repos include post-mortems alongside the code because honest failure analysis is the fastest path to better architecture.

---

## Projects

### Ace Interviewer / InterviewOS

> **Overall Winner + Best Use of Gemini API** - Hack-a-Job Hackathon

**The Problem Solved:** We eliminated the anxiety and false confidence of generic interview prep by building a system that perfectly simulates the exact interview you are about to walk into.

AI mock interview platform that scrapes the actual job posting + company culture via Tavily (RAG), cross-references it against the candidate's resume, and generates hyper-personalized questions via Gemini 2.5 Pro. Interviews happen in real-time voice via LiveKit/Whisper, with per-answer scoring on specificity, structure, and persona fit.

**Key challenges:** Multi-service AI orchestration (Tavily > Gemini > LiveKit > Whisper) in a single session flow | Async state management across live voice sessions | Structured scoring engine feeding a Recharts analytics dashboard

<p>
  <img src="https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Tailwind_4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind"/>
  <img src="https://img.shields.io/badge/Gemini_2.5_Pro-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/LiveKit-000000?style=flat-square&logo=webrtc&logoColor=white" alt="LiveKit"/>
  <img src="https://img.shields.io/badge/Whisper-412991?style=flat-square&logo=openai&logoColor=white" alt="Whisper"/>
  <img src="https://img.shields.io/badge/Tavily_(RAG)-1C3C3C?style=flat-square" alt="Tavily"/>
  <img src="https://img.shields.io/badge/Recharts-FF6384?style=flat-square" alt="Recharts"/>
</p>


---

### Sic Barber Vortex

**The Problem Solved:** Everyone has experienced terrible, slow, and frustrating AI phone agents. We solved this poor experience by utilizing WebRTC through LiveKit Cloud and ElevenLabs to deliver an ultra-low latency, natural voice assistant that actually feels human.

Voice-first AI booking assistant for a barbershop powered by Vertex AI (Gemini 2.5). Uses Function Calling to query Google Calendar in real-time to verify availability before confirming any slot. Remembers recurring clients via SQLite for contextual upselling and handles Spanish, English, and French effectively. The system is designed to be connected to a real phone number to handle both inbound and outbound calls natively.

**Key challenges:** Ultra-low latency voice orchestration (LiveKit Cloud & ElevenLabs) | Live calendar availability via Function Calling | Client memory + intelligent upselling | End-to-end automation from voice interaction to native Slack notification webhooks

<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express"/>
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="GCP"/>
  <img src="https://img.shields.io/badge/Vertex_AI-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="Vertex AI"/>
  <img src="https://img.shields.io/badge/Gemini_2.5-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/LiveKit_Cloud-000000?style=flat-square&logo=webrtc&logoColor=white" alt="LiveKit"/>
  <img src="https://img.shields.io/badge/ElevenLabs-000000?style=flat-square" alt="ElevenLabs"/>
  <img src="https://img.shields.io/badge/Google_Calendar-4285F4?style=flat-square&logo=googlecalendar&logoColor=white" alt="Google Calendar"/>
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"/>
  <img src="https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=slack&logoColor=white" alt="Slack"/>
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white" alt="Zod"/>
</p>



---

### UPM USA: Matching Platform (SIC-VeriATS V1 > V2)

> [V1 is public with full post-mortem](https://github.com/sergioillescascabiro/SIC-VeriATS) | V2 is currently in use internally by UPM USA

**The Context:** As part of my engineering work for UPM USA, I built the internal Applicant Tracking System for our annual Career Fair. The fair operates strictly on pre-scheduled interviews, requiring a robust matching process between 15 hiring companies (a record number) and 100 engineering students who are currently completing their Dual Degree programs in the US.

Built V1 as a fast MVP, then wrote an honest post-mortem documenting three architectural failures (dual auth system, schema governance collapse, zero automated tests). Threw away the codebase and rebuilt V2 with every lesson applied: unified JWT auth, 5-service Docker Compose architecture, screener role, interview scheduling, matching engine, and MinIO for document storage.

<table>
<tr>
<td width="50%">

**V1 - What went wrong**

- Dual auth: Supabase Auth + independent JWTs
- Two competing schema sources (SQL vs Alembic)
- Zero tests, debug scaffolding in main

</td>
<td width="50%">

**V2 - Production-grade rebuild**

- Single JWT auth with 4-role RBAC
- Async SQLAlchemy 2.0 + Alembic as single source
- 5-service containerized architecture

</td>
</tr>
</table>

<p>
  <img src="https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/PostgreSQL_16-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/SQLAlchemy_2.0-D71F00?style=flat-square" alt="SQLAlchemy"/>
  <img src="https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white" alt="MinIO"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" alt="Nginx"/>
  <img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
</p>

---

### UPM USA: AI Candidate Support Agent

**The Problem Solved:** Managing a cohort of 100 students completing their Dual Degree programs in the US generates an overwhelming volume of repetitive questions regarding visa status, event logistics, and administrative procedures. Instead of answering them manually, I built an interactive conversational AI that guides students 24/7 using our internal knowledge base (Notion docs, FAQs, and historical data).

RAG-powered conversational agent built on a LangGraph StateGraph that routes queries through three tools: two ChromaDB collections (visas/logistics and company profiles) and Tavily for live web search. Dual-LLM setup with automatic fallback (Groq Llama 3 primary, Vertex AI fallback). Custom ingestion pipeline to chunk and embed Notion documents, schedules, and FAQ into ChromaDB with ONNX embeddings.

**Key challenges:** Designing a tool-routing agent that searches local vector databases before hitting the web | Ingesting heterogeneous historical data from Notion and past manuals | Vertex AI fallback chain for rate limit resilience | Bilingual system prompt (Spanish/English)

<p>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph"/>
  <img src="https://img.shields.io/badge/ChromaDB-FF6F61?style=flat-square" alt="ChromaDB"/>
  <img src="https://img.shields.io/badge/Tavily-1C3C3C?style=flat-square" alt="Tavily"/>
  <img src="https://img.shields.io/badge/Groq-F55036?style=flat-square" alt="Groq"/>
  <img src="https://img.shields.io/badge/Vertex_AI-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="Vertex AI"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
</p>


---

### QuercusHealth

> [Public repo](https://github.com/sergioillescascabiro/QuercusHealth-Public)

Deep learning platform to detect *La Seca* disease across Spain's 5M-hectare Dehesa ecosystem via satellite imagery. Adapting DeepForest (RetinaNet + ResNet-50) from North American aerial data to Mediterranean satellite imagery at 0.15m/px. Custom data acquisition pipeline, 210+ annotated trees across 14 tiles, temporal cross-referencing to confirm mortality vs seasonal variation.

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/DeepForest-228B22?style=flat-square" alt="DeepForest"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/Roboflow-6706CE?style=flat-square" alt="Roboflow"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white" alt="Jupyter"/>
</p>

---

## Tech Stack

<table>
<tr>
<td valign="top" width="33%">

**Core Engineering**

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
</p>

</td>
<td valign="top" width="33%">

**AI / ML**

<p>
  <img src="https://img.shields.io/badge/Vertex_AI-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="Vertex AI"/>
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph"/>
  <img src="https://img.shields.io/badge/LiveKit-000000?style=flat-square&logo=webrtc&logoColor=white" alt="LiveKit"/>
  <img src="https://img.shields.io/badge/ChromaDB-FF6F61?style=flat-square" alt="ChromaDB"/>
  <img src="https://img.shields.io/badge/Tavily-1C3C3C?style=flat-square" alt="Tavily"/>
  <img src="https://img.shields.io/badge/ElevenLabs-000000?style=flat-square" alt="ElevenLabs"/>
  <img src="https://img.shields.io/badge/Vapi.ai-5046E5?style=flat-square" alt="Vapi"/>
</p>

</td>
<td valign="top" width="33%">

**Infrastructure**

<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="GCP"/>
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" alt="Nginx"/>
  <img src="https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white" alt="MinIO"/>
  <img src="https://img.shields.io/badge/Make.com-6D00CC?style=flat-square" alt="Make"/>
</p>

</td>
</tr>
</table>

---

## Engineering Philosophy

| | |
|---|---|
| **Product-first engineering** | Every technical decision starts with "what does the user need?" |
| **Architecture through iteration** | Build the MVP, ship it, write the post-mortem, rebuild it right |
| **Full ownership** | From prompt engineering to Dockerfile to deployment |
| **Ship, then scale** | Working prototype today, production-grade architecture tomorrow |

---

<p align="center">
  <em>Based in Chicago, IL. Open to high-impact engineering roles where I can own problems end-to-end.</em>
</p>
