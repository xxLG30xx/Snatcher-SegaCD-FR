# Snatcher – Traduction Française (SEGA-CD / Mega-CD)

Projet de traduction française du jeu **Snatcher** sur **SEGA-CD (Mega-CD)**.

Ce dépôt fait partie du **Mega-CD FR Patch Project** et se concentre exclusivement sur
la **partie technique** du projet, en particulier les **scripts Python** nécessaires
à la gestion de l’audio (conversion PCM ↔ WAV, contrôles, préparation à la réinjection).

⚠️ **Aucun fichier issu du jeu original (audio, données, images disque) n’est distribué ici.**

---

## 📌 Statut du projet

🟡 **En cours de développement**

- Traduction texte : en cours  
- Audio (voix) : analyse et adaptation en cours  
- Scripts audio : en développement / stabilisation  
- Patch public : à venir (via Releases)

---

## 🎮 Jeu concerné

- **Titre** : Snatcher  
- **Support** : SEGA-CD / Mega-CD  
- **Éditeur** : Konami  
- **Langue originale** : Japonais / Anglais  

Ce projet nécessite **une copie originale et légale du jeu**.

---

## 📂 Contenu du dépôt

Ce dépôt contient **uniquement** :

- 🛠️ **Scripts Python**
  - conversion PCM → WAV
  - conversion WAV → PCM (réinjection)
  - vérification des spécifications audio
- 📄 Documentation technique intégrée (ce README)
- 🧪 Outils d’aide au debug et à l’analyse audio

❌ **Aucun fichier WAV, PCM, ISO, BIN, CUE ou donnée protégée par copyright n’est inclus.**

---

## 🔊 Contraintes audio SEGA-CD (Snatcher)

Le moteur audio de Snatcher impose des contraintes strictes.  
Tous les scripts sont conçus pour respecter **impérativement** :

- **Mono**
- **8-bit**
- **16 000 Hz**
- **PCM brut**
- Longueur **identique à l’original**  
  - si trop long → **coupure**
  - si trop court → **padding avec silence**

⚠️ Le non-respect de ces paramètres entraîne :
- saturation
- son étouffé
- crash ou lecture incorrecte en jeu

---

## 🧰 Environnement & prérequis

- **Python** : 3.8 ou supérieur
- OS :
  - macOS (testé)
  - Linux
  - Windows

Aucune dépendance exotique n’est requise (librairies standards Python).

---

## 📁 Organisation recommandée (locale)

Exemple d’arborescence **sur ta machine** (pas dans le repo) :

