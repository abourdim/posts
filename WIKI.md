# Workshop-DIY Post Generator — Wiki

## Guide Rapide

### Premier Lancement

1. Ouvrez `workshop-post-gen.html` dans votre navigateur
2. Vous êtes sur l'onglet 🎨 Visuels par défaut
3. Tapez un sujet dans le champ "Sujet / Idée" (ex: "Arduino pour débutants")
4. Cliquez **GÉNÉRER LE POST**
5. Téléchargez avec **⬇ PNG**

### Changer de Mode

Les 5 onglets en haut permettent de basculer entre les modes. Chaque mode a sa propre interface dans la barre latérale gauche et partage la même zone d'aperçu à droite.

## Mode par Mode

### 🎨 Visuels

Le mode principal pour créer des posts Facebook professionnels.

**Workflow type:**
1. Entrez un sujet
2. Choisissez un style dans la grille (ou cochez "Auto" pour un choix aléatoire)
3. Cliquez Générer
4. Naviguez avec Préc/Suiv pour revoir l'historique

**Favoris:** Cliquez l'étoile ☆ en haut à droite de chaque carte de style pour le marquer comme favori. Utilisez le filtre "⭐ Favoris" pour ne voir que vos styles préférés.

**Style auto:** Quand "Auto" est coché, chaque génération choisit un style aléatoire.

### 🐄 Cowsay

**Workflow type:**
1. Tapez un message
2. Choisissez un animal et un arrière-plan
3. Le post se régénère automatiquement quand vous changez d'animal ou de fond
4. Optionnel: changez le style de bulle (Dire/Penser/Crier)
5. Optionnel: choisissez un format spécial (Terminal, Git, Code, BSOD, Fortune)

**Mode Duo:** Cliquez "🐄💬🐧 Duo" pour activer la conversation à 2 animaux. Un champ de réponse et un sélecteur de 2ème animal apparaissent.

**ASCII Perso:** Cliquez "✏️ ASCII perso" pour coller votre propre art ASCII. La bulle de texte s'affiche au-dessus.

**Mode Combo:** Cliquez "🎨 Combo Visuel" pour utiliser un des 58 fonds visuels au lieu des 16 fonds terminal. L'ASCII s'affiche en vert lumineux avec un overlay sombre.

### 💬 Chat / SMS

**Workflow type:**
1. Les 4 messages par défaut sont pré-remplis à la première visite
2. Modifiez les textes directement dans les champs
3. Ajoutez des bulles avec "← Gauche" ou "Droite →"
4. Cliquez ◀/▶ pour changer le côté d'une bulle
5. Changez les avatars et noms des personnages en haut
6. Choisissez un style (iMessage, WhatsApp, etc.)

**Cadre téléphone:** Active/désactive le cadre iPhone avec notch autour de la conversation.

**Limite:** Maximum 8 bulles par conversation.

### 😂 Mème

**Workflow type:**
1. Tapez le texte du haut et du bas
2. Choisissez un template
3. OU cliquez un texte rapide pour remplir et générer en un clic

**Textes rapides:** 8 mèmes pré-écrits sur le thème Workshop-DIY. Un clic remplit les champs ET génère l'image.

### 📱 Notification

**Workflow type:**
1. Remplissez titre, message et sous-texte
2. Choisissez un style OS
3. Choisissez une icône d'app
4. OU cliquez un texte rapide

## Paramètres (⚙️)

Accessible via l'icône engrenage dans le header.

- **Format:** Carré (1080×1080), Paysage (1200×630), Story (1080×1920)
- **Langue:** Français / العربية (change les messages intégrés et le rendu RTL)
- **Source:** Intégré, Manuel, Groq (IA), Claude (IA)

## Utiliser l'IA

1. Ouvrez ⚙️ Paramètres
2. Choisissez "🤖 Groq" ou "✨ Claude"
3. Entrez votre clé API
4. Le bouton "✨ IA Suggérer" apparaît dans chaque mode
5. En mode Visuels, la génération utilise l'IA automatiquement

**Groq est gratuit:** Créez un compte sur groq.com/console et copiez votre clé API.

## QR Code

1. Dans la barre latérale (mode Visuels), cochez "☑ QR Code"
2. Personnalisez l'URL, la couleur et la taille
3. Glissez le QR sur l'image pour le positionner
4. Le bouton "QR" apparaît dans la barre d'actions pour télécharger le QR seul

## Actions

| Bouton | Action | Fonctionne dans |
|--------|--------|-----------------|
| ⬇ PNG | Télécharge l'image | Tous les modes |
| 📤 Partager | Partage via Web Share API (mobile) ou copie dans le presse-papier | Tous |
| 📋 Texte | Copie le texte formaté + contacts pour coller sur Facebook | Tous |
| ↻ | Régénère avec les mêmes paramètres | Tous |
| 🎲 | Randomise le style/animal/template | Tous |
| 📦 | Batch export (toutes les variantes du mode) | Tous |
| QR | Télécharge le QR code seul | Visuels |

## Export Batch

Le bouton 📦 exporte automatiquement toutes les variantes:

- **Visuels:** 58 images (une par style)
- **Cowsay:** 25 images (une par animal)
- **Chat:** 6 images (une par style de messagerie)
- **Mème:** 8 images (une par template)
- **Notif:** 6 images (une par style OS)

## FAQ

**Q: Mes paramètres sont perdus quand je ferme le navigateur?**
Non, tout est sauvegardé en localStorage. Vos réglages, favoris, dernier post et position QR sont restaurés au prochain lancement.

**Q: L'IA ne fonctionne pas?**
Vérifiez que votre clé API est correcte et que vous avez une connexion internet. Groq est gratuit, Claude nécessite un abonnement API.

**Q: Comment ajouter un nouveau style?**
Les styles sont définis dans le code JavaScript. Ajoutez une entrée dans le tableau STYLES et un renderer dans RENDERERS.

**Q: Le batch export télécharge trop de fichiers?**
Chaque fichier est téléchargé individuellement. Votre navigateur peut demander l'autorisation pour les téléchargements multiples.

**Q: Comment utiliser le mode Story?**
Ouvrez ⚙️ Paramètres, choisissez "▯ Story (1080×1920)". Le format s'applique à tous les modes.

**Q: Puis-je utiliser cet outil hors ligne?**
Oui, sauf pour les modes IA (Groq/Claude) et le QR code personnalisé qui nécessitent internet.

**Q: Comment partager sur Facebook?**
Méthode 1: Téléchargez le PNG et uploadez-le manuellement.
Méthode 2: Sur mobile, utilisez le bouton 📤 Partager.
Méthode 3: Copiez le texte avec 📋 Texte et collez-le dans votre post.

**Q: Le logo ne s'affiche pas?**
Le logo est chargé depuis abourdim.github.io. Si vous êtes hors ligne, il sera masqué automatiquement.

## Raccourcis

- Cliquer sur un style/animal/template: régénère automatiquement
- Textes rapides (Mème/Notif): remplissent ET génèrent en un clic
- Mode Chat: première visite auto-remplit 4 messages
- ◀/▶ sur une bulle chat: swap côté gauche/droite
