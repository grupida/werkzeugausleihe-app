# 🚀 Zu GitHub hochladen

## **Schritt 1: GitHub Repo erstellen**

1. Gehe zu https://github.com/new
2. **Repository name:** `werkzeugausleihe-app` (oder was du willst)
3. **Description:** (optional) "Werkzeugausleihe v4.0 - Web-App zur Verwaltung von Werkzeugausleihen"
4. **Public** oder **Private** wählen
5. **WICHTIG:** ❌ **KEINE** README, .gitignore oder Lizenz hinzufügen (haben wir schon!)
6. **"Create repository"** klicken

## **Schritt 2: Commands ausführen**

GitHub zeigt dir nach dem Erstellen Commands an. Du brauchst diese hier:

```bash
# Ins Repo-Verzeichnis wechseln
cd /data/.openclaw/workspace/werkzeugausleihe-app

# Remote hinzufügen (ersetze USERNAME mit deinem GitHub-Namen!)
git remote add origin https://github.com/USERNAME/werkzeugausleihe-app.git

# Hochladen
git push -u origin main
```

**Beispiel:**
Wenn dein Username `chris123` ist:
```bash
git remote add origin https://github.com/chris123/werkzeugausleihe-app.git
git push -u origin main
```

## **Schritt 3: Login (wenn nötig)**

Beim ersten Push fragt GitHub nach deinen Zugangsdaten:

### **Variante A: Personal Access Token (empfohlen)**
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. "Generate new token"
3. **Scopes:** `repo` auswählen
4. Token kopieren
5. Beim `git push`:
   - **Username:** Dein GitHub-Username
   - **Password:** Den Token (NICHT dein normales Passwort!)

### **Variante B: SSH (fortgeschritten)**
Falls du SSH-Keys nutzt, ersetze die URL:
```bash
git remote set-url origin git@github.com:USERNAME/werkzeugausleihe-app.git
```

## **Fertig! 🎉**

Dein Repo ist jetzt online:
```
https://github.com/USERNAME/werkzeugausleihe-app
```

## **Bonus: GitHub Pages aktivieren (kostenlos hosten!)**

1. Gehe zu deinem Repo auf GitHub
2. **Settings** → **Pages**
3. **Source:** `main` Branch auswählen
4. **Folder:** `/ (root)`
5. **Save**

➡️ Nach 1-2 Minuten ist deine App live unter:
```
https://USERNAME.github.io/werkzeugausleihe-app/
```

**Komplett kostenlos gehostet!** 🎉

---

## **Später Änderungen hochladen:**

```bash
cd /data/.openclaw/workspace/werkzeugausleihe-app

# Änderungen committen
git add .
git commit -m "Beschreibung der Änderungen"

# Hochladen
git push
```

---

**Probleme?** Check:
- GitHub-Username richtig geschrieben?
- Token hat `repo`-Rechte?
- Repo ist leer erstellt (keine README hinzugefügt)?
