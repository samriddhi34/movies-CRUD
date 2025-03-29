# Movie CRUD API

This is a simple REST API built using Golang and Gorilla Mux that allows users to perform CRUD (Create, Read, Update, Delete) operations on movies.

## Features
- Get all movies
- Get a single movie by ID
- Add a new movie
- Update an existing movie
- Delete a movie

## Technologies Used
- **Golang**
- **Gorilla Mux** (for routing)
- **Postman** (for API testing)

## Installation & Setup

1. **Clone the repository**
   ```sh
   git clone https://github.com/samriddhi34/go-movies-CRUD.git
   cd go-movies-CRUD
   ```

2. **Install dependencies**
   ```sh
   go mod init go-movies-CRUD
   go mod tidy
   ```

3. **Run the application**
   ```sh
   go run main.go
   ```

4. **Server will start on:**
   ```
   http://localhost:8000
   ```

## API Endpoints

| Method | Endpoint          | Description          |
|--------|------------------|----------------------|
| GET    | `/movies`         | Get all movies       |
| GET    | `/movies/{id}`    | Get a movie by ID    |
| POST   | `/movies`         | Add a new movie      |
| PUT    | `/movies/{id}`    | Update a movie       |
| DELETE | `/movies/{id}`    | Delete a movie       |

## Example Requests

### Get all movies
```sh
GET http://localhost:8000/movies
```

### Get a movie by ID
```sh
GET http://localhost:8000/movies/1
```

### Add a new movie
```sh
POST http://localhost:8000/movies
Content-Type: application/json

{
    "isbn": "12345",
    "title": "New Movie",
    "director": {
        "firstName": "John",
        "lastName": "Doe"
    }
}
```

### Update a movie
```sh
PUT http://localhost:8000/movies/1
Content-Type: application/json

{
    "isbn": "67890",
    "title": "Updated Movie",
    "director": {
        "firstName": "Jane",
        "lastName": "Doe"
    }
}
```

### Delete a movie
```sh
DELETE http://localhost:8000/movies/1
```

