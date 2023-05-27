## Online Film Satış ve Kiralama Uygulaması Sınıf Diyagramı

```mermaid
classDiagram
    class Movie {
        +id: String
        +title: String
        +price: Double
    }

    class User {
        +id: String
        +name: String
        +subscribe(): void
        +buyMovie(movie: Movie): void
    }

    class Subscriber {
        +id: String
        +name: String
        +credits: Double
        +rentMovie(movie: Movie): void
    }

    class Application {
        +movies: List<Movie>
        +users: List<User>
    }

    User <|-- Subscriber
    Application "1" --> "*" Movie: has
    Application "1" --> "*" User: has
