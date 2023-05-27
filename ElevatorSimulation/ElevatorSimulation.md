## Asansör Simülasyonu

```mermaid
classDiagram
    class Building {
        +floors: Integer
        +elevators: List<Elevator>
    }

    class Elevator {
        +capacity: Integer
        +currentFloor: Integer
        +targetFloors: List<Integer>
        +isMoving: Boolean
        +doorOpen: Boolean
        +callButtonPressed(direction: String, floor: Integer): void
        +selectFloor(floor: Integer): void
        +openDoor(): void
        +closeDoor(): void
    }

    class Floor {
        +floorNumber: Integer
        +elevatorShafts: List<ElevatorShaft>
        +arrivalLights: List<Light>
        +callButtons: List<CallButton>
    }

    class ElevatorShaft {
        +elevator: Elevator
        +arrivalLight: Light
        +floor: Integer
    }

    class Light {
        +status: Boolean
    }

    class CallButton {
        +direction: String
        +floor: Integer
        +pressed: Boolean
    }

    class Person {
        +currentFloor: Integer
        +destinationFloor: Integer
    }

    class Simulator {
        +building: Building
        +currentTime: DateTime
        +generateRandomNumber(min: Integer, max: Integer): Integer
        +generatePerson(): Person
        +simulate(): void
        +logEvent(event: String): void
    }

    Building "1" --> "*" Elevator: has
    Building "1" --> "*" Floor: has
    ElevatorShaft --> Elevator
    Floor "1" --> "*" ElevatorShaft: has
    Floor "1" --> "*" Light: has
    Floor "1" --> "*" CallButton: has
