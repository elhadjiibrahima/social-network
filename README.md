# Social Network Project

Bienvenue dans le projet **Social Network**, une plateforme web complète inspirée de Facebook, développée en Go pour le backend et un framework JavaScript moderne pour le frontend. Ce projet permet aux utilisateurs de créer un profil, publier des posts, rejoindre des groupes, chatter en temps réel, et bien plus encore.

## 🧠 Fonctionnalités principales

### ✅ Authentification
- Inscription avec Email, Mot de passe, Prénom, Nom, Date de naissance.
- Champs facultatifs : Avatar, Pseudo, À propos de moi.
- Connexion/Déconnexion avec sessions et cookies.

### 🧑‍🤝‍🧑 Suivi (Followers)
- Demandes de suivi avec acceptation (ou automatique pour profils publics).
- Possibilité d'accepter/refuser les demandes de suivi.

### 👤 Profil utilisateur
- Informations personnelles.
- Posts récents.
- Liste des followers et abonnements.
- Option pour rendre son profil privé/public.

### 📝 Posts
- Créer, consulter et commenter des posts.
- Types de visibilité : public, semi-privé (followers), privé (followers choisis).
- Support des images et GIFs.

### 👥 Groupes
- Créer des groupes avec titre et description.
- Invitations et demandes d’adhésion.
- Créer des posts visibles uniquement par les membres.
- Création d’événements avec réponses (Going / Not Going).

### 💬 Chat en temps réel
- Chat privé via WebSocket (autorisé si l’un suit l’autre).
- Envoi d’emoji.
- Chat de groupe commun visible par tous les membres.

### 🔔 Notifications
- Notification en cas :
  - de demande de suivi,
  - d’invitation à un groupe,
  - de demande d’adhésion à un groupe,
  - de création d’un événement dans un groupe.

---

## 🛠️ Stack technique

### Backend
- Langage : Go
- Base de données : SQLite
- Migrations : `golang-migrate`
- WebSocket : `gorilla/websocket`
- Authentification : sessions, cookies
- Hashage des mots de passe : `bcrypt`

### Frontend
- Framework : **[à préciser : React, Vue, Svelte...]**
- Communication avec l'API : HTTP / WebSocket

### Containerisation
- **Docker** pour frontend et backend
- Ports exposés :
  - Backend : `8080`
  - Frontend : `3000` (ou autre)

---

## 📁 Arborescence recommandée

```bash
.
├── backend
│   ├── server.go
│   └── pkg
│       └── db
│           ├── sqlite
│           │   └── sqlite.go
│           └── migrations
│               └── sqlite
│                   ├── 000001_create_users_table.up.sql
│                   ├── 000001_create_users_table.down.sql
│                   ├── ...
├── frontend
│   ├── public/
│   └── src/
├── docker-compose.yml
├── Dockerfile.backend
├── Dockerfile.frontend
└── README.md
