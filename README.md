# Hi, I'm Arnav Shahi

B.Tech AIML student at Symbiosis Institute of Technology, Indore, and Data Analyst Intern at Encode AI. I build things that work in the real world: a live AI chatbot, an automated AI resume screener, a secured IoT system, a live tournament website, a company ID checker and a campus resource exchange.

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

### ReLoop: Circular Resource Exchange for Campuses
One platform for a college's used oil, e-waste and rooftop rainwater, with a single dashboard for revenue, compliance and impact.
- Oil Exchange: departments list used oil by type and grade, get a suggested price, and only FSSAI-licensed buyers can bid
- E-Waste Market: each item is triaged to resell, repair, donate or recycle, sold to CPCB-registered recyclers and verified buyers
- Rainwater: harvest potential and required tank size per building from roof area and rainfall
- Pickup scheduling with verification on arrival, auto-generated FSSAI and CPCB compliance certificates, and monthly CSR/ESG reports (PDF and CSV)

**Tech:** Next.js, React, TypeScript, PostgreSQL, Tailwind CSS, Vercel
[Live Demo](https://reloop-tan.vercel.app) | [Code](https://github.com/arnav2293-afk/reloop)

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

### CIN & LLPIN Checker
Paste a list of Indian company IDs (CINs) and LLP IDs (LLPINs) and see which are valid, exactly what is wrong with the rest, and what each one means.
- Plain-English errors that name the characters at fault, plus one-click fixes for common typos (letter O for zero, `OD` for `OR`)
- Amber warnings when the format is valid but breaks company law, such as a listed one-person company (Companies Act 2013)
- Handles 5,000 IDs per check, with summary tiles, filters, problems sorted first and Excel-safe CSV export
- 32 unit tests, dark mode, phone layout and WCAG AA contrast, with no build step or dependencies

**Tech:** JavaScript, HTML, CSS, Node test runner, Figma, GitHub Pages
[Live Site](https://arnav2293-afk.github.io/cin-llpin-checker/) | [Code](https://github.com/arnav2293-afk/cin-llpin-checker)

### QR Code Attendance Mobile App
No-code mobile app built with Google AppSheet and a QR Code API, with live Google Sheets sync. Cut attendance marking for a 40+ student class from 5+ minutes to under 30 seconds.

## Skills

**Languages and Databases:** C, C++, Python, JavaScript, TypeScript, MySQL (CREATE, ALTER, INSERT, UPDATE, SELECT), Firebase Firestore
**Web and Tools:** React, Next.js, Tailwind CSS, PostgreSQL, Streamlit, REST APIs, n8n, Docker, Git, GitHub Actions, Figma
**Security and Networking:** Password hashing, TLS, X.509 certificates, access control, MQTT, Wireshark
**AI and Data:** RAG, LLM APIs, FAISS, scikit-learn, pandas, NumPy, Power BI, Matplotlib, Seaborn

## Contact

Email: arnav2293@gmail.com
LinkedIn: [www.linkedin.com/in/arnav-shahi-b7a787369](https://www.linkedin.com/in/arnav-shahi-b7a787369)
