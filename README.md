# Git, Markdown, VS Code & HTML/CSS – snabbguide

Kortfattade exempel för dig som är ny i kursen.

---

## 1. Git & GitHub

**Git** = versionshantering på din dator (körs i terminalen).
**GitHub** = webbsida där du lagrar och delar dina repon.

### Första gången – ange vem du är
```bash
git config --global user.name "Ditt Namn"
git config --global user.email "din@mejl.se"
```

### Från mapp till GitHub
```bash
cd C:\Users\<användarnamn>\Documents\mitt-projekt   # gå till projektmappen
git init                                             # starta Git i mappen
git add .                                            # lägg till alla filer
git commit -m "Första commit"                        # spara en version
git branch -M main                                   # döp grenen till main
git remote add origin https://github.com/<användarnamn>/<repo>.git
git push -u origin main                              # ladda upp till GitHub
```

### När du ändrat något
```bash
git status                    # vad har ändrats?
git add .
git commit -m "Beskriv ändringen"
git push
```

| Kommando | Gör |
|---|---|
| `git status` | Visar ändrade filer |
| `git log --oneline` | Visar tidigare commits |
| `git clone <url>` | Kopierar ett repo till din dator |
| `git pull` | Hämtar senaste ändringarna från GitHub |

> **Tips:** Skapa repot på GitHub *utan* README om du redan har en lokalt – annars krockar de.

---

## 2. Markdown

README.md skrivs i Markdown – en förenklad variant av HTML.

| Du skriver | Resultat |
|---|---|
| `# Rubrik` | Stor rubrik |
| `## Underrubrik` | Mindre rubrik |
| `**fet**` | **fet** |
| `*kursiv*` | *kursiv* |
| `- punkt` | • punkt |
| `1. punkt` | 1. numrerad lista |
| `[länk](https://mdu.se)` | [länk](https://mdu.se) |
| `![bild](bild.png)` | visar en bild |
| `` `kod` `` | `kod` |
| `> citat` | indraget citat |

**Kodblock** – tre backticks och språket:

~~~markdown
```html
<h1>Hej</h1>
```
~~~

---

## 3. Visual Studio Code

### Installera och konfigurera
1. Ladda ner från [code.visualstudio.com](https://code.visualstudio.com) och installera.
2. **File → Open Folder** – öppna alltid hela projektmappen.
3. Installera tillägg via **Extensions** (`Ctrl + Shift + X`):
   - **Live Server** (Ritwick Dey) – visar webbsidan direkt i webbläsaren
   - **Lorem Ipsum** (Daniel Imms) – fyller på med testtext

### Bra kortkommandon
| Kortkommando | Gör |
|---|---|
| `Ctrl + Shift + P` | Command Palette – sök alla funktioner |
| `Ctrl + S` | Spara |
| `Ctrl + Shift + V` | Förhandsgranska Markdown |
| `Alt + Shift + F` | Formatera koden |
| `Ctrl + #` | Kommentera rad (svenskt tangentbord) |

### Emmet – skriv mindre kod
| Skriv + `Tab` | Blir |
|---|---|
| `!` | Färdig HTML-mall |
| `h1` | `<h1></h1>` |
| `p>lorem` | `<p>` med testtext |
| `ul>li*3` | lista med tre punkter |

---

## 4. HTML & CSS

**HTML** = innehåll och struktur. **CSS** = utseende.

### index.html
```html
<!DOCTYPE html>
<html lang="sv">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Min sida</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Hej världen</h1>
    <p>Min första webbsida.</p>
    <a class="knapp" href="https://github.com">Till GitHub</a>
</body>
</html>
```

### style.css
```css
body {
    font-family: Arial, sans-serif;
    max-width: 600px;
    margin: 40px auto;
}

h1 {
    color: #2a4d69;
}

.knapp {
    background: #2a4d69;
    color: white;
    padding: 10px 20px;
    border-radius: 6px;
    text-decoration: none;
}
```

| CSS-väljare | Träffar |
|---|---|
| `h1` | alla `<h1>` |
| `.knapp` | element med `class="knapp"` |
| `#meny` | elementet med `id="meny"` |

> Öppna `index.html` med **Live Server** (`Ctrl + Shift + P` → *Live Server: Open with Live Server*) för att se resultatet.

---

*Skapad av Mohamed Hussein – Interaktionsdesign, MDU, HT2026*
