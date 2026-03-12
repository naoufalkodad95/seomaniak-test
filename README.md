# README - Test Technique Seomaniak
## Gestion de Contacts - Application Full Stack

---

## 📋 APERÇU DU PROJET
Application full stack de gestion de contacts combinant :

- **Backend API** : Laravel (CRUD contacts)  
- **Frontend Dashboard** : React (Interface utilisateur)  
- **Communication** : API REST avec Axios  

---

## 🏗️ ARCHITECTURE TECHNIQUE
```
┌─────────────────┐      ┌─────────────────┐      ┌─────────────────┐
│                 │      │                 │      │                 │
│    React App    │ <--> │   API REST      │ <--> │  Base de        │
│   (Port 5173)   │      │  (Port 8000)    │      │  Données        │
│                 │      │                 │      │                 │
└─────────────────┘      └─────────────────┘      └─────────────────┘
         │                        │
         │                        │
    ┌────▼────┐              ┌────▼────┐
    │Contact  │              │Laravel  │
    │Form     │              │Contact  │
    │List     │              │Controller│
    │Card     │              │Model    │
    └─────────┘              └─────────┘
```

---

## 🛠️ STACK TECHNIQUE DÉTAILLÉE

### Backend - Laravel 10
| Technologie | Version | Utilisation |
|------------|---------|-------------|
| PHP        | 8.1+    | Langage principal |
| Laravel    | 10.x    | Framework PHP |
| MySQL/SQLite | -     | Base de données |
| Eloquent ORM | -     | Gestion des modèles |
| Laravel CORS | -     | Sécurité cross-origin |

### Frontend - React
| Technologie | Version | Utilisation |
|------------|---------|-------------|
| React          | 18.2+ | Bibliothèque UI |
| Vite           | 4.4+  | Build tool rapide |
| Axios          | 1.6+  | Client HTTP |
| React Hook Form| 7.47+ | Gestion formulaires |
| CSS3           | -     | Styling responsive |

---

## 📁 STRUCTURE DU PROJET
```
seomaniak-test/
│
├── seomaniak-backend/           # Projet Laravel
│   ├── app/
│   │   ├── Http/
│   │   │   ├── Controllers/
│   │   │   │   └── Api/
│   │   │   │       └── ContactController.php
│   │   │   └── Kernel.php
│   │   └── Models/
│   │       └── Contact.php
│   ├── database/
│   │   ├── migrations/
│   │   │   └── [date]_create_contacts_table.php
│   │   └── seeders/
│   ├── routes/
│   │   └── api.php
│   ├── config/
│   │   └── cors.php
│   └── .env
│
└── seomaniak-frontend/          # Projet React
    ├── src/
    │   ├── components/
    │   │   ├── ContactForm.jsx
    │   │   ├── ContactList.jsx
    │   │   └── ContactCard.jsx
    │   ├── services/
    │   │   └── contactService.js
    │   ├── App.jsx
    │   ├── App.css
    │   └── main.jsx
    ├── index.html
    └── package.json
```

---

## 🚀 INSTALLATION ET EXÉCUTION

### Prérequis
- PHP 8.1+  
- Composer  
- Node.js 18+  
- MySQL (optionnel, SQLite possible)  

### 1️⃣ Backend Laravel
```bash
# Accéder au dossier backend
cd seomaniak-backend

# Installer les dépendances PHP
composer install

# Configurer l'environnement
cp .env.example .env

DB_CONNECTION=mysql
DB_HOST=127.0.0.1      # ou localhost si MySQL local
DB_PORT=3306
DB_DATABASE=nom_de_ta_base
DB_USERNAME=ton_user_mysql
DB_PASSWORD=ton_mdp_mysql

# Générer la clé d’application Laravel
php artisan key:generate

# Lancer les migrations
php artisan migrate

# Démarrer le serveur
php artisan serve
```
> API disponible sur http://localhost:8000

### 2️⃣ Frontend React
```bash
# Accéder au dossier frontend
cd seomaniak-frontend

# Installer les dépendances Node
npm install

# Lancer l'application en développement
npm run dev
```
> Application disponible sur http://localhost:5173

---

## 📡 ENDPOINTS API
| Méthode | URL | Description | Corps de la requête |
|---------|-----|-------------|-------------------|
| GET     | /api/contacts          | Liste tous les contacts | - |
| GET     | /api/contacts/{id}     | Détail d'un contact     | - |
| POST    | /api/contacts          | Créer un contact        | {nom, prenom, email, telephone} |
| PUT     | /api/contacts/{id}     | Modifier un contact     | {nom, prenom, email, telephone} |
| DELETE  | /api/contacts/{id}     | Supprimer un contact    | - |

---

## 💻 FONCTIONNALITÉS IMPLÉMENTÉES

### Backend (Laravel)
- ✅ Modèle Contact avec validation  
- ✅ Contrôleur API RESTful complet  
- ✅ Gestion des erreurs 404  
- ✅ Réponses JSON structurées  
- ✅ Validation des données entrantes  
- ✅ Configuration CORS pour React  

### Frontend (React)
- ✅ Dashboard utilisateur responsive  
- ✅ Formulaire avec validation (React Hook Form)  
- ✅ Liste des contacts en temps réel  
- ✅ Modification de contact (pré-remplissage)  
- ✅ Suppression avec confirmation  
- ✅ États de chargement et d'erreur  
- ✅ Interface moderne et intuitive  

---

## 🎨 Captures d'écran

### Dashboard principal - Vue d'ensemble
![Dashboard](capture/dashboard.png)

### Formulaire d'ajout - Création d'un nouveau contact
![Ajout Contact](capture/ajoute.png)

### Liste des contacts - Affichage de tous les contacts
![Liste Contacts](capture/liste.png)

### Édition de contact - Formulaire pré-rempli
![Édition Contact](capture/modif.png)

### Confirmation suppression - Dialogue de confirmation
![Suppression Contact](capture/supp.png)



---

## 💡 CE QUE J'AI APPRIS
- Communication API REST via Axios  
- Gestion d'état React (useState, useEffect)  
- Validation de formulaires avec React Hook Form  
- Architecture MVC Laravel  
- CORS et sécurité cross-origin  
- UX/UI : Interface intuitive et responsive  

---

## 🔧 AMÉLIORATIONS POSSIBLES

### Court terme
- 🔐 Authentification (JWT / Laravel Sanctum)  
- 🔍 Recherche et filtrage des contacts  
- 📱 PWA (Progressive Web App)  
- 🌙 Mode sombre  

### Moyen terme
- 📎 Upload de photos de profil  
- 📊 Statistiques dashboard  
- 📧 Notifications email  
- 🔄 Pagination  

### Long terme
- 🗺️ Géolocalisation des contacts  
- 📅 Intégration calendrier  

---

## ⚠️ POINTS D'ATTENTION
- Les deux serveurs (backend + frontend) doivent tourner simultanément  
- Vérifier la configuration CORS si problèmes de connexion  
- Les ports 8000 (Laravel) et 5173 (React) doivent être libres  
- Pour MySQL, créer la base avant les migrations  

---


## 👨‍💻 Auteur
- Nom : NaoufalKodad  
- GitHub : [https://github.com/naoufalkodad95/seomaniak-test-user-dashboard)  
- Email : naoufalkodad@gmail.com  

---

