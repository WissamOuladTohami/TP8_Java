# Exercice 1 – Système de paiement extensible
---

### Objectifs pédagogiques

- Comprendre le rôle des interfaces en Java pour définir des contrats indépendants des implémentations.  
- Découpler le code métier (`PaymentProcessor`) des détails de chaque moyen de paiement.  
- Manipuler un tableau dynamique pour stocker des objets hétérogènes.  
- Ajouter de nouvelles méthodes de paiement sans modifier le processeur.

---

### Description

- **Interface `PaymentMethod`** : définit le contrat pour tout moyen de paiement :  
  - `pay(amount)` : tente de payer un montant.  
  - `refund(amount)` : tente de rembourser un montant.  
  - `getName()` : retourne le nom de la méthode de paiement.  

- **Implémentations concrètes** :  
  - `CreditCard` : carte bancaire (numéro, titulaire, solde simulé).  
  - `PayPal` : paiement en ligne (email, solde simulé).  
  - `Bitcoin` : paiement en crypto (wallet, solde simulé).  

- **Classe `PaymentProcessor`** :  
  - Stocke dynamiquement un tableau de `PaymentMethod`.  
  - Pour chaque méthode, tente un paiement et un remboursement partiel.

---

### Résultat attendu

<img width="1115" height="455" alt="TP81" src="https://github.com/user-attachments/assets/812f32e2-87b3-414b-b285-f92300c36ce5" />

---

# Exercice 2 – Système de Notification Extensible
---

### Introduction

Les interfaces en Java permettent de définir des contrats sans imposer d’implémentation.  
Ce TP crée un système de notification où différents canaux (Email, SMS, Push) implémentent une même interface.  
Le gestionnaire `NotificationManager` diffuse des messages sans connaître les détails des canaux.

---

### Objectifs pédagogiques

- Définir et implémenter une interface Java (`Notification`).  
- Découpler la logique métier de l’envoi des notifications des canaux concrets.  
- Gérer un tableau dynamique d’objets hétérogènes.  
- Trier les notifications par priorité avant diffusion.

---

### Résultat attendu

<img width="1108" height="377" alt="TP82" src="https://github.com/user-attachments/assets/c86ac9da-616a-47a2-a3a4-af3e2390074f" />



