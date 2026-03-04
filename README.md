# 🧮 Programmation_Orientee_Objet_PHP
## Description
Ce projet PHP met en place un mini-système de gestion d’étudiants et de filières en utilisant une architecture orientée objet :

- Entités métier (Etudiant, Filiere) avec validation stricte des données.

- Repository simulé en mémoire (FakeEtudiantRepository) implémentant une interface générique (RepositoryInterface).

- Autoloading des classes via spl_autoload_register.

- Scénario CRUD complet : insertion, modification, suppression et affichage des étudiants.
## Project Structure
```
project/
├── public/
│   └── index.php
├── src/
│   ├── Entity/
│   │   ├── Etudiant.php
│   │   └── Filiere.php
│   └── Repository/
│       ├── FakeEtudiantRepository.php
│       └── RepositoryInterface.php
└── README.md
```
# ⚙️ Features
## 1. Fichier index.php
Configure l’autoload des classes sous le namespace App\.

Crée des instances de Filiere et Etudiant.

Gère les erreurs de validation avec InvalidArgumentException.

- Utilise FakeEtudiantRepository pour :

- Insertion d’étudiants.

- Modification d’un étudiant existant.

- Suppression d’un étudiant.

- Affichage des résultats après chaque opération.

## 2. Classe Etudiant
- Attributs : id, nom, email, filiere.

Validation stricte :

- id doit être positif ou null.

- nom obligatoire et non vide.

- email valide selon FILTER_VALIDATE_EMAIL.

Méthodes : getters et setters.

## 3. Classe Filiere
Attributs : id, libelle.

Validation stricte :

- id positif ou null.

- libelle obligatoire et non vide.

Méthodes : getters et setters.

## 4. Interface RepositoryInterface
Définit les méthodes génériques :

- findAll()

- findById(int $id)

- save($entity)

- delete(int $id)

## 5. lasse FakeEtudiantRepository
Implémente RepositoryInterface.

Stocke les étudiants en mémoire avec auto-incrément.

Méthodes :

- save() → insertion ou mise à jour.

- findAll() → retourne tous les étudiants.

- findById() → recherche par identifiant.

- delete() → suppression.


## 💡 Concepts Practiced

- Autoloading avec spl_autoload_register.

- Organisation en entités et repositories.

- Validation stricte des données avec exceptions.

- Implémentation d’un dépôt mémoire pour simuler une base de données.

- Gestion des opérations CRUD.
