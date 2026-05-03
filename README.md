#ReviewBot

## Projektbeschreibung 
Reviewbot ist ein KI-gestütztes Code-Review-Tool, das Python Dateien analysiert und automatisierte Verbesserungsvorschläge generiert. Ziel ist es, Codequalität, Sicherheit und Dokumentation zu verbessern, bevor ein menschlicher Review erfolgt. 

# ReviewBot

## 📌 Projektbeschreibung
ReviewBot ist ein KI-gestütztes Code-Review-Tool, das Python-Dateien analysiert und automatisierte Verbesserungsvorschläge generiert. Ziel ist es, Codequalität, Sicherheit und Dokumentation zu verbessern, bevor ein menschlicher Review erfolgt.

## 🎯 Ziele
- Automatisierte Code-Reviews durchführen
- Sicherheitsprobleme erkennen
- fehlende Tests und Dokumentation identifizieren

## ❌ Nicht-Ziele
- Kein vollständiger Ersatz für menschliche Code-Reviews
- Keine automatische Code-Reparatur (nur Vorschläge)
- Kein Fokus auf Performance-Optimierung in Phase 1

## ⚙️ Setup

### Voraussetzungen
- Python 3.x
- Git

### Installation

```bash
git clone https://github.com/DEIN_USERNAME/reviewbot.git
cd reviewbot

python3 -m venv .venv
source .venv/bin/activate

pip install typer pytest openai
