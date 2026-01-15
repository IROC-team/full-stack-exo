# Full Stack Exo - FastAPI Hello World

Un projet simple de démonstration utilisant FastAPI, géré avec Pixi et Taskfile.

## Prérequis : Installation de Pixi

Ce projet utilise [Pixi](https://pixi.sh/) pour la gestion des dépendances et de l'environnement.

Si vous n'avez pas encore Pixi, vous pouvez l'installer avec la commande suivante (macOS/Linux) :

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

Pour Windows (PowerShell) :

```powershell
powershell -ExecutionPolicy Bypass -c "irm -useb https://pixi.sh/install.ps1 | iex"
```

Après l'installation, redémarrez votre terminal ou sourcez votre fichier de configuration shell (ex: `source ~/.zshrc`).

## Installation du projet

1. Clonez ce dépôt (si ce n'est pas déjà fait).
2. Installez les dépendances du projet avec Pixi :

```bash
pixi install
```

## Utilisation

Le projet utilise un `Taskfile` pour simplifier les commandes courantes. Assurez-vous d'être dans l'environnement du projet ou utilisez `pixi run`.

Pour voir toutes les tâches disponibles :

```bash
task --list
```

### Lancer le serveur

Pour démarrer le serveur de développement (avec rechargement automatique) :

```bash
task run
```
Le serveur démarrera sur le port défini dans le fichier `.env` (par défaut 8000).

### Tester l'API

Dans un autre terminal, vous pouvez tester l'endpoint `/hello` :

```bash
task request NAME=VotreNom
```

Exemple :
```bash
task request NAME=Alice
```
Cela enverra une requête à `http://localhost:8000/hello/Alice`.

### Lancer les tests

Pour exécuter les tests :

```bash
task tests
```
