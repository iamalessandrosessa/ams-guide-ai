# GitHub Copilot Guide Hub

Un sito web moderno e professionale per visualizzare guide complete su GitHub Copilot e automazione AI, organizzate in un percorso didattico progressivo.

## 🎯 Caratteristiche

- **Design Professionale**: Interfaccia pulita senza emoji, tema dark elegante
- **Completamente Responsive**: Ottimizzato per desktop, tablet e mobile
- **Percorso Didattico**: Guide organizzate da setup base a metodologie avanzate
- **Contenuti Completi**: 4 guide dettagliate con esempi pratici e codice
- **Riferimenti Ufficiali**: Sezione dedicata con tutti i link GitHub Copilot
- **Navigazione Intuitiva**: TOC per ogni guida, scroll smooth, back navigation

## 📚 Guide Disponibili

### 1. GitHub Copilot CLI su Windows (Introduzione)
**Durata**: 15 minuti | **Livello**: Base | **Status**: ✅ Completa

Guida fondamentale per iniziare. Setup completo di GitHub Copilot CLI su Windows.

**Contenuti**:
- Prerequisiti (Windows 10+, Account GitHub, Copilot attivo)
- Installazione tramite `winget install GitHub.Copilot`
- Login e autenticazione con `/login`
- Comandi principali: `suggest`, `explain`, `chat`, `/model`
- Esempi pratici con code blocks
- Troubleshooting Windows

**File**: `pages/cli-windows.html`

---

### 1bis. Automation Assets Engineering (Intro Parallela - WSL)
**Durata**: 30+ minuti | **Livello**: Completa | **Status**: ✅ Completa

Guida Engineering di Giancarlo Compagno. Parallelo alla guida CLI Windows ma con setup WSL/Linux.

**Contenuti**:
- Panoramica Automation Assets per SLCM
- Cambio di paradigma (capacità distribuita vs piattaforma centralizzata)
- Ecosistema strumenti (Development, Testing, Quality)
- MCP Servers e CLI Tools
- Quick Start guide
- **Sezione completa riferimenti ufficiali GitHub Copilot**
- Link alla guida HTML originale esterna

**File**: `pages/automation-assets.html`

---

### 2. Agent Skills con GitHub Copilot
**Durata**: 20 minuti | **Livello**: Avanzata | **Status**: ✅ Completa

Come utilizzare le Agent Skills per estendere il comportamento di Copilot con regole strutturate.

**Contenuti**:
- Cos'è una Agent Skill e come funziona
- Marketplace skills.sh per Skills pronte
- Installazione e posizionamento (`.github/skills/`)
- Uso in **VS Code** (percorso stabile)
- Uso in **IntelliJ/JetBrains** (public preview)
- Esempi reali **Spring Java**: controller, service, DTO patterns
- Esempi reali **Angular**: best practices enterprise
- File `SKILL.md` completi con regole e output
- Riferimenti ufficiali

**File**: `pages/agent-skills.html`

---

### 3. Tecnica Backlog + Kanban (Spec-Driven)
**Durata**: 45 minuti | **Livello**: Metodologia | **Status**: ✅ Completa

Metodologia completa per gestire progetti con approccio Spec-Driven usando Backlog.md.

**Contenuti**:
- Workflow completo: `prompt.md` → `spec.md` → task atomici
- Installazione Backlog.md (globale vs locale)
- Wizard init con configurazione consigliata
- Generazione spec.md da prompt.md con Copilot
- Generazione task atomici da spec.md
- Comandi essenziali Backlog.md
- **Esecuzione con Agent Mode**: algoritmo selezione task, prompt "Master"
- Esecuzione con Copilot CLI per review
- **Continuità tra sessioni** (spec.md come verità tecnica)
- Best practices e anti-pattern
- Cheat-sheet comandi completo

**File**: `pages/backlog-kanban.html`

---

## 🗂️ Struttura del Progetto

```
AMS Guide AI/
├── index.html                      # Homepage con intro e card guide
├── assets/
│   ├── css/
│   │   ├── styles.css             # Stili globali (dark theme, navbar, footer)
│   │   ├── guides-page.css        # Stili lista guide
│   │   └── guide-template.css     # Template riutilizzabile per guide
│   └── js/
│       └── script.js              # Animazioni, scroll smooth, navbar
├── pages/
│   ├── guides.html                # Lista guide con ordine didattico
│   ├── riferimenti.html           # Pagina riferimenti ufficiali GitHub
│   ├── cli-windows.html           # Guida 1: CLI Windows
│   ├── automation-assets.html     # Guida 1bis: Automation Assets
│   ├── agent-skills.html          # Guida 2: Agent Skills
│   └── backlog-kanban.html        # Guida 3: Backlog + Kanban
├── Guide/                         # 📁 Documenti sorgente originali
│   ├── Guida - GitHub Copilot da CLI Windows.docx
│   ├── Guida - Usare Agent Skills con GitHub Copilot.pdf
│   ├── Guida - Tecnica Backlog (+ Kanban) con GitHub Copilot.docx
│   ├── Guida Giancarlo Compagno - GitHub Copilot + Tools.html
│   └── Guida Giancarlo Compagno - GitHub Copilot + Tools_files/
├── README.md                      # Questa guida
└── PROGETTO_COMPLETATO.md        # Documentazione completamento progetto
```

### Nota sulla cartella `Guide/`

La cartella `Guide/` contiene i **documenti sorgente originali** (Word, PDF, HTML) da cui sono state estratte le guide.

**Consiglio**: **Mantienila** per:
- ✅ Riferimento ai contenuti originali
- ✅ Backup dei materiali sorgente
- ✅ Eventuali aggiornamenti futuri
- ✅ Confronto con le versioni HTML

