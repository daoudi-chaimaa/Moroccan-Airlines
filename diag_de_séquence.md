sequenceDiagram
    participant Utilisateur
    participant Système
    participant Administrateur

    Utilisateur->>Système: Réserver un vol
    Système-->>Utilisateur: Confirmation de réservation

    Utilisateur->>Système: Consulter ses réservations
    Système-->>Utilisateur: Afficher les réservations

    Utilisateur->>Système: Effectuer un paiement
    Système-->>Utilisateur: Confirmation de paiement

    Administrateur->>Système: Gérer les vols
    Système-->>Administrateur: Confirmation de gestion

    Administrateur->>Système: S'authentifier
    Système-->>Administrateur: Accès autorisé
  
