# CS50 Finance — Stock Trading Web App

This project is an implementation of **CS50 Finance**, the stock trading simulation web application from Harvard’s CS50 course.  
It allows users to **register, log in, look up stock quotes, buy and sell shares, and track their portfolio performance** in real time.

---

## Table of Contents

- [Overview](#overview)  
- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [How to Run](#how-to-run)  
- [Database Schema](#database-schema)  
- [Repository Structure](#repository-structure)  
- [Roadmap](#roadmap)  
- [License](#license)

---

## Overview

This project replicates a simplified version of a trading platform, where users can simulate buying and selling stocks with virtual cash.  
The system fetches live stock data via an API and records each transaction, updating the user’s balance and holdings.

It demonstrates skills in **web development, databases, and API integration**, aligned with professional engineering practices.

---

## Features

- **User authentication**: registration, login, and secure sessions.  
- **Portfolio management**: track current holdings and cash balance.  
- **Real-time quotes**: fetch stock prices using an external API.  
- **Buy and sell transactions**: executed with balance checks.  
- **Transaction history**: logs every operation with timestamp.  
- **Error handling and input validation**.  

---

## Tech Stack

- **Python (Flask)** — backend web framework  
- **Jinja2** — HTML templating  
- **SQLite** — relational database  
- **HTML, CSS, Bootstrap** — frontend design  
- **APIs** — stock price lookup (IEX or Alpha Vantage depending on setup)  

---

## How to Run

1. Clone the repository and unzip:

```bash
unzip CS50Finance.zip
cd CS50Finance
```

2. Create and activate a virtual environment:

```bash
python -m venv .venv
# Linux/macOS
source .venv/bin/activate
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Set the environment variable for Flask and API key:

```bash
# Linux/macOS
export FLASK_APP=app.py
export API_KEY=your_api_key_here

# Windows PowerShell
setx FLASK_APP app.py
setx API_KEY your_api_key_here
```

5. Initialize the database:

```bash
flask db upgrade
```

6. Run the application:

```bash
flask run
```

7. Open your browser at `http://127.0.0.1:5000/`.

---

## Database Schema

- **users**: id, username, hash (password), cash  
- **transactions**: id, user_id, symbol, shares, price, timestamp  

This schema ensures full traceability of portfolio and historical trades.

---

## Repository Structure

```
.
├── app.py                 # Main Flask application
├── helpers.py             # Utility functions (e.g., API lookups)
├── templates/             # Jinja2 HTML templates
│   ├── layout.html
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── quote.html
│   ├── buy.html
│   ├── sell.html
│   └── history.html
├── static/                # CSS and assets
├── finance.db             # SQLite database (generated)
├── requirements.txt
└── README.md
```

---

## Roadmap

- Add **password reset functionality**.  
- Integrate with **PostgreSQL/MySQL** for production-ready deployment.  
- Add **unit and integration tests**.  
- Improve frontend with more responsive design.  
- Deploy on **Heroku / AWS Elastic Beanstalk**.  

---

## License

- **MIT**

---

### Recruiter’s note

This project demonstrates ability to:  
- Build and deploy a **full-stack web application**.  
- Handle **authentication, session management, and database design**.  
- Integrate **external APIs** and handle real-world constraints (e.g., balance validation).  
- Apply **best practices in software engineering and documentation**.

It reflects strong foundations in **backend development, databases, and web application design**.
