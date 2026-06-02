#  FamiliaBudget — Backend

> API REST intelligente pour la gestion de budget familial

![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688?logo=fastapi)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?logo=postgresql)
![Scikit-learn](https://img.shields.io/badge/ML-Scikit--learn-F7931E?logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-green)

---

##  Description

Backend de l'application mobile **FamiliaBudget**. Il expose une API REST sécurisée (JWT) consommée par le frontend Flutter, gère la base de données PostgreSQL et intègre des modules de Data Science pour l'analyse et la prévision budgétaire.

---

##  Architecture

```
FamiliaBudget-backend/
├── main.py                  ← Point d'entrée FastAPI
├── requirements.txt         ← Dépendances Python
├── .env                     ← Variables d'environnement
├── app/
│   ├── routers/             ← Endpoints (auth, budget, users...)
│   ├── models/              ← Modèles SQLAlchemy (PostgreSQL)
│   ├── schemas/             ← Schémas Pydantic
│   ├── services/            ← Logique métier
│   └── ml/                  ← Modules Machine Learning
│       ├── forecasting.py   ← Prévisions budgétaires
│       ├── anomaly.py       ← Détection d'anomalies
│       └── recommendations.py ← Recommandations personnalisées
└── database.py              ← Connexion PostgreSQL
```

---

##  Fonctionnalités

-  **Authentification JWT** — Register, Login, refresh token
-  **Gestion des rôles** — Admin, Utilisateur, Co-utilisateur
-  **CRUD Budget** — Dépenses, revenus, catégories
-  **Analyse financière** — Statistiques et rapports
-  **Machine Learning**
  - Prévisions budgétaires (Scikit-learn)
  - Détection d'anomalies de dépenses
  - Recommandations personnalisées
-  **Notifications** — Alertes dépassement de budget

---

##  Technologies

| Outil | Usage |
|-------|-------|
| FastAPI | Framework API REST |
| PostgreSQL | Base de données relationnelle |
| SQLAlchemy | ORM Python |
| Pydantic | Validation des données |
| JWT (python-jose) | Authentification |
| Pandas | Manipulation des données |
| Scikit-learn | Modèles ML |
| Matplotlib | Visualisation |

---

##  Installation

```bash
# Cloner le dépôt
git clone https://github.com/HayfaBouali/FamiliaBudget-backend.git
cd FamiliaBudget-backend

# Créer un environnement virtuel
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Installer les dépendances
pip install -r requirements.txt

# Configurer les variables d'environnement
cp .env.example .env
# Modifier .env avec vos paramètres PostgreSQL

# Lancer le serveur
uvicorn main:app --reload
```

---

##  Documentation API

Une fois lancé, la documentation interactive est disponible sur :
- Swagger UI : `http://localhost:8000/docs`
- ReDoc : `http://localhost:8000/redoc`

---

##  Projet lié

 [FamiliaBudget — Frontend Flutter](https://github.com/HayfaBouali/FamiliaBudget)

---

##  Auteure

**Haifa Bouali** — Étudiante en Génie Logiciel, orientée Data Science  
ESSAT Gabès, Tunisie

---

## 📄 Licence

Ce projet est sous licence [MIT](LICENSE).
