# بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ

# Workshop-DIY — Générateur de Posts V3.0

Outil multi-mode de création de visuels pour **Workshop-DIY** (Chelles 77500). Application 100% client-side, fichier HTML unique, zéro dépendance serveur.

## 5 Modes de Création

### 🎨 Visuels — 58 Styles

Le mode principal. Génère des visuels Facebook professionnels avec texte, logo, doodles et pied de page.

| Catégorie | Nb | Exemples |
|-----------|-----|----------|
| **Classique** | 15 | Journal, Tableau Noir, Blueprint, Polaroid, Fiche Recette... |
| **Kiddy** | 10 | Lego, Scratch, Crayon, Comic, Puzzle, Chasse au Trésor... |
| **Formes** | 10 | Robot, Fusée, Ampoule, Cerveau, Main, Arbre... |
| **Andalous** | 13 | Alhambra, Arabesque, Zellige, Astrolabe, Moucharabieh... |
| **Intense** | 10 | Acier Brossé, Flammes, Camouflage, Neon City, Béton Brut... |

Fonctions: style auto/manuel, thumbnails live, filtres par catégorie, favoris ⭐, historique Préc/Suiv.

### 🐄 Cowsay — ASCII Art

Génère des images avec des animaux ASCII dans un style terminal/geek.

- **25 animaux**: vache, tux, robot, dragon, crâne, alien, t-rex, hibou, grenouille, poulpe, mouton, chameau, éléphant, canard, souris, chauve-souris, licorne, chat, lapin, renard, tortue, sorcier, père Noël, vache endormie, vache folle
- **16 arrière-plans**: Terminal vert, Ambre CRT, Tableau noir, Blanc, Matrix, Écran bleu, Ubuntu, Hacker, C64, Game Boy, Arcade, Blueprint, Circuit, Cahier, Post-it, Craft bois
- **3 styles de bulle**: Dire, Penser, Crier
- **6 formats spéciaux**: Terminal ($), Git Commit, Code Comment, BSOD, Fortune Cookie (50 citations)
- **Mode Duo**: 2 animaux en conversation
- **ASCII personnalisé**: Collez votre propre art
- **Mode Combo**: Animal ASCII sur fond visuel (58 styles)

### 💬 Chat / SMS

Génère de fausses conversations de messagerie.

- **6 styles**: iMessage, WhatsApp, Messenger, SMS, Discord, Telegram
- **Personnages**: Avatar emoji + nom personnalisables pour chaque côté
- **Messages**: Ajoutez jusqu'à 8 bulles, swap gauche/droite, édition en ligne
- **Options**: Cadre téléphone (iPhone), horodatage, indicateur de frappe (...)
- **Auto-fill**: 4 messages par défaut sur le thème Workshop-DIY

### 😂 Mème

Générateur de mèmes classiques avec texte Impact.

- **8 templates**: Drake, Galaxy Brain, Distracted, Bouton Rouge, Scroll de Vérité, Expanding Brain, Change My Mind, This is Fine
- **8 textes rapides**: Mèmes pré-écrits Workshop-DIY (un clic pour générer)
- **Texte Impact**: Outline noir, auto-wrap, redimensionnement automatique

### 📱 Notification

Fausses notifications push réalistes.

- **6 styles OS**: iOS Light, iOS Dark, Android, Android Dark, Windows 11, macOS
- **12 icônes d'app**: 🛠️ 🤖 🚀 ⚡ 💡 🧩 🔧 🎯 📐 🔬 🎮 🏗️
- **6 textes rapides**: Premier robot, Nouvel atelier, Niveau débloqué, Rappel, Places limitées, Impression 3D
- **Réalisme**: Barre d'état, ombre, timestamp "maintenant", 2ème notification en fond

## Fonctionnalités Transversales

### Contenu Bilingue FR/AR

- 30 messages intégrés en français, 20 en arabe littéraire (فصحى)
- Rendu RTL automatique avec police Cairo
- Basculement via Paramètres ⚙️

### 4 Sources de Contenu

- **📦 Intégré**: Messages pré-écrits avec correspondance par sujet
- **✏️ Manuel**: Saisie libre du titre, message et CTA
- **🤖 Groq**: Génération IA via API Groq (clé gratuite sur groq.com)
- **✨ Claude**: Génération IA via API Anthropic

L'IA fonctionne dans les 5 modes: bouton "✨ IA Suggérer" pour cowsay, chat, mème et notif.

### 3 Formats d'Export

- **◻ Carré**: 1080×1080 (Facebook, Instagram)
- **▭ Paysage**: 1200×630 (Facebook link preview)
- **▯ Story**: 1080×1920 (Instagram/TikTok Stories)

### QR Code Intégré

- Toggle on/off, URL personnalisable
- Couleur au choix, taille ajustable (5–25%)
- Drag and drop sur le canvas
- Téléchargement séparé

### Actions

- **⬇ PNG**: Télécharger (nom de fichier inclut mode + style)
- **📤 Partager**: Web Share API (mobile) / copie clipboard (desktop)
- **📋 Texte**: Copie formatée pour Facebook avec contacts
- **↻ Régénérer**: Relance le mode actif
- **🎲 Aléatoire**: Randomise le style du mode actif
- **📦 Batch**: Export multi-styles par mode

### Favoris ⭐

- Étoile sur chaque style visuel
- Onglet "Favoris" pour accès rapide
- Persisté en localStorage

### Interface

- Thème clair par défaut (teal + or, inspiration islamique), toggle sombre
- 5 onglets de mode dans le header
- Paramètres dans modal flottant
- Input + Générer sticky en haut de chaque mode
- Auto-génération au clic sur style/animal/template
- Bismillah en calligraphie dans le header

### Persistance

- Tous paramètres sauvegardés en localStorage
- Dernier post affiché au démarrage
- Historique jusqu'à 30 posts (mode Visuels)
- Position et taille du QR sauvegardées
- Favoris persistés

## Déploiement

Fichier unique `workshop-post-gen.html` (273 KB) — aucune installation.

- **Local**: Ouvrir dans un navigateur
- **GitHub Pages**: Copier dans le repo
- **Claude.ai**: Fonctionne en artifact

Les modes IA nécessitent une connexion internet et une clé API.

## Statistiques

- 5 modes de création
- 58 styles visuels + 25 animaux + 16 fonds + 8 templates + 6 styles chat + 6 styles notif
- 50 citations fortune cookie
- ~5300 lignes, fichier unique
- 0 dépendance serveur

## Contact

- workshop-diy.org
- contact@workshop-diy.org
- 06 19 51 51 73
- Chelles 77500
- https://abourdim.github.io/apps/
