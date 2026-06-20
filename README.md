# Zenith-OS-Assistant 🚀

Intelligent OS assistant built for the SVCE Hackathon to simplify file organization and browser tab management using AI. Stay productive with smart file sorting, automated folder creation, and seamless browser control.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)

## 🎯 Overview

Zenith-OS-Assistant is a hackathon-grade productivity system that:

- **Organizes files automatically** by type, creation date, or content pattern
- **Suggests folder structures** and displays them via interactive directory trees
- **Manages browser tabs** using dedicated browser extensions
- **Provides a clean web interface** for file uploads and management
- **Processes operations locally** using Python and Flask

## 📊 System Architecture

```
┌─────────────────────────────────────────────────────────┐
│          Frontend (HTML/CSS/JS Templates)              │
└────────────────────┬────────────────────────────────────┘
                     │ HTTP
                     ▼
┌─────────────────────────────────────────────────────────┐
│             Flask Backend (Python)                     │
├─────────────────────────────────────────────────────────┤
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  │
│  │ File Handler │  │ NLP/AI Engine│  │ Browser Ext. │  │
│  │ (shutil, os) │  │ (Categorizer)│  │ Integration  │  │
│  └──────────────┘  └──────────────┘  └──────────────┘  │
└─────────────────────────────────────────────────────────┘
```

## ✨ Features

### 📁 Smart File Management
- **Type-based Sorting**: Automatically groups files into categories like Documents, Images, Videos, Code, and Archives.
- **Date-based Sorting**: Organizes files hierarchically by year and month of creation.
- **Content Pattern Matching**: Identifies invoices, resumes, and backups using regex patterns.

### 🌐 Browser Tab Manager
- Connects with custom browser extensions to manage open tabs.
- Voice/text capabilities (via AI operator) to command browser actions.

### 🌳 Interactive Directory Tree
- Visualizes the proposed file structure before moving files.
- Generates beautiful ASCII-style folder trees (`├──`, `└──`).

### ⚙️ Modular Backend
- **Flask-based API** for command interpretation.
- Easy to extend with new file types and organization rules.

## 📁 Project Structure

```text
Zenith-OS-Assistant-Smart-File-and-Browser-Manager/
├── app.py                     # Main Flask application
├── requirements.txt           # Python dependencies
├── AI/                        # AI operator scripts and logic
│   └── operator/
├── browserextension/          # Chrome/Firefox extension code
├── static/                    # CSS, JS, and image assets
├── templates/                 # HTML UI templates
│   ├── index.html             # Upload interface
│   ├── analyze.html           # Tree visualization
│   └── results.html           # Organization results
├── uploads/                   # Temporary file storage (auto-generated)
└── README.md                  # This documentation
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Modern Web Browser (Chrome/Firefox)

### Setup Instructions (3 minutes)

```bash
# 1. Clone the repository
git clone https://github.com/meswaramuthu/Zenith-OS-Assistant-Smart-File-and-Browser-Manager.git
cd Zenith-OS-Assistant-Smart-File-and-Browser-Manager

# 2. Create & activate virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate          # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Start the server
python app.py
```

**Result:** The application will be running at `http://127.0.0.1:5000/`

## 🔗 How it Works

### 1. Upload
Users upload multiple files (documents, images, code files, etc.) through the clean web interface.

### 2. Analyze
The backend analyzes the files (mime types, extensions, creation dates) and generates a proposed folder structure.

### 3. Organize
With one click, the application physically moves the files into beautifully organized, auto-generated subdirectories.

## 📦 Technology Stack

### Frontend
- **HTML5/CSS3** - Responsive UI
- **JavaScript** - Client-side interactivity
- **Jinja2** - Dynamic HTML templating

### Backend
- **Python (Flask)** - Web framework
- **Werkzeug** - Secure file handling
- **shutil & os** - System-level file operations
- **mimetypes** - File type inference

## 🔧 Development Workflow

### Adding Custom File Categories
Edit the `suggest_category_by_extension` function in `app.py`:
```python
extension_categories = {
    ...
    '.pdf': 'Documents',
    '.sketch': 'Design Files', # Add your custom type
}
```

## 🐛 Troubleshooting

### Port 5000 is in use
If the Flask server fails to start, specify a different port:
```bash
flask run --port=8080
```

### Files not organizing correctly
Check the allowed extensions list in `app.py`:
```python
ALLOWED_EXTENSIONS = {'txt', 'pdf', 'png', 'jpg', 'jpeg', ...}
```

## 📄 License
MIT - See LICENSE file for details.

---

**Built with ❤️ during the SVCE Hackathon**
