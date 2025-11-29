# Docker LEMP Stack - Local Development Environment

Un environnement de développement local basé sur Docker avec une stack LEMP (Linux, Nginx, MySQL, PHP) et phpMyAdmin.

## 🚀 Stack Technique

- **Nginx** 1.21
- **PHP** 8.1-FPM avec extension PDO MySQL
- **MySQL** 8.0
- **phpMyAdmin** 5

## 📁 Structure du Projet
docker-lemp/
├── .docker/
│ ├── mysql/
│ │ └── my.cnf
│ ├── nginx/
│ │ └── conf.d/
│ │ └── php.conf
│ └── php/
│ └── Dockerfile
├── src/
│ └── index.php
├── .env
├── .env.example
├── .gitignore
└── docker-compose.yml

text

## ⚡ Démarrage Rapide

1. **Cloner le repository**
   ```bash
   git clone <votre-repo>
   cd docker-lemp
Configurer l'environnement

bash
cp .env.example .env
Démarrer les containers

bash
docker compose up -d
Configurer le host local
Ajouter cette ligne à /etc/hosts :

text
127.0.0.1 php.test
🌐 Accès aux Services
Application : http://php.test

phpMyAdmin : http://localhost:8080

Identifiants : root / root

Base de données : demo

🛠 Commandes Utiles
bash
# Démarrer les services
docker compose up -d

# Arrêter les services
docker compose stop

# Redémarrer les services
docker compose restart

# Voir les logs
docker compose logs -f

# Supprimer tout l'environnement
docker compose down -v --rmi all --remove-orphans

# Accéder au container PHP
docker compose exec php bash
⚙️ Configuration
Variables d'environnement (.env)
COMPOSE_PROJECT_NAME : Nom du projet Docker

Bases de données
Les données MySQL sont persistées via un volume Docker nommé.

📝 Fonctionnalités
✅ Serveur Nginx configuré pour PHP

✅ PHP 8.1 avec extensions MySQL

✅ Base de données MySQL persistante

✅ Interface phpMyAdmin

✅ Hot-reload du code source

✅ Configuration UTF-8 pour MySQL

✅ Health checks pour les dépendances

🔧 Personnalisation
Modifiez les fichiers de configuration dans le dossier .docker/ pour adapter l'environnement à vos besoins.

Basé sur le tutoriel : Docker for local web development
