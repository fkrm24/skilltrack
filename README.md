# Projet SkillTracker

## Objectif
Créer des comptes utilisateurs avec la possibilité de suivre les compétences et d’organiser des tâches et objectifs. L'interface sera intuitive avec une sidebar, permettant de naviguer entre les compétences, objectifs, bibliothèque et agenda.

### Fonctionnalités
- **Suivi des compétences** avec objectifs et tâches associées. Une compétence atteindra son niveau maximum lorsque tous les objectifs seront remplis.
- **Calendrier interactif** où les tâches seront affichées aux dates définies par l'utilisateur.
- **Bibliothèque de ressources** permettant aux utilisateurs de stocker des pages web utiles pour atteindre leurs objectifs.

## API REST

### Utilisateurs
- **POST /users**  
  Inscription d'un nouvel utilisateur  
  **Paramètres :**  
  - `id`  
  - `username`  
  - `password`  
  - `email`  

### Compétences
- **POST /skills**  
  Ajouter une compétence  
  **Paramètres :**  
  - `id`  
  - `user_id`  
  - `skill_name`  
  - `level`  

- **GET /skills**  
  Récupérer la liste des compétences de l’utilisateur  

### Objectifs
- **POST /skills/{skills_id}/goals**  
  Ajouter un objectif pour une compétence  
  **Paramètres :**  
  - `id`  
  - `skills_id`  
  - `description`  

- **GET /skills/{skills_id}/goals**  
  Récupérer les objectifs pour une compétence  

### Tâches
- **POST /skills/{skills_id}/goals/{goals_id}/tasks**  
  Ajouter une tâche pour un objectif  
  **Paramètres :**  
  - `id`  
  - `goals_id`  
  - `description`  
  - `completed`  
  - `due_date`  

- **PUT /tasks/{task_id}/validate**  
  Marquer une tâche comme terminée  

### Calendrier
- **GET /calendar**  
  Récupérer les tâches dans le calendrier  

### Bibliothèque
- **POST /library**  
  Ajouter une page web à la bibliothèque  
  **Paramètres :**  
  - `id`  
  - `resource_title`  
  - `resource_url`
  - 






![WhatsApp Image 2024-10-09 at 12 35 50](https://github.com/user-attachments/assets/6ee3b398-a891-4ca7-aaeb-9e1c3b27e5d0)
