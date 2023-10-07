# Workshop-DIY Post Generator — Project Prompt V6.0

## Pour réutiliser
Attachez `workshop-post-gen.html` + ce fichier. Dites: "Lis le prompt et le code, puis attends mes instructions."

---

## Identité
**Workshop-DIY** — ateliers maker/STEM enfants, Chelles 77500.
Site: workshop-diy.org · Contact: contact@workshop-diy.org / 06 19 51 51 73
GitHub: abourdim.github.io/apps/ · بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ

## App
Générateur posts Facebook. HTML unique, ~6300 lignes, ~320 KB. Zéro serveur. PWA.

### Design: Teal (#0d7377) + Or (#c9963b) + Crème (#faf6ef)
### Polices: Permanent Marker, Courier Prime, Cairo, Amiri, Tajawal, Noto Kufi Arabic

### 5 Modes
1. 🎨 Visuels (58 styles, 5 catégories)
2. 🐄 Cowsay (35 animaux × 16 fonds, solo/duo/custom/combo)
3. 💬 Chat (6 styles, max 8 bulles, FR/AR)
4. 😂 Mème (12 templates + upload image, FR/AR)
5. 📱 Notif (6 styles OS, FR/AR)

### Features
- Live preview tous les champs
- Bilingue FR/🇩🇿AR (30+30 msgs, 50+50 fortunes, 4 polices arabes, RTL, quick texts)
- Texte libre draggable (✏️), 9 polices dont 3 arabes
- Galerie (100 thumbnails) + Export/Import JSON entre machines
- PWA + Service Worker + bouton 📲
- Raccourcis: Ctrl+Enter/S/Shift+R
- QR Code drag & drop
- Batch export, favoris ⭐, thème clair/sombre
- 3 formats: carré/paysage/story
- 4 sources: intégré/manuel/Groq/Claude

### Architecture
- Vanilla JS, `var`, fonctions nommées, Canvas 2D
- `getCanvasDims()` pour dimensions
- Auto-generate: `if(postCanvas.width>0) generateXxx()`
- `oninput` sur texte, `onchange` sur select/checkbox
- Gallery: debounce 2s via `scheduleGallerySave()`
- AR fonts: `getArFont(styleId)` → Amiri/Tajawal/Cairo/Noto Kufi
- `updateLangContent()` met à jour quick texts/placeholders/noms

### Package (12 fichiers)
index.html, start_here.html, workshop-post-gen.html, README.html/.md, WIKI.html/.md, cheatsheet.html, PROJECT_PROMPT.md, CHANGELOG.md, COMMIT_MESSAGE.txt, qr-workshop-diy.png

### Règles
1. Tester JS: `node -e "new Function(js)"`
2. onclick → function existe
3. Pas de doublons
4. Tout input → auto-generate
5. Fichier unique, liens .html
6. Bumper version, re-rendre overlays après generate
7. `updateLangContent()` après changements AR
