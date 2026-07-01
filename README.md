# AmazeSort

<p align="center">
  <img src="https://img.shields.io/badge/AmazeSort-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="AmazeSort">
</p>

<p align="center">
  <strong>AI-powered file organization for the modern desktop</strong>
</p>

<p align="center">
  <a href="https://github.com/AmazeContinuityProjects/AmazeSort/actions/workflows/python-app.yml">
    <img src="https://github.com/AmazeContinuityProjects/AmazeSort/actions/workflows/python-app.yml/badge.svg" alt="CI">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/license/AmazeContinuityProjects/AmazeSort?style=flat-square&label=License" alt="License">
  <img src="https://img.shields.io/github/repo-size/AmazeContinuityProjects/AmazeSort?style=flat-square&label=Repo%20Size&color=blueviolet" alt="Repo Size">
  <br>
  <img src="https://img.shields.io/badge/Python_3.10+-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white" alt="PySide6">
  <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face">
</p>

---

## Overview

AmazeSort is a Python-based desktop application that intelligently organizes files using three approaches:

1. **Rule-based** — traditional pattern matching with customizable rules
2. **Hybrid** — combines rules with transformer-model associations
3. **Full AI** — transformer-based classification using DistilBERT

The app scans your destination directory structure, learns associations from your existing organization, and automatically sorts files into the right folders.

> **Note:** This project is in alpha stage. The UI is functional but some features are still being implemented.

---

## Features

- **Generalized Architecture** — Define your own hierarchical guidebook (syllabus.json) for any domain
- **AI-Enhanced Classification** — DistilBERT-based transformer model for accurate file categorization
- **Dynamic Association Generation** — Recursively scans directories and merges structure with guidebook
- **Duplicate Detection** — File hashing (MD5/SHA-256) prevents redundant processing
- **Modern, Responsive UI** — PySide6 with Fluent/Material-inspired design
- **Real-time Progress** — Dual progress bars for training and sorting operations
- **Extensible** — Modular design for future enhancements (WinUI3, database integration)

---

## Tech Stack

| Category | Technology |
|----------|------------|
| **Language** | Python 3.10+ |
| **UI Framework** | PySide6 (Qt6) |
| **ML Framework** | Hugging Face Transformers (DistilBERT/DistilGPT2) |
| **PDF Processing** | PyPDF2 |
| **Fuzzy Matching** | fuzzywuzzy |
| **Hash Detection** | hashlib |

---

## Quick Start

```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
python app.py
```

---

## Architecture

| Module | File | Purpose |
|--------|------|---------|
| **Configuration** | `config.py` | Settings, thresholds, directories |
| **Utilities** | `utils.py` | Normalization, fuzzy matching, PDF extraction, hashing |
| **Associations** | `associations.py` | Directory scanning & association tree generation |
| **AI Model** | `ai_model.py` | DistilBERT training & prediction |
| **File Sorter** | `file_sorter.py` | Core sorting logic (rule/hybrid/AI) |
| **UI** | `main_ui.py` / `settings_dialog.py` | PySide6 graphical interface |
| **Entry Point** | `app.py` | Application bootstrap |

---

## Modes

1. **Rule-based** — Uses enriched associations from the scanned directory structure
2. **Hybrid** — Rule scores + transformer confidence with configurable weights
3. **Full AI** — Pure transformer model prediction

---

## Contributing

Contributors are required to sign a CLA before contributing. See individual contribution guidelines in each repository.

---

## License

Dual-licensed: GPL-3.0 for public use; commercial licenses available from the maintainer.
