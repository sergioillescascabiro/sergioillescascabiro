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

Computer & AI Engineer with a dual Master's (UPM Madrid + IIT Chicago). I started in telecom engineering and enterprise systems (Java/Spring Boot, OpenShift, Kubernetes at Minsait/Indra), where I learned what production-grade means under real SLAs.

That foundation pushed me toward AI-native products. Today I design multi-agent voice systems, build RAG pipelines from multiple sources, and ship platforms where architecture follows user needs. I build fast, break things deliberately, document what went wrong, and rebuild better.

---

## Missions

### Ace Interviewer / InterviewOS

> **Overall Winner + Best Use of Gemini API** - Hack-a-Job Hackathon

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

Voice-first AI booking assistant for a barbershop. Vertex AI (Gemini 1.5 Flash) with Function Calling queries Google Calendar in real-time to verify availability before confirming any slot. Remembers recurring clients via SQLite for contextual upselling. Handles Spanish, English, and French with culturally adapted tone. Full automation pipeline: voice call > AI conversation > calendar check > booking > Make.com webhook > notification.

**Key challenges:** Function Calling for live calendar availability | Client memory + intelligent upselling based on visit history | Multilingual prompt engineering with Deepgram Nova-2 auto-detection | End-to-end automation from voice to notification

<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express"/>
  <img src="https://img.shields.io/badge/Vertex_AI-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="Vertex AI"/>
  <img src="https://img.shields.io/badge/Gemini_1.5_Flash-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/Vapi.ai-5046E5?style=flat-square" alt="Vapi"/>
  <img src="https://img.shields.io/badge/ElevenLabs-000000?style=flat-square" alt="ElevenLabs"/>
  <img src="https://img.shields.io/badge/Google_Calendar-4285F4?style=flat-square&logo=googlecalendar&logoColor=white" alt="Google Calendar"/>
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"/>
  <img src="https://img.shields.io/badge/Make.com-6D00CC?style=flat-square" alt="Make"/>
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white" alt="Zod"/>
</p>

---

### SIC-VeriATS: V1 > V2

> [V1 is public with full post-mortem](https://github.com/sergioillescascabiro/SIC-VeriATS)

Blind recruitment platform for university job fairs. Built V1 as a fast MVP, then wrote an honest post-mortem documenting three architectural failures (dual auth system, schema governance collapse, zero automated tests). Threw away the codebase and rebuilt V2 with every lesson applied: unified JWT auth, 5-service Docker Compose architecture, screener role, interview scheduling, matching engine, and MinIO for document storage.

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
