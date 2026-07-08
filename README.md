---

## 📊 Dataset

| File | Description |
|------|-------------|
| historical_win.csv | World Cup finals history 1930–2022 (Champion, Runner-Up, Top Scorer, Attendance, Goals) |
| team_stats.csv | Team performance stats per tournament (wins, losses, draws, goals, rankings, squad value) |
| fixtures_2026.csv | 2026 World Cup match schedule (teams, stages, stadiums, dates) |

> **Note:** Several data gaps in the original Kaggle datasets were identified and corrected by cross-referencing verified historical World Cup records — including missing final appearances for Argentina (1930, 1990) and Brazil (1950).

---

## 🚧 Challenges & Solutions

| Challenge | Solution |
|-----------|----------|
| Kaggle dataset missing World Cup finals (1930, 1950, 1990, 2006) | Manually researched and added correct historical rows via Power Query Append |
| DAX measures showing inflated numbers | Discovered duplicate rows per team per year — fixed using MAX aggregation and new calculated columns |
| Power Query "Replace Values" changing entire column instead of one row | Deleted broken Applied Steps and edited cells individually to avoid cross-team contamination |
| Chatbot returning "None" for all values | Discovered CSV column names exported from Power BI had "Sum of..." prefixes — rewrote all column references to match exactly |
| Chatbot CSV not found on Streamlit Cloud deployment | Restructured GitHub repo to include proper data/ subfolder instead of root-level files |

---

## 🔮 Future Improvements

- Connect to a live World Cup API (api-football.com) for real-time match score updates
- Upgrade chatbot to use Claude AI API for more natural, conversational responses
- Add player-level statistics (Messi, Mbappé, Vinicius Jr.)
- Embed chatbot directly inside Power BI using Web visual
- Add predictive analytics — which team is most likely to win 2026 based on historical patterns
- Expand to all 48 qualified teams instead of just the Big 3

---

## ▶️ How to Run the Chatbot Locally

```bash
# 1. Clone this repository
git clone https://github.com/alia-analyzes/fifa-chatbot

# 2. Navigate into the folder
cd fifa-chatbot

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the chatbot
python -m streamlit run app.py
```

---

## 📸 Screenshots

### 🏠 Home Page — Toggle Navigation
![Home](screenshots/home.png)

### 🇦🇷 Argentina Dashboard
![Argentina](screenshots/argentina.png)

### 🇧🇷 Brazil Dashboard
![Brazil](screenshots/brazil.png)

### 🇫🇷 France Dashboard
![France](screenshots/france.png)

### 🤖 AI Chatbot
![Chatbot](screenshots/chatbot.png)

---

## 👩‍💻 Author

**Alia Arif**
Third-year BSc Data Science Student

🔗 [LinkedIn](https://www.linkedin.com/in/alia-arif-analyst/)
🐱 [GitHub](https://github.com/alia-analyzes)
📧 alia97arif01@gmail.com
