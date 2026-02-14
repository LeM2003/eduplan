# 🎓 EduPlan - Dashboard Éducatif Multi-Utilisateur

<div align="center">

![EduPlan](https://img.shields.io/badge/EduPlan-Education_Dashboard-4F46E5?style=for-the-badge)
[![Status](https://img.shields.io/badge/Status-In_Development-yellow?style=for-the-badge)](https://github.com/LeM2003/eduplan)
[![Year](https://img.shields.io/badge/Year-2024-blue?style=for-the-badge)](https://github.com/LeM2003/eduplan)

**Système de gestion éducative pour le suivi pédagogique multi-utilisateur**

[🐛 Signaler un bug](https://github.com/LeM2003/eduplan/issues) • [💡 Proposer une fonctionnalité](https://github.com/LeM2003/eduplan/issues)

</div>

---

## 📋 À propos

**EduPlan** est un dashboard éducatif développé pour faciliter la gestion et le suivi pédagogique au sein d'établissements d'enseignement. Ce projet personnel de 2024 démontre mes compétences en développement backend, gestion de bases de données et création de systèmes multi-utilisateurs.

### 🎯 Objectif du Projet

Créer une plateforme centralisée permettant à différents acteurs (administrateurs, enseignants, étudiants) de :
- Suivre les performances académiques
- Gérer les données pédagogiques
- Générer des rapports automatisés
- Visualiser les métriques de réussite

---

## ✨ Fonctionnalités Principales

### 👥 Gestion Multi-Utilisateur
- **Système d'authentification** sécurisé avec gestion de rôles
- **Trois niveaux d'accès** :
  - 🔴 **Administrateur** : Contrôle total, gestion des utilisateurs, configuration système
  - 🟡 **Enseignant** : Saisie de notes, suivi de classe, génération de rapports
  - 🟢 **Étudiant** : Consultation de notes, suivi de progression

### 📊 Tableaux de Bord Personnalisés
- **Dashboard Admin** : Vue d'ensemble de l'établissement, statistiques globales
- **Dashboard Enseignant** : Gestion de classes, saisie de notes, suivi individuel
- **Dashboard Étudiant** : Consultation de notes, progression, objectifs

### 📈 Reporting Automatisé
- **Extraction automatique** de métriques de performance
- **Génération de rapports** par classe, par étudiant, par matière
- **Visualisations graphiques** pour faciliter l'analyse
- **Export de données** pour traitement externe

### 📚 Gestion des Données Pédagogiques
- Gestion des **classes et groupes**
- Gestion des **matières et modules**
- Suivi des **notes et évaluations**
- Historique complet des performances

### 🔒 Sécurité & Permissions
- **Authentification** robuste
- **Système de permissions** granulaire par rôle
- **Isolation des données** : chaque utilisateur voit uniquement ses données
- **Audit trail** : traçabilité des actions

---

## 🛠️ Technologies Utilisées

### Backend
- **PHP** - Logique applicative et gestion serveur
- **MySQL** - Base de données relationnelle pour stockage des données
- **PDO** - Requêtes préparées sécurisées

### Frontend
- **HTML5 / CSS3** - Structure et design
- **JavaScript** - Interactivité et validations
- **Chart.js** _(possiblement)_ - Visualisations de données

### Architecture
- **Architecture Backend** structurée
- **Séparation des responsabilités**
- **Gestion des flux de données** optimisée

---

## 📊 Modèle de Données

### Entités Principales

```
┌─────────┐
│  USERS  │──────► Administrateurs, Enseignants, Étudiants
└─────────┘
     │
     ├──────► ┌──────────┐
     │        │ CLASSES  │
     │        └──────────┘
     │
     ├──────► ┌──────────┐
     │        │ SUBJECTS │ (Matières)
     │        └──────────┘
     │
     └──────► ┌─────────┐
              │ GRADES  │ (Notes)
              └─────────┘
```

### Flux de Données

1. **Enseignant** saisit les notes dans le système
2. Les données sont **validées et stockées** dans la base MySQL
3. Le système **calcule automatiquement** les moyennes et statistiques
4. Les **rapports sont générés** et accessibles selon les permissions
5. Les **étudiants peuvent consulter** leurs résultats

---

## 🎯 Cas d'Usage

### Pour les Administrateurs
- Vue d'ensemble complète de l'établissement
- Gestion des utilisateurs (création, modification, suppression)
- Génération de rapports globaux
- Configuration du système

### Pour les Enseignants
- Gestion de leurs classes
- Saisie et modification de notes
- Génération de bulletins
- Suivi individuel des étudiants
- Communication avec les étudiants

### Pour les Étudiants
- Consultation de leurs notes en temps réel
- Visualisation de leur progression
- Accès à leur historique académique
- Suivi de leurs objectifs

---

## 💡 Compétences Démontrées

Ce projet met en avant ma maîtrise de :

✅ **Architecture Backend** - Conception de systèmes complexes  
✅ **Sécurité & Authentification** - Gestion des accès et permissions  
✅ **Bases de Données** - Modélisation, optimisation, requêtes avancées  
✅ **Gestion Multi-Utilisateur** - Isolation des données, rôles  
✅ **Reporting & Analytics** - Extraction et visualisation de métriques  
✅ **UX Multi-Rôle** - Interfaces adaptées à chaque type d'utilisateur

---

## 🚀 Installation

### Prérequis
- PHP 7.4 ou supérieur
- MySQL 8.0 ou supérieur
- Serveur web (Apache/Nginx)

### Étapes d'Installation

> ⚠️ **Note** : Le code source sera publié prochainement après refactoring.

```bash
# 1. Cloner le projet
git clone https://github.com/LeM2003/eduplan.git
cd eduplan

# 2. Configurer la base de données
# Importer le fichier database/eduplan.sql

# 3. Configurer la connexion
# Éditer config/database.php avec vos informations

# 4. Lancer le serveur
# Avec WAMP/XAMPP : Placer dans htdocs/www
# Ou : php -S localhost:8000

# 5. Accéder à l'application
# http://localhost/eduplan
```

---

## 🗺️ Roadmap

### Version Actuelle (v1.0 - Développement)
- ✅ Architecture backend complète
- ✅ Système d'authentification multi-rôle
- ✅ Gestion des utilisateurs
- ✅ Saisie et consultation de notes
- ✅ Rapports de base

### Prochaines Améliorations

#### Court Terme
- [ ] Publication du code source
- [ ] Documentation technique complète
- [ ] Guide d'installation détaillé
- [ ] Tests unitaires

#### Moyen Terme
- [ ] **Module de messagerie** entre enseignants et étudiants
- [ ] **Gestion d'emploi du temps**
- [ ] **Système de notifications** par email
- [ ] **Tableau de bord temps réel** avec WebSockets
- [ ] **Export PDF** des bulletins

#### Long Terme
- [ ] **Application mobile** pour étudiants
- [ ] **API REST** pour intégrations tierces
- [ ] **Analyses prédictives** avec Machine Learning
- [ ] **Gestion des absences et retards**
- [ ] **Plateforme de cours en ligne** intégrée

---

## 📸 Aperçu

> 📌 **Note** : Des captures d'écran seront ajoutées prochainement lors de la publication du code.

### Interface Planifiée

- **Dashboard Administrateur** - Vue d'ensemble statistiques
- **Dashboard Enseignant** - Gestion de classes
- **Dashboard Étudiant** - Consultation notes
- **Module de Saisie** - Interface de saisie de notes
- **Rapports** - Génération de bulletins

---

## 🔒 Sécurité

### Mesures Implémentées

- 🔐 **Authentification sécurisée** avec hachage de mots de passe
- 🛡️ **Protection contre injections SQL** (requêtes préparées)
- ✅ **Validation des entrées** côté serveur
- 🔑 **Gestion des sessions** sécurisée
- 👥 **Isolation des données** par rôle
- 📝 **Audit trail** des actions sensibles

---

## 🤝 Contribution

Les contributions sont les bienvenues une fois le code source publié !

### Comment Contribuer ?

1. Fork le projet
2. Créer une branche (`git checkout -b feature/NouvelleFonctionnalite`)
3. Commit les changements (`git commit -m 'Ajout NouvelleFonctionnalite'`)
4. Push vers la branche (`git push origin feature/NouvelleFonctionnalite`)
5. Ouvrir une Pull Request

---

## 👨‍💻 Auteur

<div align="center">

### **Mouhamadou Diouf**

🎓 Étudiant en **Master Data Science & Intelligence Artificielle**  
📍 Swiss UMEF University - Dakar, Sénégal

🎓 **Licence Statistique et Informatique Décisionnelle**  
📍 BEM Dakar | Diplômé le 31 août 2025

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mouhamadou_Diouf-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mouhamadou-diouf-364309276)
[![GitHub](https://img.shields.io/badge/GitHub-@LeM2003-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/LeM2003)
[![Email](https://img.shields.io/badge/Email-dioufmouha71@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:dioufmouha71@gmail.com)

**Compétences** : Python • R • SQL • PHP • MySQL • Power BI • Data Analysis • Backend Development

</div>

---

## 📂 Mes Autres Projets

### [💰 EcoTrack - Gestionnaire de Finances](https://github.com/LeM2003/ecotrack)
Application web complète de gestion financière personnelle (Projet de mémoire de licence)

### [🔍 Analyse COVID-19 Sénégal](https://github.com/LeM2003/covid19-senegal-analysis)
Analyse statistique des données épidémiologiques avec R

### [🛠️ Python SysAdmin Tools](https://github.com/LeM2003/Python-SysAdmin-Tools)
Outils d'automatisation réseau et sécurité

---

## 📄 Licence

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.

```
Copyright (c) 2024 Mouhamadou Diouf
```

---

## 📞 Contact

- 🐛 **Bugs** : [Ouvrir une issue](https://github.com/LeM2003/eduplan/issues)
- 💬 **Questions** : [Discussions GitHub](https://github.com/LeM2003/eduplan/discussions)
- 📧 **Email** : dioufmouha71@gmail.com

---

## 🙏 Remerciements

- 🏫 **BEM Dakar** pour la formation académique
- 👨‍🏫 Mes professeurs pour leurs enseignements
- 🌐 La communauté open source pour les ressources

---

<div align="center">

### ⭐ Si ce projet vous intéresse, n'hésitez pas à lui donner une étoile ! ⭐

**Made with ❤️ in Dakar, Senegal 🇸🇳**

---

[![Visitors](https://visitor-badge.laobi.icu/badge?page_id=LeM2003.eduplan)](https://github.com/LeM2003/eduplan)
[![GitHub stars](https://img.shields.io/github/stars/LeM2003/eduplan?style=social)](https://github.com/LeM2003/eduplan)

</div>
