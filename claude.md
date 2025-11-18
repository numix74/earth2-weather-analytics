# Claude - Guide du Projet Earth-2 Weather Analytics Blueprint

## Vue d'ensemble

Le **Earth-2 Weather Analytics Blueprint** est une implémentation de référence d'un service d'analyse de données géospatiales développé par NVIDIA. Ce projet combine plusieurs fonctionnalités de la plateforme Earth-2 de NVIDIA pour créer un système complet d'analyse météorologique accéléré par l'IA et Omniverse.

## Objectifs du Projet

Ce blueprint démontre trois capacités principales :

1. **Visualisation à grande échelle** : Utilisation de la plateforme NVIDIA Omniverse pour agréger et visualiser des données météorologiques
2. **Modèles d'IA météorologiques** : Déploiement et mise à l'échelle de modèles d'IA via les Nvidia Inference Microservices (NIMs)
3. **Fédération de données** : Framework d'adaptateurs connectant divers magasins de données partenaires et publics

## Architecture

Le projet est composé de trois composants principaux :

### 1. Earth-2 Command Center (E2CC)
- Application Omniverse Kit avec extensions
- Interface utilisateur pour la visualisation de données géospatiales
- Front-end du blueprint

### 2. Data Federation Mesh (DFM)
- Couche d'orchestration
- Traite les pipelines de différentes sources de données
- Connecte les sources de données à E2CC
- Génère les textures nécessaires

### 3. FourCastNet NIM (FCN NIM)
- Modèle d'IA météorologique
- Packagé comme Nvidia Inference Microservice
- Prévisions météorologiques mondiales

## Structure du Dépôt

```
earth2-weather-analytics/
├── docs/               # Documentation complète
├── src/                # Code source
├── e2cc/               # Extensions Earth-2 Command Center
├── deploy/             # Configuration de déploiement (Helm charts)
├── ci/                 # Configuration CI/CD
└── README.md           # Documentation principale
```

## Documentation Disponible

La documentation est organisée de manière séquentielle :

1. **[00_workflow.md](./docs/00_workflow.md)** - Vue d'ensemble du flux de travail
2. **[01_prerequisites.md](./docs/01_prerequisites.md)** - Prérequis (logiciels et matériel)
3. **[02_quickstart.md](./docs/02_quickstart.md)** - Guide de démarrage rapide
4. **[03_microk8s_deployment.md](./docs/03_microk8s_deployment.md)** - Guide de déploiement
5. **[04_omniverse_app.md](./docs/04_omniverse_app.md)** - Guide Earth-2 Command Center
6. **[05_data_federation_mesh.md](./docs/05_data_federation_mesh.md)** - Guide Data Federation Mesh
7. **[06_sequence.md](./docs/06_sequence.md)** - Diagrammes de séquence
8. **[07_troubleshooting.md](./docs/07_troubleshooting.md)** - Dépannage

## Démarrage Rapide

### Clonage du Dépôt

```bash
# Installer Git LFS
git lfs install

# Cloner le dépôt
git clone git@github.com:NVIDIA-Omniverse-blueprints/earth2-weather-analytics.git
cd earth2-weather-analytics

# S'assurer que tous les fichiers LFS sont récupérés
git lfs fetch --all
```

### Prérequis Techniques

- **Connaissances requises** :
  - Niveau intermédiaire en Python
  - Niveau intermédiaire en Docker
  - Niveau débutant en Kubernetes / Helm Charts

- **Infrastructure** :
  - GPU NVIDIA compatible
  - Kubernetes (recommandé : MicroK8s)
  - Accès aux NIMs NVIDIA

## Capacités de Visualisation

Le blueprint peut générer plusieurs types de visualisations :

- Analyse multivariée des données météorologiques
- Visualisation de données régionales
- Rendu RTX haute qualité
- Modèles de vent et température
- Précipitations et autres variables atmosphériques

## Sécurité et Déploiement

⚠️ **Avertissement** : Ce blueprint est fourni "tel quel" comme référence. Pour un déploiement en production :

- Faites réviser les risques et menaces potentielles par des experts en sécurité
- Définissez les limites de confiance
- Implémentez les capacités de journalisation et de surveillance
- Sécurisez les canaux de communication
- Intégrez l'authentification et l'autorisation avec des contrôles d'accès appropriés
- Maintenez le déploiement à jour
- Assurez-vous que les conteneurs/code source sont sécurisés et exempts de vulnérabilités connues

## Licence

Ce projet est fourni sous la licence Omniverse License Agreement. Consultez [LICENSE.md](./LICENSE.md) pour le texte complet de la licence.

## Technologies Utilisées

- **Plateforme** : NVIDIA Omniverse
- **IA** : FourCastNet NIM
- **Conteneurisation** : Docker
- **Orchestration** : Kubernetes / Helm
- **Langage principal** : Python
- **Visualisation** : Omniverse Kit

## Support et Contribution

Ce blueprint est conçu spécifiquement pour les développeurs souhaitant construire leurs propres systèmes météorologiques/climatiques accélérés par l'IA.

Pour toute question ou contribution, référez-vous aux guides de documentation fournis dans le dossier `docs/`.
