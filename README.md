# AutoForceAI (Digital Employee Platform)

[English](README.md) | [中文](README_CN.md)

> **"Empower Every Enterprise with Intelligent Digital Workforce"**
>
> **"Not just Digital Employees, but your Automated Business Empire"**

**AutoForceAI** 思渡AI (sdosoft.com) is an **AI-native, full-stack, enterprise-grade** digital employees platform. Even without deep AI development background, you can use this project to build a complete AI business intelligence system **out of the box**.

It is more than just a simple Agent framework; it is a comprehensive solution that deeply integrates **Large Language Models (LLM)**, **Robotic Process Automation (RPA)**, **Enterprise Knowledge Brain (RAG)**, and **Business Systems (BI/ERP/CRM)**. By simulating the learning, thinking, and executing capabilities of human employees, AutoForceAI helps enterprises achieve an **AI-driven closed loop of automated business processes**.

## 🌟 Product Matrix

This project delivers a complete AI business solution, covering the full spectrum from infrastructure to application layer:

-   **🧠 AI Middle Platform**: Unified model orchestration, plugin management, and knowledge engine.
-   **📚 AI Knowledge Base**: Enterprise Knowledge Brain & Q&A system based on RAG technology, supporting solution generation.
-   **🤖 Digital Employee**: Autonomous agents capable of planning and executing complex tasks via RPA.
-   **👤 Digital Human**: High-fidelity 3D/2D avatars for video generation and live streaming.
-   **🛍️ AI eCommerce**: AI-driven e-commerce system including product management, design, image generation, copywriting, order processing, and QC.
-   **💹 AI Marketing**: Full-link marketing automation platform integrating short video creation, text-to-image, and image-to-video.
-   **🤝 AI Customer Service**: 24/7 intelligent reception with multi-turn dialogue and intent recognition.
-   **👥 AI CRM**: Intelligent customer relationship management with auto-profiling and lead scoring.
-   **🔍 GEO (Generative Engine Optimization)**: Content optimization system for generative answer engines.

### Core Modules

-   **Multimodal Brain**: Core cognitive engine (`digital-brain`) deeply integrating leading models like **DeepSeek, Qwen, Doubao, OpenAI, Seedance2.0, Runway**.
-   **RPA Workers**: Distributed execution units (`rpa-worker`) that automate browser tasks like content posting and data gathering.
-   **Unified Console**: Full-featured admin dashboard (`apps/web-console`) including CRM, Order Management, and Digital Human configuration.
-   **AI Mall**: A complete commercial marketplace for AI skills and templates (`apps/ai-mall`).
-   **Official Landing**: Production-ready product showcase site (`apps/official-site`).
-   **E-commerce Core**: Built-in product and order management backend (`services/ecommerce-core`).

## � Screenshots

<div align="center">
  <p><strong>Enterprise Brain Dashboard</strong></p>
  <img src="docs/screenshots/qydn.png" alt="Enterprise Brain - qydn.png" width="800"/>
</div>

<div align="center">
  <p><strong>Intelligent Knowledge Base & RAG Engine</strong></p>
  <img src="docs/screenshots/kb.png" alt="Knowledge Base - kb.png" width="800"/>
</div>

<div align="center">
  <p><strong>AI Customer Service Expert</strong></p>
  <img src="docs/screenshots/kfzj.png" alt="Customer Service Expert - kfzj.png" width="800"/>
</div>

<div align="center">
  <p><strong>GEO Traffic Engine</strong></p>
  <img src="docs/screenshots/geo.png" alt="GEO Engine - geo.png" width="800"/>
</div>

<div align="center">
  <p><strong>Product Matrix</strong></p>
  <img src="docs/screenshots/cp.png" alt="Digital Employee Product Matrix - cp.png" width="800"/>
</div>

## �📊 Editions & Comparison

AutoForceAI adopts a **"Core Open Source + Commercial Enhancement"** dual-model strategy. While our long-term vision is full open source, to ensure sustainable development and meet enterprise needs, we will gradually release high-value modules to the Community Edition.

