# بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ

# Workshop-DIY — Générateur de Posts V4.1

Outil multi-mode de création de visuels pour **Workshop-DIY** (Chelles 77500). Application 100% client-side, fichier HTML unique, zéro dépendance serveur. PWA installable.

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

### 🐄 Cowsay — 35 Animaux ASCII

Génère des images avec des animaux ASCII dans un style terminal/geek.

- **35 animaux**: vache, tux, robot, dragon, crâne, alien, t-rex, hibou, grenouille, poulpe, mouton, chameau, éléphant, canard, souris, chauve-souris, licorne, chat, lapin, renard, tortue, sorcier, père Noël, endormi, fou, serpent, manchot, crabe, baleine, abeille, dino, singe, fantôme, panda, perroquet
- **16 arrière-plans**: Terminal vert, Ambre CRT, Tableau noir, Blanc, Matrix, Écran bleu, Ubuntu, Hacker, C64, Game Boy, Arcade, Blueprint, Circuit, Cahier, Post-it, Craft bois
- **3 styles de bulle**: Dire, Penser, Crier
- **6 formats spéciaux**: Terminal ($), Git Commit, Code Comment, BSOD, Fortune Cookie (50 citations)
- **Mode Duo**: 2 animaux en conversation
- **ASCII personnalisé**: Collez votre propre art
- **Mode Combo**: Animal ASCII sur fond visuel (58 styles)
- **Live preview**: Chaque modification régénère instantanément

### 💬 Chat / SMS

Génère de fausses conversations de messagerie.

- **6 styles**: iMessage, WhatsApp, Messenger, SMS, Discord, Telegram
- **Personnages**: Avatar emoji + nom personnalisables (live update)
- **Messages**: Ajoutez jusqu'à 8 bulles, swap gauche/droite, édition en ligne (live)
- **Options**: Cadre téléphone (iPhone), horodatage, indicateur de frappe (...)
- **Auto-fill**: 4 messages par défaut sur le thème Workshop-DIY

### 😂 Mème

Générateur de mèmes classiques avec texte Impact.

- **12 templates**: Drake, Galaxy Brain, Distracted, Bouton Rouge, Scroll de Vérité, Expanding Brain, Change My Mind, This is Fine, Success Kid, Aliens Guy, Two Buttons, Stonks
- **8 textes rapides**: Mèmes pré-écrits Workshop-DIY (un clic pour générer)
- **Image personnalisée**: Uploadez votre propre image comme fond de mème
- **Texte Impact**: Outline noir, auto-wrap, redimensionnement automatique
- **Live preview**: Le texte se met à jour en temps réel

### 📱 Notification

Fausses notifications push réalistes.

- **6 styles OS**: iOS Light, iOS Dark, Android, Android Dark, Windows 11, macOS
- **12 icônes d'app**: 🛠️ 🤖 🚀 ⚡ 💡 🧩 🔧 🎯 📐 🔬 🎮 🏗️
- **6 textes rapides**: Premier robot, Nouvel atelier, Niveau débloqué, Rappel, Places limitées, Impression 3D
- **Live preview**: Chaque champ se met à jour instantanément

## Fonctionnalités Transversales

### Live Preview

Tous les champs de texte dans tous les modes régénèrent l'image en temps réel pendant la saisie. Plus besoin de cliquer "Générer" après chaque modification.

### Texte Libre (✏️)

Ajoutez du texte libre sur n'importe quelle image générée:
- 6 polices: Impact, Marker, Mono, Cairo, Bangers, Arial
- Couleur et taille personnalisables
- Drag & drop pour positionner
- Multi-textes supportés
- Undo (↩) et Clear (🗑)

### Raccourcis Clavier

- **Ctrl+Enter**: Générer
- **Ctrl+S**: Télécharger PNG
- **Ctrl+Shift+R**: Aléatoire

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
- **✏️ Texte libre**: Ajouter du texte draggable sur l'image
- **📦 Batch**: Export multi-styles par mode

### PWA / Installation

- Bouton 📲 dans le header (apparaît quand installable)
- Service Worker pour cache offline
- Manifest intégré, compatible Android/iOS
- Fonctionne hors ligne (sauf IA et QR)

### Favoris ⭐

- Étoile sur chaque style visuel
- Onglet "Favoris" pour accès rapide
- Persisté en localStorage

### Persistance

- Tous paramètres sauvegardés en localStorage
- Dernier post affiché au démarrage
- Historique jusqu'à 30 posts (mode Visuels)
- Position et taille du QR sauvegardées
- Favoris persistés

## Déploiement

Fichier unique `workshop-post-gen.html` (~310 KB) — aucune installation.

- **Local**: Ouvrir dans un navigateur
- **GitHub Pages**: Copier dans le repo
- **PWA**: Installer via le bouton 📲
- **Claude.ai**: Fonctionne en artifact

Les modes IA nécessitent une connexion internet et une clé API.

## Statistiques

- 5 modes de création
- 58 styles visuels + 35 animaux + 16 fonds + 12 templates mème + 6 styles chat + 6 styles notif
- 50 citations fortune cookie
- ~6150 lignes, fichier unique
- 0 dépendance serveur

## Contact

- workshop-diy.org
- contact@workshop-diy.org
- 06 19 51 51 73
- Chelles 77500
- https://abourdim.github.io/apps/

### Galerie & Export/Import

- **🖼️ Galerie**: Historique visuel des posts générés (thumbnails 200px, max 100)
- **📥 Exporter JSON**: Backup complet (settings, favoris, galerie, compteur, QR)
- **📤 Importer JSON**: Restaure sur une autre machine (fusion sans doublons)
- **🗑 Reset**: Efface toutes les données locales
- **Compteur**: Nombre total de posts générés, persisté
- Debounce 2s — ne sauvegarde pas pendant la saisie live
- Accessible via ⚙️ Paramètres → DONNÉES
