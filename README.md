# 🌌 Zenith-OS-Assistant: Smart File and Browser Manager

A voice- and text-controlled OS assistant built to simplify file organization and browser tab management using AI.  
Designed and built during **SVCE Hackathon**.

---

## 🚀 Overview

**Zenith-OS-Assistant** is an AI-powered productivity tool that helps users manage files and browser tasks efficiently via natural language and voice commands. Whether it's organizing files by type or date, or managing browser tabs with ease, this assistant empowers users to interact with their system like never before.

---

## 🧠 Features

- 🗂️ **Smart File Manager**
  - Organize files by type (e.g., PDF, images, code)
  - Sort files by creation or modification date
  - Move and rename files intelligently using commands

- 🌐 **Browser Tab Manager**
  - Open, close, or group tabs using voice or typed instructions
  - Manage URLs and bookmarks using a natural interface

- 🗣️ **Voice + Text Input**
  - Command the assistant via mic or keyboard
  - Built-in NLP processing for flexible interaction

- 🧩 **Modular Backend**
  - Flask-based API server for command interpretation
  - Scalable design with easy plugin integration

---

## 🔧 Tech Stack

| Layer          | Technology        |
|----------------|-------------------|
| Frontend       | HTML, CSS, JS     |
| Backend        | Python (Flask)    |
| NLP            | OpenAI / spaCy    |
| Voice Input    | SpeechRecognition |
| File Handling  | OS, shutil, pathlib|
| Browser Control| PyAutoGUI / Selenium |

---

## 📦 Installation

```bash
git clone https://github.com/sujitlaware1809/Zenith-OS-Assistant-Smart-File-and-Browser-Manager.git
cd Zenith-OS-Assistant-Smart-File-and-Browser-Manager
pip install -r requirements.txt
python app.py
