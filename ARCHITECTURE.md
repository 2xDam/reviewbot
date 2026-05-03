# ReviewBot Architecture

## 1. Ziel von ReviewBot

ReviewBot ist ein KI-gestütztes Code-Review-System für Python-Projekte. Es soll Entwickler dabei unterstützen, typische Probleme in Codequalität, Sicherheit, Tests und Dokumentation frühzeitig zu erkennen.

## 2. Was ReviewBot können soll

- Python-Dateien einlesen und analysieren
- Code-Reviews mit Hilfe eines LLMs generieren
- Hinweise zu Codequalität, Sicherheit, Tests und Dokumentation geben
- Ergebnisse später strukturiert ausgeben, z.B. als JSON oder Markdown
- verschiedene LLM-Backends unterstützen, z.B. Cloud-Modelle und lokale Modelle

## 3. Was ReviewBot ausdrücklich nicht können soll

- menschliche Code-Reviews vollständig ersetzen
- automatisch produktiven Code verändern
- sicherheitskritische Freigaben alleine treffen
- vollständige statische Analyse-Tools wie SonarQube ersetzen

## 4. Ideen aus flake8 und bandit

### flake8

flake8 ist ein statisches Analysewerkzeug für Python. ReviewBot übernimmt daraus die Idee, Code systematisch auf Stil- und Qualitätsprobleme zu prüfen.

Übernommene Ideen:
- klare Trennung einzelner Prüfbereiche
- reproduzierbare Analyse
- kurze, konkrete Hinweise für Entwickler

### bandit

bandit ist ein Security-Scanner für Python. ReviewBot übernimmt daraus die Idee, sicherheitsrelevante Muster explizit zu betrachten.

Übernommene Ideen:
- Fokus auf typische Sicherheitsprobleme
- Priorisierung nach Schweregrad
- Hinweise auf unsichere APIs oder riskante Patterns

## 5. Erste geplante Architektur

```text
User
  |
  v
CLI
  |
  v
Reviewer
  |
  v
Prompt Builder
  |
  v
LLM Backend
  |
  v
Review Output