Non è utilizzata dal sito web ma è utile come archivio dei materiali.

---

## 🚀 Come Usare

### Metodo 1: Apertura Diretta (Quick)
Doppio click su `index.html` per aprire la homepage nel browser.

### Metodo 2: Server Locale (Consigliato)

**Con Python 3:**
```bash
cd "C:\Users\alesessa\Progetti\Progetti_Personali\AMS Guide AI"
python -m http.server 8000
```
Poi visita `http://localhost:8000`

**Con Node.js:**
```bash
npx http-server
```

**Con PHP:**
```bash
php -S localhost:8000
```

---

## 🎨 Personalizzazione

### Colori
I colori sono definiti in `assets/css/styles.css` tramite variabili CSS:

```css
:root {
    --primary-color: #2563eb;      /* Blu primario */
    --secondary-color: #7c3aed;    /* Viola */
    --accent-color: #06b6d4;       /* Cyan */
    --dark-bg: #0f172a;            /* Background scuro */
    --darker-bg: #020617;          /* Background più scuro */
    --light-text: #f8fafc;         /* Testo chiaro */
    --muted-text: #cbd5e1;         /* Testo attenuato */
    --card-bg: #1e293b;            /* Background card */
    --border-color: #334155;       /* Colore bordi */
}
```

### Font
Il sito usa **Inter** da Google Fonts. Per cambiarlo, modifica l'import in ogni file HTML:

```html
<link href="https://fonts.googleapis.com/css2?family=TUO_FONT:wght@300;400;600;700&display=swap" rel="stylesheet">
```

---

## 🔗 Pagina Riferimenti

La pagina `pages/riferimenti.html` contiene tutti i link ufficiali GitHub Copilot:

- **Documentazione Generale**: Docs, Getting Started
- **CLI**: Guida uso da terminale, comandi
- **IDE**: VS Code, JetBrains, Visual Studio
- **Agent Skills**: Docs, Changelog, Guide
- **Risorse**: Blog, Changelog, Trust Center, Community

Accessibile dal menu principale: **Home | Guide | Riferimenti**

---

## 🛠️ Tecnologie Utilizzate

- **HTML5**: Struttura semantica e accessibile
- **CSS3**: Variabili CSS, Grid, Flexbox, animazioni
- **JavaScript Vanilla**: Scroll smooth, animazioni, navbar sticky
- **Google Fonts**: Tipografia professionale (Inter)

---

## 📱 Compatibilità Browser

- ✅ Chrome/Edge (90+)
- ✅ Firefox (88+)
- ✅ Safari (14+)
- ✅ Opera (76+)

---

## 📋 Checklist Contenuti

### Guide Complete
- ✅ CLI Windows (Base)
- ✅ Automation Assets (Intro parallela WSL)
- ✅ Agent Skills (Avanzata)
- ✅ Backlog + Kanban (Metodologia)

### Design
- ✅ Zero emoji (design professionale)
- ✅ Dark theme con gradients
- ✅ Responsive design
- ✅ Animazioni fluide

### Navigazione
- ✅ Homepage
- ✅ Pagina lista guide
- ✅ Pagina riferimenti
- ✅ TOC per ogni guida
- ✅ Back navigation
- ✅ Footer con link

### Contenuti Formattati
- ✅ Code blocks
- ✅ Info boxes e note boxes
- ✅ Checklist styled
- ✅ Steps list
- ✅ Tool cards
- ✅ Mini cards grid

---

## 🎯 Percorso Didattico Consigliato

### Per Principianti
1. **Inizia da**: CLI Windows (Guida 1)
2. **Poi**: Agent Skills (Guida 2) per funzionalità avanzate
3. **Infine**: Backlog + Kanban (Guida 3) per metodologia completa

### Per Utenti Linux/WSL
1. **Inizia da**: Automation Assets (Guida 1bis)
2. **Poi**: Agent Skills (Guida 2)
3. **Infine**: Backlog + Kanban (Guida 3)

### Per Team
1. **Setup base**: CLI Windows o Automation Assets
2. **Standardizzazione**: Agent Skills per comportamenti consistenti
3. **Workflow**: Backlog + Kanban per gestione progetto

---

## 🔄 Aggiornamenti Futuri

### Possibili Miglioramenti
- [ ] Funzione di ricerca nelle guide
- [ ] Toggle dark/light mode
- [ ] Download PDF delle guide
- [ ] Sistema commenti/feedback
- [ ] Versioning guide
- [ ] Supporto multilingua (EN/IT)

### Deployment
- [ ] Deploy su GitHub Pages
- [ ] Deploy su Netlify/Vercel
- [ ] Custom domain

---

## 📄 Licenza

Questo progetto è stato creato per uso interno e educativo. Le guide sono proprietà dei rispettivi autori:
- Guide base: contenuti originali
- Guida Automation Assets: Giancarlo Compagno (Engineering)

---

## 📞 Supporto

Per domande, suggerimenti o segnalazione errori:
- Apri un issue nel repository
- Contatta il team di sviluppo

---

## ✨ Crediti

**Creato con GitHub Copilot**

Guide curate e sviluppate con l'assistenza di GitHub Copilot per massimizzare produttività e qualità del codice.

---

## 📊 Statistiche Progetto

- **Guide**: 4 complete
- **Pagine HTML**: 7
- **File CSS**: 3
- **Linee di codice**: ~5000+
- **Tempo lettura totale**: ~2 ore
- **Livello copertura**: Base → Avanzato → Metodologia

---

**Versione**: 1.0  
**Data**: 13/02/2026  
**Status**: ✅ Production Ready

