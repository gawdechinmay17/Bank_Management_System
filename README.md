# 🏦 Bank Management System

A simple Python-based bank management system with both a command-line interface (CLI) and a web-based UI built with Streamlit.

---

## 📁 Project Structure

```
├── app.py          # Streamlit web application (UI layer)
├── hello.py        # Bank class with all core logic (refactored from h.ipynb)
├── data.json       # JSON file used as the database
├── main.ipynb      # Original CLI version (Jupyter Notebook)
└── h.ipynb         # Refactored Bank class for use with Streamlit
```

---

## ✨ Features

- **Create Account** — Register with name, age, email, and a 4-digit PIN. Auto-generates a unique account number.
- **Deposit Money** — Add funds (max ₹10,000 per transaction).
- **Withdraw Money** — Deduct funds with balance validation.
- **Show Account Details** — View all account information securely using account number + PIN.
- **Update Info** — Change name, email, or PIN.
- **Delete Account** — Permanently remove an account.

---

## 🛠️ Tech Stack

| Layer       | Technology        |
|-------------|-------------------|
| Language    | Python 3.x        |
| Web UI      | Streamlit         |
| Storage     | JSON (flat file)  |
| Notebook    | Jupyter Notebook  |

---

## 🚀 Getting Started

### 1. Clone / Download the project

```bash
git clone <your-repo-url>
cd bank-management-system
```

### 2. Install dependencies

```bash
pip install streamlit
```

### 3. Run the Streamlit App

Make sure `hello.py` (the Bank class file exported from `h.ipynb`) is in the same directory as `app.py`, then run:

```bash
streamlit run app.py
```

### 4. Run the CLI Version (Optional)

Open `main.ipynb` in Jupyter Notebook or JupyterLab and run all cells:

```bash
jupyter notebook main.ipynb
```

---

## 🔐 Account Number Format

Account numbers are auto-generated as a 7-character alphanumeric string containing:
- 3 random letters
- 3 random digits
- 1 special character (from `!@#$%^&*`)

Example: `x2N@G46`

---

## 📦 Data Storage

All account data is stored locally in `data.json`. Each record looks like:

```json
{
    "name": "John Doe",
    "age": 25,
    "email": "john@example.com",
    "pin": 1234,
    "accountNo.": "x2N@G46",
    "balance": 1000
}
```

> ⚠️ **Note:** PINs are stored in plain text. This project is intended for learning purposes only and is not suitable for production use.

---

## ⚙️ Business Rules

- Minimum age to open an account: **18 years**
- PIN must be exactly **4 digits**
- Maximum deposit per transaction: **₹10,000**
- Withdrawals are rejected if balance is insufficient

---

## 📌 Known Limitations

- No authentication beyond PIN (no hashing/encryption)
- Single-user access only (no concurrency handling)
- Data stored in a flat JSON file (not scalable)
- No transaction history

---

## 🙋 Author

Built as a learning project to explore Python OOP, file I/O, and Streamlit UI development.