| Modules | Community Edition <br> *AutoForceAI* | Professional Edition <br> *Powered by SDOSOFT* |
| :--- | :--- | :--- |
| **Infrastructure** | ✅ Full Standalone/Docker | ✅ HA Cluster / K8s Operator |
| **🧠 AI Middle Platform** | ✅ Multi-Model / Basic RAG | ✅ Enterprise RAG (Complex Parsing / Hybrid Search) / Audit Logs |
| **📚 AI Knowledge Base** | ✅ Text/PDF/Markdown Parsing | ✅ Enterprise Knowledge Brain / Solution Generation / Knowledge Graph |
| **🔍 GEO** | ✅ Basic Content Optimization / Keyword Analysis | ✅ Multi-Engine Ranking Monitor / Auto-Optimization / Competitor Analysis |
| **🤝 AI Customer Service** | ✅ Text Chat / Intent Recognition | ✅ Voice/Phone Integration (ASR/TTS) / Human Handover |
| **💹 AI Marketing** | ✅ Basic Text/Image Gen | ✅ Short Video Creation / Product Design (T2I/I2V) / Matrix Auto-Posting |
| **🛍️ AI E-commerce** | ✅ Product/Order Mgmt | ✅ Multi-Platform ERP Sync / Competitor Monitoring / Intelligent Selection |
| **👥 CRM** | ✅ Customer Profile / History | ✅ Lead Scoring / Mining / Sales SOP Automation |
| **👤 Digital Human** | ✅ 2D Basic Avatar | ✅ High-Fidelity 3D Interactive / Real-time Streaming |
| **🤖 Digital Employee (Agent)** | ✅ Local Execution / Basic Workflow | ✅ Cloud Cluster Scheduling / Human-like Behavior Simulation / Complex Verification Handling |
| **Support** | Community (GitHub Issues) | Dedicated Manager / 7x24h SLA / Private Customization |

> 💡 **The Community Edition currently includes the core business scenarios mentioned above**, allowing you to build a complete commercial system. The Professional Edition focuses on enhancements for **mass scale**, **complex integration**, and **high-value vertical scenarios**.

## 🏗️ Architecture Stack

The system is composed of five main planes:

1.  **Control Plane**: `apps/web-console` (Next.js 14, React, Tailwind CSS) - *Includes CRM, Marketing, & Ops modules.*
2.  **Data Plane**: `services/digital-brain` (FastAPI, Python 3.10+, PostgreSQL/SQLite)
3.  **Execution Plane**: `services/rpa-worker` (Python, Selenium/Playwright)
4.  **Business Plane**: `services/ecommerce-core` (FastAPI, SQLAlchemy) - *Handles products & orders.*
5.  **Traffic Plane**: `apps/official-site` & `apps/ai-mall` (Next.js, React, Tailwind CSS)

## 🚀 Getting Started

### Prerequisites

- **Python**: 3.10+
- **Node.js**: 18+ (LTS recommended)
- **Database**: PostgreSQL (Production) or SQLite (Dev default)
- **Redis**: Recommended for task queues

### Installation Guide

#### 1. Setup Backend (Digital Brain)
```bash
cd services/digital-brain
# Create virtual environment (recommended)
python -m venv venv
# Activate: .\venv\Scripts\Activate (Windows) or source venv/bin/activate (Linux/Mac)

pip install -r requirements.txt

# Configure Environment
cp .env.example .env
# Edit .env with your API keys and DB details

# Run Server
python server.py
# API will be available at http://localhost:8002/docs
```

#### 2. Setup Frontend (Web Console)
```bash
cd apps/web-console
npm install

# Configure Environment
cp .env.example .env.local

# Run Development Server
npm run dev
# Dashboard at http://localhost:3000
```

#### 3. Setup RPA Worker (Optional)
Required only if you plan to run browser automation tasks.
```bash
cd services/rpa-worker
pip install -r requirements.txt
cp .env.example .env
python worker_main.py
```

