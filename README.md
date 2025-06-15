# Text‑to‑SQL LLM App (MySQL + Streamlit + LangChain + Google PaLM)

**A user-friendly web app that lets you chat with your MySQL database using natural‑language queries. Powered by Google PaLM, LangChain, and Streamlit.**

---

## 🚀 Why it matters

Turn complex SQL queries into simple English conversations. Ask questions like “How many white Adidas T‑shirts are left?” or “What revenue will we generate if we sell all S‑size shirts with discounts?” — and get immediate answers. No SQL knowledge required.

---

## 🧩 Key Features

- Natural‑language to SQL translation (Google PaLM)
- Encourages accurate answers with few‑shot prompting
- Fast similarity search using Hugging Face embeddings + Chroma
- Intuitive Streamlit interface
- Powered by LangChain agent framework
- Runs on local MySQL database

---

## 📦 What’s Inside

```
.
├── main.py              # Streamlit app — handles UI & user interactions
├── langchain_helper.py  # Builds and manages the LLM‑to‑SQL chain
├── few_shots.py         # Sample prompts for few‑shot learning
├── requirements.txt     # Python dependencies
└── .env                 # Store your Google API key securely
```

---

## ⚙️ Setup & Run

1. **Clone the repo**  
   ```bash
   git clone https://github.com/skill-curb/Text-To-SQL-LLM-App-with-MYSQL-SteamLit-LangChain-using-Google-Palm.git
   cd Text-To-SQL-LLM-App-with-MYSQL-SteamLit-LangChain-using-Google-Palm
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Get a Google PaLM API key**  
   Sign up at [Makersuite](https://makersuite.google.com), then add to your `.env`:
   ```
   GOOGLE_API_KEY="your_api_key_here"
   ```

4. **Set up your MySQL database**  
   Run your creation script (`CREATE TABLE …`) to load your schema and sample data.

5. **Start the app**  
   ```bash
   streamlit run main.py
   ```

6. **Chat away**  
   Ask questions like:
   - „How many white Adidas T‑shirts are in stock?“  
   - „What’s the total value of S‑size inventory?“  
   - „How much sales can we make today if we sell all XL shirts after discounts?“

---

## 🛠 Under the Hood

1. **Streamlit UI**: Accepts user input and displays SQL + results.  
2. **LangChain pipeline**:  
   - **Few‑shot prompting** guides PaLM to generate accurate SQL.  
   - **Hugging Face embeddings + Chroma** fetch relevant examples.  
   - **SQL agent** executes the query and returns results.  
3. **MySQL** stores your product, stock, and sales data.

---

## ✅ Troubleshooting

- **Missing `GOOGLE_API_KEY`** – make sure it’s present in your `.env`.  
- **MySQL connection errors** – verify your credentials/port/schema.  
- **Weird SQL output** – try expanding your prompt examples (few-shot logic).

---

