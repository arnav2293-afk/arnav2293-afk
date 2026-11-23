# Hi, I'm Arnav Shahi

B.Tech AIML and Data Science student at Symbiosis Institute of Technology, Indore, and Data Analyst Intern at Encode AI. I build things that work in the real world: a live AI chatbot, an automated AI resume screener, a secured IoT system and a live tournament website.

## Projects

### Ask Your PDF: RAG Chatbot with Page Citations
Upload a PDF, ask questions, and get answers with page-level citations.
- Hybrid search (FAISS + BM25 with Reciprocal Rank Fusion): **100% hit rate@5 and 0.882 MRR** on 42 hand-verified questions
- LLM failover across Groq and Gemini with timeouts, retries and a circuit breaker, so the app keeps answering during outages
- API keys kept out of code with Streamlit secrets and .gitignore

**Tech:** Python, FAISS, BM25, sentence-transformers, Groq and Gemini APIs, Streamlit
[Live Demo](https://ask-your-pdf-arnav.streamlit.app) | [Code](https://github.com/arnav2293-afk/ask-your-pdf-rag)

### AI Resume Screener: Automated n8n Workflow
Email a PDF resume and it is scored against a job description and logged to Google Sheets automatically.
- n8n pipeline: Gmail trigger, PDF text extraction, LLM scoring and Google Sheets logging
- The LLM returns strict JSON (score 0–100, summary, top and missing skills, Shortlist / Maybe / Reject), and a Code node validates it and flags bad replies as `NEEDS MANUAL REVIEW`
- Append-or-update matched on email, so a candidate who applies twice still gets one row
- Runs on Gemini's free tier, with a ready Claude API version that shares the same prompt and parsing code

**Tech:** n8n, Python, Gemini and Claude APIs, Gmail, Google Sheets
[Code](https://github.com/arnav2293-afk/ai-resume-screener)

### Securing an IoT Sensor on MQTT
A simulated temperature sensor sends readings to an MQTT broker. I proved in Wireshark that the open setup leaked data and passwords, then locked it down step by step.
- Open broker on port 1883: readings and password visible in plain text
- Hashed passwords, TLS 1.2+ on port 8883 and X.509 certificates: only encrypted data visible
- Least-privilege access rules: 4/4 automated checks pass
- Audited against a 17-point GDPR checklist

**Tech:** Python, paho-mqtt, Eclipse Mosquitto, Docker, Wireshark, TLS
[Code](https://github.com/arnav2293-afk/mqtt-iot-security)

### pickle.rizz.rally: Live Tournament Website
Players register and follow live scores and brackets on their phones.
- TypeScript scheduling engine: snake seeding, round-robin fixtures and a court packer with zero back-to-back games
- Organiser login with Firebase Authentication, and Firestore rules that keep player phone numbers private
- Firestore transactions so several organisers can enter scores at once without overwriting each other

**Tech:** React, TypeScript, Tailwind CSS, Firebase, GitHub Actions, GitHub Pages
[Live Site](https://picklerizzrally.github.io/)

### QR Code Attendance Mobile App
No-code mobile app built with Google AppSheet and a QR Code API, with live Google Sheets sync. Cut attendance marking for a 40+ student class from 5+ minutes to under 30 seconds.

## Skills

**Languages and Databases:** C, C++, Python, TypeScript, MySQL (CREATE, ALTER, INSERT, UPDATE, SELECT), Firebase Firestore
**Web and Tools:** React, Tailwind CSS, Streamlit, REST APIs, n8n, Docker, Git, GitHub Actions
**Security and Networking:** Password hashing, TLS, X.509 certificates, access control, MQTT, Wireshark
**AI and Data:** RAG, LLM APIs, FAISS, scikit-learn, pandas, NumPy, Power BI, Matplotlib, Seaborn

## Contact

Email: arnav2293@gmail.com
LinkedIn: [www.linkedin.com/in/arnav-shahi-b7a787369](https://www.linkedin.com/in/arnav-shahi-b7a787369)
