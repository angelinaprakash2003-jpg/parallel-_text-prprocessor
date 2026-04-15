

🚨 *Parallel Text Handling Processor*  
*Disaster & Crisis Communication Monitor*  
_Infosys Springboard Project_

📌 *Overview*  
A dual-stream text analysis engine built with Python that handles disaster-related content from social media (tweets) and messaging apps (WhatsApp chats) at the same time to derive actionable insights in almost real time.

In major disasters such as the *Kerala Floods (2018)* or the *Turkey-Syria Earthquake (2023)*, millions of messages arrive within just a few hours. This system is built to analyze both data streams in parallel, enabling quicker, data-driven deployment of relief efforts.

---

⚡ *Key Features*  
- 🔄 *Parallel Processing* – Leverages `ProcessPoolExecutor` to distribute data processing across multiple CPU cores concurrently  
- 📊 *Dual-Stream Analysis* – Handles tweets and WhatsApp messages simultaneously  
- 🔍 *Rule Engine* – 7 regex-driven crisis categories (distress calls, disaster types, resources, etc.)  
- 🧹 *Real-Time Cleaning Preview* – Visualizes text cleaning steps one by one  
- 📡 *Real-Time CSV Analysis* – Upload any CSV to immediately receive alert classifications  
- 💾 *SQLite Storage* – All processed outputs are saved to a local database  
- 📈 *Streamlit Dashboard* – Offers interactive charts, word clouds, and sentiment analysis  

---

📦 *Project Structure*
parallel_text_processor/
│
├── main.py              # Entry point
├── preprocessing.py     # Text cleaning
├── processor.py         # Parallel processing logic
├── aggregator.py        # Merge results
├── rule_engine.py       # Regex rules
├── output_generator.py  # Create CSV/DB outputs
├── dashboard.py         # Streamlit UI
│
├── data/
│   ├── tweets/          # Crisis tweets dataset
│   └── whatsapp/        # WhatsApp chat dataset
│
└── output/              # Generated results
📦 *Datasets Used*
Dataset	Source	Description
CrisisLexT26	CrisisNLP	27,000+ annotated tweets covering 26 global disaster events
WhatsApp Chat	Kaggle	Community-level messaging dataset simulating crisis communication
🛠️ *Installation*
Clone the repository
git clone https://github.com/Serg...
cd ParallelTextProcessor

Set up virtual environment
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # Mac/Linux

Install required packages
pip install -r requirements.txt
🚀 *How to Run*  
*Step 1 – Execute the pipeline (processes datasets, creates outputs)*
python main.py
*Step 2 – Start the dashboard*
streamlit run dashboard.py
📊 *Dashboard Tabs*
Tab	Description
📡 Real-Time Analysis	Upload CSV or input text → get instant alert classification
🐦 Tweets	Displays keywords, word cloud, sentiment, rule engine charts
💬 WhatsApp	Shows keywords, active senders, word cloud, sentiment
🔍 Rule Engine	Regex patterns, CSV outputs, SQLite DB preview
🔍 *Rule Engine Categories*
Rule	Keywords
`distress_signals`	help, trapped, rescue, sos, urgent, missing, emergency
---

