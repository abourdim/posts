# Workshop-DIY Post Generator — Project Prompt V4.0

## Pour réutiliser ce prompt
Copiez ce fichier dans une nouvelle conversation Claude avec le fichier `workshop-post-gen.html` attaché.
Dites: "Voici le projet Workshop-DIY. Lis le prompt et le code, puis attends mes instructions."

---

## Identité du Projet

**Workshop-DIY** est une association d'ateliers maker/STEM pour enfants à **Chelles 77500** (Seine-et-Marne).
- Site: workshop-diy.org
- Contact: contact@workshop-diy.org / 06 19 51 51 73
- GitHub: abourdim.github.io/apps/
- Valeurs: éducation, maker, DIY, robotique, Arduino, impression 3D, code
- Identité islamique: بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ dans le header

## L'Application

**Générateur de posts Facebook** — fichier HTML unique, 100% client-side, zéro serveur, PWA installable.
~5850 lignes, ~300 KB. Tout est dans UN seul fichier (HTML + CSS + JS + données).

### Design System
- **Couleurs**: Teal (#0d7377) + Or (#c9963b) + Crème (#faf6ef)
- **Polices**: Permanent Marker (titres), Courier Prime (body), Cairo (arabe)
- **Style**: Géométrie islamique subtile, thème clair/sombre, responsive

### 5 Modes de Création

#### 1. 🎨 Visuels (58 styles)
Le mode principal. Posts Facebook avec texte, logo, doodles, footer.
- 5 catégories: Classique (15), Kiddy (10), Formes (10), Andalous (13), Intense (10)
- Chaque style a un renderer Canvas 2D dédié
- Grille de thumbnails live, favoris ⭐, historique Préc/Suiv (30 posts)
- Style auto (aléatoire) ou sélection manuelle

#### 2. 🐄 Cowsay (35 animaux × 16 fonds)
ASCII art en image. Style terminal/geek.
- 35 animaux définis en ASCII dans `ASCII_ANIMALS`
- 16 arrière-plans dans `COWSAY_BGS` + `COWSAY_BG_RENDERERS`
- 3 bulles: say, think, shout
- 6 formats spéciaux: terminal ($), git commit, code comment, BSOD, fortune (50 citations), none
- Modes: solo, duo (2 animaux conversation), custom ASCII, combo (ASCII sur fond visuel)
- Live preview sur chaque modification

#### 3. 💬 Chat / SMS (6 styles)
Fausses conversations de messagerie.
- Styles: iMessage, WhatsApp, Messenger, SMS, Discord, Telegram
- Max 8 bulles, swap gauche/droite, avatars emoji + noms
- Options: cadre iPhone, timestamps, typing indicator
- Auto-fill 4 messages à la première visite
- Live update: texte des bulles, noms, avatars, ajout/suppression régénèrent instantanément

#### 4. 😂 Mème (12 templates)
Mèmes classiques avec texte Impact.
- Templates: Drake, Galaxy Brain, Distracted, Bouton Rouge, Scroll, Expanding, Change My Mind, This is Fine, Success Kid, Aliens Guy, Two Buttons, Stonks
- 8 textes rapides pré-écrits Workshop-DIY
- **Upload image personnalisée** comme fond de mème
- Auto-wrap, auto-resize du texte, live preview

#### 5. 📱 Notification (6 styles OS)
Fausses notifications push.
- Styles: iOS Light/Dark, Android Light/Dark, Windows 11, macOS
- 12 icônes d'app, 6 textes rapides
- Barre d'état, ombre, 2ème notif en fond, live preview

### Fonctionnalités Transversales

- **Live Preview**: Tous les champs régénèrent l'image en temps réel
- **3 formats**: Carré 1080×1080, Paysage 1200×630, Story 1080×1920
- **Bilingue**: FR (30 msgs) / AR (20 msgs, RTL auto avec Cairo)
- **4 sources**: Intégré, Manuel, Groq (gratuit), Claude (API Anthropic)
- **IA**: Bouton "✨ IA Suggérer" dans chaque mode
- **QR Code**: Toggle, URL/couleur/taille, drag & drop
- **Texte libre (✏️)**: Texte draggable, 6 polices, couleur/taille, multi-textes, undo/clear
- **Actions**: PNG, Web Share, copie texte, régénérer, aléatoire, batch export
- **Batch**: Visuels=58, Cowsay=35, Chat=6, Mème=12, Notif=6
- **Favoris**: ⭐ persistés en localStorage
- **Aide**: Modal ❓ avec 5 onglets
- **PWA**: Manifest + Service Worker + bouton 📲
- **Raccourcis**: Ctrl+Enter (générer), Ctrl+S (PNG), Ctrl+Shift+R (aléatoire)
- **Persistance**: localStorage (thème, langue, format, favoris, QR, dernier post)

### Architecture du Code

```
HTML:
├── Header (bismillah, logo, 📲, ❓, ⚙️, 🌙)
├── Help Modal (5 onglets) + Settings Modal
├── Mode Tabs (visuels, cowsay, chat, meme, notif)
├── Sidebar (5 panels avec inputs live)
├── Canvas (#postCanvas)
├── Download Bar (PNG, Partager, Texte, ↻, 🎲, ✏️, 📦, QR)
├── Text Overlay Panel (input, color, size, font, apply, ↩, 🗑)
└── History Nav

JS:
├── State (currentMode, state{}, cowState{}, chatBubbles[], textOverlays[])
├── Data (STYLES[], MESSAGES_FR/AR[], COWSAY_ANIMALS[], MEME_TEMPLATES[], etc.)
├── Core: generate(), switchMode(), getCanvasDims(), regenerateCurrent()
├── Per-mode: generateCowsay/Chat/Meme/Notif()
├── AI: callGroq(), callClaude(), aiSuggestForMode()
├── Overlay: toggleTextOverlay(), applyTextOverlay(), renderOverlays(), undoOverlay()
├── Actions: downloadImage(), shareImage(), batchExport()
├── PWA: installPWA(), SW registration
├── Keyboard: Ctrl+Enter/S/Shift+R
└── Utils: roundRect(), wrapText(), toggleTheme/Settings/Help()
```

### Conventions de Code

- Vanilla JS pur, `var` partout, fonctions nommées
- Canvas 2D (`getContext('2d', {willReadFrequently:true})`)
- `getCanvasDims()` pour dimensions (jamais hardcoder)
- Auto-generate: `if(document.getElementById('postCanvas').width>0) generateXxx()`
- Live preview: `oninput` sur texte, `onchange` sur select/checkbox
- Text overlays: `setTimeout(renderOverlays, 50)` après generate
- Fichier unique, PWA manifest inline, SW blob URL

### Package (11 fichiers)

| Fichier | Rôle |
|---------|------|
| index.html | GitHub Pages entry (= start_here) |
| start_here.html | Landing page |
| workshop-post-gen.html | L'APP |
| README.html / .md | Doc technique |
| WIKI.html / .md | Guide utilisateur + FAQ |
| cheatsheet.html | Cheat sheet imprimable |
| PROJECT_PROMPT.md | Ce fichier |
| COMMIT_MESSAGE.txt | Git commit |
| qr-workshop-diy.png | QR code |

### Règles pour Continuer

1. Tester JS: `node -e "new Function(js)"` après chaque edit
2. Vérifier onclick → function existe
3. Pas de fonctions en double
4. Tout nouveau input/sélecteur → auto-generate
5. Fichier unique, liens .html (pas .md)
6. Bumper version dans header
7. Re-rendre overlays après generate
8. Mettre à jour docs + prompt à chaque release

### Idées V5

- Export GIF / vidéo animée
- Mode poster A4 imprimable
- Achievements / gamification
- Intégration Facebook Graph API
- Galerie de posts (sauvegarde locale)
- Mode diaporama (plusieurs slides)
