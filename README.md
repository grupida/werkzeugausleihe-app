# 🔨 Werkzeugausleihe v4.0

Eine moderne, benutzerfreundliche Web-App zur Verwaltung von Werkzeugausleihen – komplett als **Single-File HTML** ohne Backend!

## ✨ Features

### **Mitarbeiter-Funktionen:**
- 📦 Werkzeug-Katalog durchsuchen (mit Suche & Kategorien)
- 🛒 Warenkorb-System für Reservierungen
- 📅 Zeitraum-Auswahl (von/bis)
- 🔧 Schadensmeldung mit Foto-Upload
- ⚠️ Überfälligkeits-Warnung bei verspäteten Rückgaben

### **Admin-Funktionen:**
- 📊 Dashboard mit Statistiken & Top 5 Werkzeugen
- ➕ Werkzeuge hinzufügen/bearbeiten/löschen
- 🏷️ Kategorien (Elektro, Hand, Garten, Mess, Sicherheit, etc.)
- 📱 QR-Code-Generator für jedes Werkzeug
- 📄 CSV-Import/Export
- ✅ Reservierungen bestätigen & ausgeben
- ↩️ Rückgaben dokumentieren (Zustand + Kommentar)
- 🔧 Schadensmeldungen verwalten
- 📈 Überfälligkeits-Tracking
- 📜 Vollständige History (Reservierung → Ausgabe → Rückgabe)

## 🚀 Installation

### **Variante 1: Lokale Nutzung**
1. Datei `index.html` herunterladen
2. Doppelklick → öffnet im Browser
3. Fertig! 🎉

### **Variante 2: Auf Webserver**
1. `index.html` auf Webspace hochladen
2. URL aufrufen
3. Fertig!

**Keine Installation nötig!** Läuft komplett im Browser.

## 🔐 Admin-Zugang

**Standard-Passwort:** `admin123`

⚠️ **Wichtig:** Ändere das Passwort im Code (Zeile ~532):
```javascript
const ADMIN_PASSWORD = 'admin123'; // <- Hier ändern!
```

## 📊 Datenbank

Die App nutzt **sql.js** (SQLite im Browser) + **localStorage** zur Persistierung.

**Daten bleiben erhalten:**
- Solange der Browser-Cache nicht gelöscht wird
- Bei gleichem Browser & gleichem PC

**Backup:**
- Admin → "Daten exportieren" (CSV)
- Browser DevTools → Application → Local Storage → `werkzeugDB` kopieren

## 📸 Screenshots

*(Hier könntest du später Screenshots einfügen)*

## 🛠️ Technologie

- **Frontend:** Vanilla HTML/CSS/JavaScript
- **Datenbank:** sql.js (SQLite im Browser)
- **QR-Codes:** qrcode.js
- **Speicher:** localStorage (Browser)

**Keine Abhängigkeiten installieren!** Alles läuft über CDN.

## 📝 CSV-Import Format

```csv
Werkzeug,Beschreibung,Zustand,Inventarnummer,Kategorie
Bohrmaschine,Makita 18V,Gut,WZ-001,Elektro
Hammer,Schlosserhammer 500g,Neu,WZ-002,Hand
Säge,Stichsäge Bosch,Gebraucht,WZ-003,Elektro
```

**Hinweis:** Datei muss UTF-8 kodiert sein (für Umlaute).

## 🔄 Workflow

### **Reservierung (Mitarbeiter):**
1. Werkzeuge auswählen → Warenkorb
2. Name + Zeitraum (von/bis) eingeben
3. "Reservieren" → Status: **Reserviert** (orange)

### **Ausgabe (Admin):**
1. Admin sieht Reservierung
2. "Ausgeben" klicken → Status: **Ausgeliehen** (rot)

### **Rückgabe (Admin):**
1. "Rückgabe" klicken
2. Zustand auswählen (OK/Defekt/Reinigung/Reparatur)
3. Optional: Kommentar hinzufügen
4. Status: **Zurückgegeben** (grau) → Werkzeug wieder verfügbar

### **Schadensmeldung:**
1. Mitarbeiter/Admin meldet Schaden
2. Status: **Defekt** (schwarz) → blockiert Ausleihe
3. Admin markiert als "behoben" → wieder verfügbar

## ⚠️ Überfälligkeit

- Ausleihen mit überschrittenem "Bis"-Datum werden **rot** markiert
- Badge: **⚠️ Überfällig** (pulsierend)
- Dashboard zeigt Anzahl überfälliger Ausleihen

## 🏆 Top 5 Statistik

Admin-Dashboard zeigt die 5 meistgenutzten Werkzeuge (nach Anzahl Ausleihen).

## 📂 Projekt-Struktur

```
werkzeugausleihe-app/
├── index.html          # Die komplette App (Single-File)
├── README.md           # Diese Datei
├── LICENSE             # MIT Lizenz
└── .gitignore          # Git-Ignore-Regeln
```

## 🤝 Contribution

Pull Requests sind willkommen! Für größere Änderungen bitte zuerst ein Issue öffnen.

## 📄 Lizenz

[MIT](LICENSE) - Frei nutzbar für private & kommerzielle Projekte!

## 💡 Ideen für Erweiterungen

- [ ] Multi-User mit Login
- [ ] E-Mail-Benachrichtigungen
- [ ] Barcode-Scanner
- [ ] Wartungsintervalle
- [ ] Kalenderansicht
- [ ] Erinnerungen (Browser-Notifications)
- [ ] Mehrfach-Werkzeuge (Bestand-Management)
- [ ] PDF-Export (Inventarliste, QR-Etiketten)
- [ ] Dark Mode

---

**Entwickelt mit ❤️ und KI-Power 💊**

**Version:** 4.0  
**Letzte Aktualisierung:** 2026-02-19
