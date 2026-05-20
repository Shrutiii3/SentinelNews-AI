# 🛡️ SentinelNews AI
**An Autonomous, Cross-Lingual News Auditing Framework**

SentinelNews is a multi-agent AI pipeline designed to systematically mitigate misinformation and hidden political bias in digital media. It utilizes an agentic workflow to scrape live news, verify core claims against professional journalist databases, and dynamically rewrite heavily biased articles into neutral, AP-style text.

![Project Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Gemini](https://img.shields.io/badge/Google_Gemini-3.1_Flash--Lite-orange)

---

## 🚀 Key Features
* **Multi-Agent Architecture:** Utilizes a Planner Agent to orchestrate sequential tasks and an Executor Agent for advanced LLM computations.
* **Live Fact-Checking:** Integrates the `factcheckexplorer` library to validate core claims against live databases of verified journalists.
* **Cross-Lingual Auditing:** Normalizes regional Hindi news into English using `deep-translator` before submitting text for LLM analysis.
* **Bias Detection & Mitigation:** Scores political and emotional bias (0-100 scale) and generates fact-based, neutralized rewrites.
* **Built-in Fault Tolerance:** Handles API rate limits (429/503 errors) with automatic retries and exponential backoff to prevent pipeline crashes.

---

## 📸 Dashboard Preview


> **Live Feed & Scraping**
> 
> <img width="2552" height="1164" alt="SentinelNews1" src="https://github.com/user-attachments/assets/cc15ab1f-ca8a-4b59-8266-8c82ebee7a08" />


> **Manual Audit & Neutral Rewrite**
> 
> <img width="2560" height="1172" alt="SentinelNews2" src="https://github.com/user-attachments/assets/1bf975ba-ebdb-45bf-9fcb-33c5a12c4bb4" />

---

## 🛠️ Tech Stack & Microservices
* **LLM Orchestration:** Google Gemini 3.1 Flash-Lite API
* **Frontend UI:** Streamlit, Plotly, Pandas
* **Data Extraction:** BeautifulSoup, feedparser, requests
* **Translation Module:** deep-translator
* **Fact-Checking Module:** factcheckexplorer (Google Fact Check Tools API)

---

## 💻 How to Run (Google Colab)
This project is optimized to run seamlessly in Google Colab, utilizing Streamlit and a Cloudflare Tunnel to serve the web UI securely without exposing API keys.

### Prerequisites
1. A Google Account (for Google Colab).
2. A free [Google Gemini API Key](https://aistudio.google.com/).

### Setup Instructions
1. Open the `SentinelNews_AI.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. Click on the **🔑 Secrets** icon on the left sidebar.
3. Add a new secret with the Name: `GEMINI_API_KEY` and paste your API key in the Value field.
4. **Crucial:** Toggle the button to enable **Notebook access** for the secret.
5. Go to the top menu and click **Runtime > Run all**.
6. Scroll to the bottom of the output in the final cell. You will see a Cloudflare Tunnel link generated (e.g., `https://random-words.trycloudflare.com`).
7. Click that link to open your live SentinelNews Enterprise dashboard!

