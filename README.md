# 🎯 SkillSprint AI
**Resource-Aware Semantic Job Matching & Curriculum Engine**

*Built for the USAII Global AI Hackathon 2026*

## 📌 The Problem
Engineering students often struggle to translate academic coursework into industry-ready skills. Standard matching algorithms rely on brittle keyword filters, and generic coding bootcamps ignore the physical constraints of a student's reality (heavy lab schedules, lack of cloud GPUs, or access to specific hardware).

## 💡 The Solution
SkillSprint AI is an intelligent, resource-aware career bridging platform. It doesn't just score a candidate against a job description; it acts as an autonomous career coach. 

By taking into account a student's weekly availability, academic load, and physical hardware resources, it generates a highly personalized, complexity-weighted 14-week learning sprint to close the exact semantic skill gaps standing between them and their target role.

## 🚀 Key Features
* **Hybrid Matching Engine:** Filters opportunities using hard structural metadata (domain, experience level) before applying soft semantic vector matching.
* **Semantic Skill Gap Analysis:** Utilizes NLP (`all-MiniLM-L6-v2`) to recognize conceptual skill overlaps (e.g., matching "React (Basic)" to a "React" requirement) rather than failing on rigid string subtractions.
* **Resource-Aware Curriculum:** Dynamically alters the 14-week sprint based on physical constraints. If a student owns an ESP32 board, the AI shifts theoretical IoT modules into bare-metal hardware debugging. 
* **Responsible AI Guardrails:** Built-in confidence thresholds prevent the system from hallucinating career paths; if a profile falls below a 40% match affinity, the timeline engine suspends execution and advises foundational bridging.

## 🧠 Technical Architecture
* **Frontend UI:** Streamlit
* **Language Models:** Hugging Face `SentenceTransformers` (`all-MiniLM-L6-v2`)
* **Data Processing:** Pandas, NumPy
* **Vector Math:** Scikit-Learn (Cosine Similarity)
* **Visualization:** Plotly Express

*Note: For the purposes of evaluating this MVP while adhering to strict data privacy and PII protection standards, all student profiles and job requirement datasets used in this repository are synthetic.*

## ⚙️ How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Punya22/SkillSprint-AI.git](https://github.com/Punya22/SkillSprint-AI.git)
   cd SkillSprint-AI
2. **Install Dependencies:**
pip install -r requirements.txt
3. **Launch the application:**
streamlit run app.py
**The application will automatically open in your default web browser**
