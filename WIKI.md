# Workshop-DIY — Guide d'Utilisation V4.1

## Démarrage Rapide

1. Ouvrez `workshop-post-gen.html` dans votre navigateur (ou installez via 📲)
2. Choisissez un mode: 🎨 Visuels, 🐄 Cowsay, 💬 Chat, 😂 Mème, 📱 Notif
3. Modifiez le texte — l'image se met à jour en temps réel
4. Cliquez ⬇ PNG pour télécharger ou 📤 pour partager

**Astuce**: Tout changement (texte, style, option) régénère instantanément l'image. Plus besoin de cliquer "Générer" après chaque modification!

## Mode par Mode

### 🎨 Visuels
- Tapez un sujet dans le champ "Thème du post"
- Cliquez un style dans la grille (ou laissez "Auto")
- Marquez vos favoris ⭐ et filtrez avec l'onglet "Favoris"
- Naviguez l'historique avec Préc/Suiv (30 derniers posts)

### 🐄 Cowsay
- Tapez votre message → preview live
- Cliquez un animal (35 choix) et un fond (16 choix)
- Changez bulle (Dire/Penser/Crier), format (Terminal/Git/Code/BSOD/Fortune)
- Mode Duo: 2 animaux en conversation
- Mode Combo: ASCII sur fond visuel

### 💬 Chat
- Les 4 premières bulles sont pré-remplies
- Ajoutez des bulles (← Gauche / Droite →), max 8
- Tapez dans une bulle → la conversation se met à jour en direct
- Changez les noms et avatars des personnages (live)
- Activez/désactivez cadre iPhone et timestamps

### 😂 Mème
- Tapez le texte haut/bas → preview live
- Choisissez un template (12) ou uploadez votre image (📷)
- Utilisez les textes rapides pour un mème en 1 clic

### 📱 Notif
- Remplissez titre/message/sous-texte → preview live
- Changez le style OS (6) et l'icône d'app (12)
- Utilisez les textes rapides pour une notif en 1 clic

## Texte Libre (✏️)

1. Cliquez ✏️ dans la barre d'actions
2. Tapez votre texte, choisissez police/couleur/taille
3. Cliquez "Appliquer" (ou Entrée)
4. Glissez le texte sur l'image pour le positionner
5. Ajoutez plusieurs textes, ↩ pour annuler, 🗑 pour tout effacer

## Paramètres (⚙️)

- **Format**: Carré (Facebook), Paysage (link preview), Story (Instagram)
- **Langue**: Français (30 msgs) ou Arabe (20 msgs RTL)
- **Source**: Intégré, Manuel, Groq (IA gratuite), Claude (IA Anthropic)

## Configuration IA

### Groq (gratuit)
1. Créez un compte sur groq.com
2. Copiez votre clé API
3. Collez dans Paramètres ⚙️ → Clé Groq

### Claude (Anthropic)
1. Obtenez une clé API sur console.anthropic.com
2. Collez dans Paramètres ⚙️ → Clé Claude

L'IA fonctionne dans les 5 modes via le bouton "✨ IA Suggérer".

## QR Code

1. Activez le toggle QR dans le panel Visuels
2. Personnalisez l'URL, la couleur et la taille
3. Glissez le QR sur l'image pour le positionner
4. Téléchargez le QR séparément via le bouton "QR"

## Raccourcis Clavier

- **Ctrl+Enter**: Générer/Régénérer
- **Ctrl+S**: Télécharger PNG
- **Ctrl+Shift+R**: Randomiser style

## Actions

| Bouton | Action | Détail |
|--------|--------|--------|
| ⬇ PNG | Télécharger | Fichier nommé workshop-diy-{mode}-{style}-{timestamp}.png |
| 📤 Partager | Web Share API | Mobile: partage natif / Desktop: copie clipboard |
| 📋 Texte | Copier le texte | Format Facebook avec contacts workshop-diy.org |
| ↻ | Régénérer | Relance le mode actif |
| 🎲 | Aléatoire | Randomise le style |
| ✏️ | Texte libre | Ajouter du texte draggable |
| 📦 | Batch | Exporte tous les styles du mode |

## Batch Export

| Mode | Nombre d'images |
|------|-----------------|
| Visuels | 58 (ou favoris seuls) |
| Cowsay | 35 animaux |
| Chat | 6 styles |
| Mème | 12 templates |
| Notif | 6 OS |

## Installation PWA

Le bouton 📲 apparaît dans le header quand l'app est installable.
- Android: "Ajouter à l'écran d'accueil"
- iOS: Safari → Partager → Sur l'écran d'accueil
- Desktop: Chrome → bouton installer

L'app fonctionne hors ligne (sauf IA et QR dynamique).

## FAQ

**Les paramètres sont-ils sauvegardés?**
Oui, tout est en localStorage: thème, langue, format, favoris, QR, dernier post.

**Ça marche hors ligne?**
Oui via le Service Worker (après la première visite). L'IA et les polices Google nécessitent internet.

**Comment partager sur Facebook?**
⬇ PNG → Upload directement sur Facebook. Ou 📤 Partager sur mobile.

**Mon logo ne s'affiche pas?**
Le logo est chargé depuis un SVG inline. En offline, il est déjà intégré.

**Peut-on ajouter des styles personnalisés?**
Pas encore via l'UI. Mais vous pouvez ajouter un style dans le tableau `STYLES[]` et un renderer dans `RENDERERS{}`.

**Le format Story, c'est quoi?**
1080×1920 — format vertical pour Instagram/TikTok Stories.

**Le batch export est lent?**
Normal — chaque image est rendue en Canvas puis téléchargée. 58 images ≈ 30 secondes.

**Comment utiliser l'image uploadée pour le mème?**
Mode Mème → section "Image Perso" → cliquez "📷 Uploader une image". Le template sélectionné sera remplacé par votre image.

## Raccourcis Cachés

- Clic sur un style/animal/template/icône → génère automatiquement
- Texte rapide → remplit ET génère en un clic
- Chat: clic ◀/▶ pour swap côté d'une bulle (live)
- Favoris ⭐ sur les visuels persistés entre sessions
- Ctrl+Enter depuis n'importe quel champ pour régénérer

## Galerie & Transfert

### Galerie (🖼️)
1. Ouvrez ⚙️ Paramètres
2. Cliquez "🖼️ Galerie" — le compteur montre le nombre de posts
3. Parcourez vos posts avec mode, style et date
4. Survolez pour supprimer (✕) un post individuel
5. "📥 Tout exporter" télécharge toutes les images

### Transférer entre machines
1. Sur l'ancienne machine: ⚙️ → "📥 Exporter JSON"
2. Transférez le fichier .json (email, clé USB, cloud)
3. Sur la nouvelle machine: ⚙️ → "📤 Importer JSON"
4. Tout est restauré: favoris, galerie, paramètres, compteur

### Reset
⚙️ → 🗑 supprime toutes les données locales (avec confirmation).
