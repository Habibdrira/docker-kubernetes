# Docker & Kubernetes Lab

Ce dépôt contient les implémentations du projet "Docker-kubernetes lab pfa.pdf", couvrant Docker, Docker Compose, Kubernetes, Jenkins, SonarQube, et Gitflow. L'étape 2 implémente une application Flask conteneurisée avec Docker.

## Étape 2 : Application Flask

### Pré-requis
- Ubuntu 20.04 LTS
- Docker installé
- Git installé

### Installation
1. Cloner le dépôt :
   ```bash
   git clone https://github.com/Habibdrira/docker-kubernetes.git
   cd docker-kubernetes/etape2-flask-app
   ```
2. Construire l'image Docker :
   ```bash
   docker build -t flask-app:latest .
   ```
3. Lancer le conteneur :
   ```bash
   docker run -d -p 5000:5000 --name flask-container flask-app:latest
   ```
4. Tester l'application :
   ```bash
   curl http://localhost:5000
   ```

### Sortie attendue
```
Hello, World! This is a Flask app running in Docker.
```

### Fichiers
- `app.py` : Application Flask.
- `requirements.txt` : Dépendances (Flask==2.0.1, Werkzeug==2.0.3).
- `Dockerfile` : Instructions pour construire l'image.

## Étapes futures
Les étapes suivantes (Docker Compose, Kubernetes, Jenkins, etc.) seront ajoutées dans des dossiers dédiés (`etape3`, `etape4`, etc.).

## Licence
MIT
