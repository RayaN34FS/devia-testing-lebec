# User Stories

## 1. Récupération de tous les utilisateurs (GET /users)
**En tant qu'utilisateur,**  
Je veux voir une liste de tous les utilisateurs,  
Afin de pouvoir accéder aux informations sur tout le monde dans le système.  

### Critères d'acceptation :
- Le système récupère une liste de tous les utilisateurs depuis la base de données.
- La réponse inclut les détails essentiels des utilisateurs (par exemple, ID, nom, email).
- S'il n'y a pas d'utilisateurs, le système renvoie une liste vide.

---

## 2. Création d'un utilisateur (POST /users)
**En tant qu'administrateur,**  
Je veux créer un nouvel utilisateur,  
Afin de l'ajouter au système avec les informations nécessaires.  

### Critères d'acceptation :
- Une requête valide contient les informations de l'utilisateur (par exemple, nom, email, mot de passe).
- Le système crée un nouvel utilisateur et le stocke dans la base de données.
- Si les données saisies sont invalides, le système renvoie une erreur 400 avec un retour sur la validation.
- Après la création, le système répond avec les détails du nouvel utilisateur créé.

---

## 3. Mise à jour d'un utilisateur (PUT /users/:id)
**En tant qu'administrateur,**  
Je veux mettre à jour les informations d'un utilisateur,  
Afin de modifier ses données si nécessaire.  

### Critères d'acceptation :
- Le système met à jour l'utilisateur sur la base de l'ID fourni et du corps de la requête.
- Une requête valide contient uniquement les champs à mettre à jour (par exemple, email, rôle).
- Si l'ID de l'utilisateur n'existe pas, le système renvoie une erreur 404.
- Si les données saisies sont invalides, le système renvoie une erreur 400 avec un retour sur la validation.
- Les détails mis à jour de l'utilisateur sont reflétés dans la base de données.
