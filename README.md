
# Bug Hunter Pro 🕵️‍♂️💻

Welcome to **Bug Hunter Pro** – an advanced modular vulnerability scanner framework for bug bounty hunters and ethical hackers.

---

## 📦 What's Inside

```
bug_hunter_pro/
├── core/                  # Main engine and report generation
├── configs/               # Tool configurations and API keys
├── modules/               # Specialized modules (subdomain, port scan, etc.)
├── logs/                  # Scan logs
├── reports/               # Generated reports
```

---

## 🛠 Requirements

Before using this tool, install the following:

### ✅ System Tools (Linux or WSL recommended)

```bash
sudo apt update && sudo apt install -y nmap nikto sqlmap sublist3r dirsearch python3-pip
```

### ✅ Python Dependencies

```bash
pip install -r requirements.txt
```

> You can create a `requirements.txt` later with any Python modules you add (like `requests`, `rich`, etc.)

---

## 🚀 How to Use

### 1. Navigate to the project folder

```bash
cd bug_hunter_pro
```

### 2. Set up configurations

Edit `configs/tools_config.json` to include paths or API keys if needed.

### 3. Run the Scanner

Eventually you'll use a script like:

```bash
python3 core/scanner.py
```

That script will handle:

- Running modules from `/modules/`
- Collecting results
- Logging and report generation

---

## 🔍 Module Overview

| Module             | Description                          |
|--------------------|--------------------------------------|
| `subdomain_enum.py` | Finds subdomains with Sublist3r     |
| `port_scan.py`      | Scans open ports with Nmap          |
| `dir_brute.py`      | Brute-forces hidden directories     |
| `web_vuln_scan.py`  | Scans for web vulnerabilities       |
| `sql_injection.py`  | Uses SQLMap for SQLi detection      |
| `api_tester.py`     | API-specific logic (coming soon)    |
| `gpt_assistant.py`  | GPT-powered analysis (optional)     |

---

## 🧠 GPT Integration (Optional)

If you have an OpenAI API key, you can extend `gpt_assistant.py` to analyze scan results and suggest solutions or even write reports.

---

## 📄 Output

Results will be saved in:

- `logs/` → Raw logs
- `reports/` → Human-readable reports (HTML/Markdown)

---

## ⚠️ Legal Notice

This tool is intended **only for legal and authorized testing** (e.g., bug bounty programs, your own systems). Unauthorized scanning of systems you do not own is **illegal**.

---

## 📫 Questions?

Message your favorite AI sidekick. 😉

---

Happy hunting! 🐛💰
