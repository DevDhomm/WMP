# 🎵 Windows Music Player (WMP)

Lecteur audio interactif avec fonctionnalités avancées, intégré dans une application Tauri/React.

## 🎯 Fonctionnalités

- **Lecture de fichiers audio** (MP3, M4A, WAV, FLAC) depuis le dossier `~/Music`
- **Visualiseur audio temps réel** avec [audiomotion-analyzer](https://www.audiomotion.dev)
- **Gestion de playlist** :
  - Drag & Drop des pistes ([@dnd-kit](https://dndkit.com))
  - Mode aléatoire (shuffle)
  - Navigation précédent/suivant
- **Affichage des métadonnées** :
  - Cover album animée
  - Artiste & titre
  - Paroles synchronisées (via [lyrics.ovh](https://lyrics.ovh))
- **Système de thème** avec effets visuels personnalisés

## 📦 Dépendances

```bash
# Core
@tauri-apps/plugin-fs
music-metadata

# Audio
react-h5-audio-player
audiomotion-analyzer

# Drag & Drop
@dnd-kit/core
@dnd-kit/sortable
@dnd-kit/utilities
```

## 💡 Notes Techniques

- **Performance** : Utilisation de useRef pour les références audio
- **Sécurité** :
    -Les fichiers sont lus via Tauri (sandboxé)
    -Les paroles utilisent une API externe (CORS géré)
- **Animations** :
    -Transition CSS pour les covers
    -Effets de flou dynamiques

## 🚨 Limitations Connues
-  Format M4A nécessite parfois un rechargement
-  L'API lyrics.ovh a une limite de 100 req/heure
-  Le visualiseur est gourmand en ressources

## Comment utiliser

1. **Télécharger** l'application
2. Ouvrez le dossier `~/Music` et ajoutez vos fichiers audio
3. Ouvrez l'application et attendez que le lecteur audio se charge
4. Glissez-déposez des fichiers audio dans la zone de playlist
5. Utilisez les boutons de contrôle pour naviguer dans la playlist

## Comment Contribuer

1. **Cloner** le dépôt : `git clone https://github.com/DevDhomm/WMP.git`
2. **Allez dans le dossier** : `cd WMP`
3. **Installer** les dépendances : `npm install`
3. **Lancer** en mode développement : `npm run dev tauri`

## 📄 Licence

MIT - Inclure les crédits pour :
- **AudioMotion**
- **DnD Kit**
- **Iconify**