## � Quick Start

### 1. Create Enterprise & Invite Members
- **Create Enterprise**: After first login, go to **Organization Management** -> **Enterprise Settings**, click "Create New Enterprise" and enter the name. The system will auto-generate the default structure.
- **Invite Members**: In **Organization Management** -> **Member List**, click "Invite Member" at the top right. Copy the link or code and send it to your colleagues. They can join your workspace after registration.

### 2. Configure AI Middle Platform (LLM API Keys)
To enable the Digital Brain to think, you need to configure the LLM API Keys:
1. Navigate to **AI Middle Platform** -> **Model Management**.
2. Click "Add Model Provider" and select your provider (e.g., DeepSeek, ZhipuAI, OpenAI, Qwen).
3. Enter the `API Key` and enable the service.
4. Set the model as the **System Default Reasoning Engine** in "Default Model Settings".

## �📂 Project Structure

```
├── apps/                   # Frontend Applications
│   ├── web-console/        # Management Console (Full Enterprise Edition)
│   ├── ai-mall/            # AI Marketplace
│   ├── official-site/      # Official Landing Page
│   └── ...                 # More Application Modules
├── services/               # Backend Services
│   ├── digital-brain/      # Core AI Engine & Logic
│   ├── rpa-worker/         # Automation Agents
│   ├── ecommerce-core/     # E-commerce Core Backend
│   └── ...                 # More Microservices
├── scripts/                # Maintenance & Tool Scripts
└── docs/                   # Documentation
```

## 🤝 Contributor Guide (CLA)

We welcome contributions from the community! To ensure the project's long-term development and legal compliance, all code contributors must agree to the following **Contributor License Agreement (CLA)**:

1.  **Copyright Grant**: You agree to grant the project maintainers (**SDOSOFT AI Team**) the right to use, modify, and distribute your contributed code.
2.  **Protocol Adjustment**: You authorize the project maintainers to adjust the open-source license in future versions (e.g., changing to a more permissive or stricter license).
3.  **Commercial Use**: You explicitly allow your contributions to be included in commercial products or cloud services provided by the project maintainers.

Submitting a Pull Request is considered as your agreement to the above terms.

Detailed guidelines can be found in [CONTRIBUTING.md](CONTRIBUTING.md).

## 🙏 Acknowledgments

AutoForceAI is built on the shoulders of giants. Special thanks to these amazing open-source projects:
- [LangChain](https://github.com/langchain-ai/langchain)
- [FastAPI](https://github.com/tiangolo/fastapi)
- [Next.js](https://github.com/vercel/next.js)
- [Playwright](https://github.com/microsoft/playwright)

## 📞 Contact & Communication

- **Commercial Cooperation / Custom Development**: Please contact author email `andylin@sdosoft.com`
- **Issue Feedback**: Please prefer [GitHub Issues](../../issues) for archiving and helping others.
- **Technical Group**: Scan the QR code to join WeChat group (Please email if expired).

<img src="docs/screenshots/wechat_group.jpg" alt="WeChat Group" width="200" />

## ⚠️ Disclaimer

- This project is for learning, research, and legal commercial use only. Do not use this project for any illegal purposes (such as cyber attacks, fraud, etc.).
- The user assumes all consequences (including but not limited to data loss, legal disputes) arising from the use of this project, and the open-source author assumes no responsibility.
- The use of third-party models (such as OpenAI, DeepSeek, etc.) involved in this project must comply with the service terms of each provider.

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**.

- **AutoForceAI** is an open-source project initiated and maintained by **[SDOSOFT (思渡AI)](https://www.sdosoft.com)**.
- If you **modify** or **secondary develop** this project and use it for **online services** (i.e., providing software functionality via a network), you must **open source your complete source code** in accordance with the AGPL-3.0 agreement.
- For full license text, please refer to the [LICENSE](LICENSE) file.
