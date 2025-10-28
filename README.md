# 💸 Smart Expense Assistant (PocketMind)

**Smart Expense Assistant** is an AI-powered Flask application that helps users manage their daily expenses, classify them as *Needs* or *Wants*, and generate personalized money-saving insights.  
It integrates **Gemini AI** for analysis and **Firebase** for data management.

---

## 🧩 Project Structure
```

Pocket-Mind/
│
├── main.py                  # Flask backend – handles routes and AI logic
├── templates/               # HTML UI pages
│   ├── home.html
│   ├── dashboard.html
│   ├── planner.html
│   ├── analysis.html
│   └── insights.html
├── serviceAccountKey.json   # Firebase admin SDK key (NOT to upload publicly)
├── requirements.txt         # Python dependencies
└── README.md

````

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Khushalha/Pocket-Mind.git
cd Pocket-Mind
````

### 2️⃣ Create and Activate a Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate   # for Windows
# OR
source venv/bin/activate  # for Mac/Linux
```

### 3️⃣ Install Required Libraries

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Get Your Gemini API Key

1. Go to [Google AI Studio](https://aistudio.google.com/app/apikey).
2. Create a new **Gemini API Key**.
3. Open `main.py` and replace:

   ```python
   GEMINI_API_KEY = "your api key"
   ```

   with your actual key:

   ```python
   GEMINI_API_KEY = "AIza...yourkey..."
   ```

---

### 5️⃣ Set Up Firebase

1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Create a new project.
3. Navigate to:
   **Project Settings → Service Accounts → Generate new private key**
4. Download the JSON file and rename it to:

   ```
   serviceAccountKey.json
   ```
5. Place it in your project root (same folder as `main.py`).

⚠️ **Important:** Never upload this JSON file to GitHub.
Add it to your `.gitignore` file like this:

```
serviceAccountKey.json
```

---

### 6️⃣ Run the Application

```bash
python main.py
```

Then open your browser at:
👉 [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🧠 How It Works

* **main.py** – Handles AI prompts, Firebase setup, and Flask routes.
* **Gemini AI** – Classifies transactions as “Need” or “Want” and provides personalized saving tips.
* **Firebase** – Securely manages backend data such as user transactions.
* **HTML Templates** – Define the frontend UI (Home, Dashboard, Planner, Analysis, Insights).
* **requirements.txt** – Lists all Python modules required to run this project.

---

## 🧾 Features

✅ Expense classification using Gemini AI
✅ Personalized savings advice
✅ Financial insights chat assistant
✅ Firebase-backed data management
✅ Flask-based user interface

---

## 🛡️ Security Tips

* 🚫 Never commit `serviceAccountKey.json` or API keys to GitHub.
* 🔒 Use `.env` files for secrets if deploying online.
* 🧾 Add sensitive files to `.gitignore` before pushing.

---


