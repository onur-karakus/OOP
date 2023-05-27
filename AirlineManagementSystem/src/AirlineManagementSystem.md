## Uçuş ve Pilot Yönetim Sistemi Sınıf Diyagramı

```mermaid
classDiagram
    class Airline {
        +id: String
        +aircrafts: List<Aircraft>
        +getFlights(): List<Flight>
    }

    class Aircraft {
        +type: String
        +status: String
    }

    class Flight {
        +id: String
        +departureAirport: Airport
        +arrivalAirport: Airport
        +departureTime: DateTime
        +arrivalTime: DateTime
        +pilot: Pilot
        +coPilot: Pilot
    }

    class Airport {
        +id: String
        +name: String
    }

    class Pilot {
        +name: String
        +experienceLevel: String
    }

    Airline "1" --> "*" Aircraft: owns
    Airline "1" --> "*" Flight: operates
    Flight "1" --> "1" Airport: departure from
    Flight "1" --> "1" Airport: arrival to
    Flight "1" --> "1" Pilot: pilot
    Flight "1" --> "1" Pilot: co-pilot


