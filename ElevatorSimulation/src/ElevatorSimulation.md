## Kodluyoruz Sigorta Şirketi Asansör Simülasyonu

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
        +floor:
