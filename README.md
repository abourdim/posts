# بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ

# Workshop-DIY — Générateur de Posts V2.2

Outil de création de visuels Facebook pour **Workshop-DIY** (Chelles 77500). Application 100% client-side, fichier HTML unique, zéro dépendance serveur.

## Fonctionnalités

### 58 Styles Visuels

| Catégorie | Nb | Exemples |
|-----------|-----|----------|
| **Classique** | 15 | Journal, Tableau Noir, Blueprint, Polaroid, Fiche Recette... |
| **Kiddy** | 10 | Lego, Scratch, Crayon, Comic, Puzzle, Chasse au Trésor... |
| **Formes** | 10 | Robot, Fusée, Ampoule, Cerveau, Main, Arbre... |
| **Andalous** | 13 | Alhambra, Arabesque, Zellige Joyeux, Astrolabe STEM, Moucharabieh Lumière... |
| **Intense** | 10 | Acier Brossé, Flammes, Camouflage, Neon City, Béton Brut, Heure Dorée... |

### Contenu Bilingue FR/AR

- 30 messages intégrés en français
- 20 messages en arabe littéraire (فصحى)
- Rendu RTL automatique avec police Cairo
- Basculement via ⚙️ Paramètres

### Sources de Contenu

- **📦 Intégré** — Messages pré-écrits avec correspondance par sujet
- **✏️ Manuel** — Saisie libre du titre, message et CTA
- **🤖 Groq** — Génération IA via API Groq (clé requise)
- **✨ Claude** — Génération IA via API Anthropic (clé requise)

### QR Code Intégré

- Toggle on/off dans la barre latérale
- URL personnalisable (défaut: workshop-diy.org)
- Couleur au choix via color picker
- Taille ajustable par slider (5%–25%)
- Positionnement par drag and drop sur le canvas
- Téléchargement séparé via bouton QR

### Interface

- Thème clair par défaut (palette teal et or, inspiration islamique)
- Toggle clair/sombre dans le header
- Paramètres dans modal flottant (Format, Langue, Source)
- Barre latérale : Sujet, Générer, Styles avec thumbnails live
- Filtres par catégorie avec accents colorés
- Aperçu sticky à droite
- Bismillah en calligraphie dans le header

### Persistance et Historique

- Tous les paramètres sauvegardés en localStorage
- Dernier post affiché au démarrage
- Historique de navigation Préc / Suiv (jusqu'à 30 posts)
- Click sur un style = re-rendu automatique
- Position et taille du QR sauvegardées

### Actions

- **PNG** — Télécharger l'image
- **Texte** — Copier le texte formaté pour Facebook (titre + message + CTA + contacts)
- **Régénérer** — Nouveau contenu, même style
- **Style** — Style aléatoire
- **Batch** — Export multi-styles
- **QR** — Télécharger le QR code seul

## Déploiement

Fichier unique `workshop-post-gen.html` — aucune installation requise.

- **Local** : Ouvrir dans un navigateur
- **GitHub Pages** : Copier dans le repo
- **Claude.ai** : Fonctionne en artifact

Les modes IA (Groq/Claude) nécessitent une connexion internet et une clé API.

## Contact

- workshop-diy.org
- contact@workshop-diy.org
- 06 19 51 51 73
- Chelles 77500
- https://abourdim.github.io/apps/
