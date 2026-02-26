# Godot Audio Templates

Collection de templates audio interactifs pour Godot 4.

## 🎹 Scènes disponibles

### 1. Keyboard Synth Scene
**Fichier:** `scenes/keyboard_synth_scene.tscn`

🎥 **[Voir la démo vidéo](https://cloud.robinmoretti.eu/s/2By8NjZnKGF2dGL)**

Synthétiseur interactif avec trois lignes de contrôle au clavier.

**Contrôles:**

**Ligne 1 - Synthétiseur (génération d'ondes)**
- `A Z E R T Y U I O P` : Notes musicales (Do à La)
- Génère des ondes audio en temps réel

**Ligne 2 - Samples audio**
- `Q W D F G H J K L` : Déclenchement de samples audio (sons de pièces/monnaie)

**Ligne 3 - Effets sonores**
- `X` : Octave bas (-1 octave)
- `C` : Octave haut (+1 octave)
- `V` : Toggle vibrato (oscillation de pitch)
- `B` : Change forme d'onde (sine → square → sawtooth)
- `N` : Reset tous les effets
- `M` : Ajoute une quinte (harmonie)

### 2. Pitch Detection Scene
**Fichier:** `scenes/pitch_detection_scene.tscn`

🎥 **[Voir la démo vidéo](https://cloud.robinmoretti.eu/s/ARSD6PNPjZid5ry)**

Détection de pitch en temps réel via microphone avec contrôle d'un personnage 2D.

**Fonctionnalités:**
- Capture audio du microphone
- Analyse de fréquence en temps réel
- Contrôle d'un CharacterBody2D selon le pitch détecté
- Environnement de plateforme avec tileset

### 3. Rhythm Note Game
**Fichier:** `scenes/rythm_note_game.tscn`

🎥 **[Voir la démo vidéo](https://cloud.robinmoretti.eu/s/FbDL78Tb7YkaSLL)**

Jeu de rythme avec détection de notes au microphone.

**Fonctionnalités:**
- Spawn de notes défilantes
- Détection de pitch via microphone
- Système de détection de collision pour valider les notes
- Perfect pour un jeu type Guitar Hero vocal

### 4. Turn with Pitch Scene
**Fichier:** `scenes/turn_with_pitch_scene.tscn`

Scène simple de détection de pitch pour contrôles basiques.

**Fonctionnalités:**
- Détection de pitch microphone
- Base pour créer des interactions contrôlées par la voix

## 🔧 Configuration Audio

Le projet utilise un bus audio `Mic` configuré dans `audio/default_bus_layout.tres` pour la capture microphone.

## 📁 Structure du projet

```
godot-audio-templates/
├── scenes/           # Scènes principales
├── scripts/          # Scripts GDScript
├── prefabs/          # Prefabs réutilisables
├── audio/            # Fichiers audio et configuration
├── textures/         # Assets visuels
└── records/          # Dossier d'enregistrement vidéo
```

## 🚀 Utilisation

1. Ouvrez le projet dans Godot 4
2. Sélectionnez une des scènes dans le dossier `scenes/`
3. Lancez la scène (F5)
4. Pour la Keyboard Synth Scene, utilisez les touches du clavier
5. Pour les autres scènes, autorisez l'accès au microphone

## 🎤 Permissions microphone

Les scènes utilisant le microphone nécessitent l'autorisation d'accès au microphone système.

## 📹 Enregistrement

Pour enregistrer une session:
```bash
godot --path "chemin/vers/projet" --write-movie res://records/session.avi
```

Note: Le mode enregistrement capture uniquement en offline (pas de son en temps réel pendant l'enregistrement).

