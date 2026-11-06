# 🎙️ Hotel-Voice-Agent-Customer-Support-Elavenlabs-n8n

![n8n](https://img.shields.io/badge/Workflow-n8n-FF6C37?style=flat&logo=n8n&logoColor=white)
![ElevenLabs](https://img.shields.io/badge/Voice-ElevenLabs-black?style=flat&logo=elevenlabs&logoColor=white)
![OpenAI](https://img.shields.io/badge/AI-GPT--4o-412991?style=flat&logo=openai&logoColor=white)
![Pinecone](https://img.shields.io/badge/Database-Pinecone-262730?style=flat&logo=pinecone&logoColor=white)
![Google Drive](https://img.shields.io/badge/Source-Google_Drive-4285F4?style=flat&logo=googledrive&logoColor=white)

---

## 🚀 The Solution: Autonomous Guest Intelligence
This project features a **Fully Autonomous AI Voice Agent** specifically engineered for the **Lake View Hotel**. It addresses the challenge of scaling customer support by providing a 24/7, human-like voice interface capable of handling complex guest inquiries. 

The agent manages real-time conversations regarding room reservations, seasonal pricing, hotel amenities, and stay policies. By utilizing a **Retrieval-Augmented Generation (RAG)** architecture, the system ensures all verbal responses are derived from the hotel's official knowledge base, providing accurate and reliable information without human intervention.

---

## ✅ Problems Solved
- **Eliminating Wait Times:** Guests no longer need to wait for a front-desk operator for basic information or reservation queries.
- **Consistency in Support:** Every guest receives the same high-quality, polite, and accurate information regardless of the time of day.
- **Automated Knowledge Sync:** When hotel policies or room prices change in the master Google Doc, the Voice AI updates its knowledge automatically via the ingestion pipeline, ensuring it never gives outdated information.

---

## 🖼️ System Architecture

### 1. Conversational Voice Pipeline (ElevenLabs + n8n)
The core interaction engine where voice input is processed, analyzed, and answered in real-time.
<div align="center">
  <img src="images/n8n-voice-agent-overview.jpeg" width="100%" alt="n8n Voice Agent Architecture" style="border-radius:10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);"/>
</div>

### 2. Knowledge Ingestion & Vectorization (Data Pipeline)
The backend process that syncs the Lake View Hotel's documentation with the AI's long-term vector memory.
<div align="center">
  <img src="images/n8n-info-loader-overview.jpeg" width="100%" alt="n8n Info Loader Architecture" style="border-radius:10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);"/>
</div>

---

## 🧠 Core Technical Pillars

### 1. 🗣️ High-Fidelity Voice Synthesis (ElevenLabs)
The system utilizes **ElevenLabs** for industry-leading voice quality. It doesn't just read text; it understands the emotional context of the guest's question. When a query requires specific hotel data, the ElevenLabs agent triggers a custom **n8n tool**, bridging the gap between natural conversation and structured data retrieval.

### 2. 🔍 RAG-Driven Intelligence (Pinecone Vector DB)
To ensure the agent provides specific details about the **Lake View Hotel** (and not generic AI guesses), it uses **Retrieval-Augmented Generation**:
- **Semantic Search:** The agent converts guest questions into vectors to find the most relevant information in the **Pinecone** database.
- **Fact-Grounded Responses:** The AI only answers based on the retrieved data, eliminating "hallucinations."

### 3. 🔄 Recursive Knowledge Sync (Google Drive Ingestion)
The "Info Loader" workflow automates the maintenance of the hotel's knowledge base. It pulls the latest guidelines and rates from **Google Drive**, processes the text through a **Recursive Character Splitter**, and updates the vector embeddings via **OpenAI**. 

### 4. 🧠 Agentic Reasoning (GPT-4o Controller)
Inside the n8n ecosystem, the **AI Agent Node** (powered by GPT-4o) acts as the brain. It evaluates the guest's request, decides which database tools to call, and formats the technical findings into a warm, hospitable, and concise verbal response.

---

## 🛠️ Technical Stack
| Layer | Technology |
| :--- | :--- |
| **🔄 Automation** | n8n (State Management & API Orchestration) |
| **🎙️ Voice Interface** | ElevenLabs (Conversational Voice AI) |
| **🧠 AI Brain** | OpenAI GPT-4o (Reasoning & Embeddings) |
| **💾 Vector Store** | Pinecone (High-speed Semantic Search) |
| **📂 Source Data** | Google Drive (Dynamic Knowledge Base) |

---

## ✍️ Author
**Muneeb Ali Khan**
- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)

---

## 📜 License
This project is licensed under the MIT License.
