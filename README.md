# 🎵 Music Player Component

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

Performance : Utilisation de useRef pour les références audio
Sécurité :
  Les fichiers sont lus via Tauri (sandboxé)
  Les paroles utilisent une API externe (CORS géré)
Animations :
  Transition CSS pour les covers
  Effets de flou dynamiques

## 🚨 Limitations Connues
  Format M4A nécessite parfois un rechargement
  L'API lyrics.ovh a une limite de 100 req/heure
  Le visualiseur est gourmand en ressources

## 📄 Licence

MIT - Inclure les crédits pour :
  AudioMotion
  DnD Kit
  Iconify

