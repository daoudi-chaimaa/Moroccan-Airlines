# Diagramme de Classe

```mermaid
classDiagram
    class Vol {
        +String numeroVol
        +Date dateVol
        +Aéroport aeroportDepart
        +Aéroport aeroportArrivee
        +Avion avion
        +EquiPage equipage
        +addReservation()
        +getDetails()
    }
    
    class Avion {
        +String type
        +int capacite
        +int anneeFabrication
        +String modele
        +verifierDisponibilite()
    }

    class Aéroport {
        +String codeIATA
        +String nom
        +String ville
        +String pays
    }

    class Passager {
        +String nomComplet
        +String numeroPasseport
        +Date dateNaissance
        +String nationalite
        +String contact
        +faireReservation()
    }

    class Reservation {
        +int idReservation
        +Date dateReservation
        +String statut
        +float prixTotal
        +payerReservation()
    }

    class EquiPage {
        +String nomComplet
        +String fonction
        +String numeroLicence
        +String nationalite
    }

    Vol "1" --> "0..*" Avion : Utilise
    Vol "1" --> "1" Aéroport : AéroportDépart
    Vol "1" --> "1" Aéroport : AéroportArrivee
    Vol "1" --> "1..*" EquiPage : A un équipage
    Vol "1" --> "0..*" Reservation : Associe
    Reservation "0..*" --> "1" Passager : Contient
