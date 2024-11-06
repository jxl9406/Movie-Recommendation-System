### Project Description

The Movie Recommendation Backend is a RESTful API that manages movie information and user reviews. It stores movie details and user-generated reviews, allowing users to associate reviews with specific movies. The backend is built with Spring Boot and connects to a MongoDB database.

### Features

- **CRUD Operations** for movies and reviews.
- **MongoDB Integration** to store and manage data.
- **Review Linking**: Users can add reviews to specific movies.
- **RESTful API** endpoints for interaction with the data.

### Technologies Used

- **Java 17**
- **Spring Boot**
- **Spring Data MongoDB**
- **MongoDB**
- **Clone the Repository**:
    
    ```bash
    git clone htts://github.com/your-username/movie-recommendation-backend.git
    cd movie-recommendation-backend
    ```
    
- **Configure MongoDB**:
    - Ensure MongoDB is installed and running on your local machine or on a specified server.
    - The default configuration assumes MongoDB is running at `localhost:27017`. If you are using a different setup, update the MongoDB URI in `application.properties` under `src/main/resources`.
- **Install Dependencies**:
    - You can import this project into an IDE such as IntelliJ or Eclipse, which will automatically download dependencies.
    - Alternatively, run the following command to download dependencies:
        
        ```bash
        ./mvnw install
        ```
        
- **Run the Application**:
    
    ```bash
    ./mvnw spring-boot:run
    ```
    
    The server should now be running at `http://localhost:8080`
    

### API Endpoints

| HTTP Method | Endpoint | Description |
| --- | --- | --- |
| POST | `/movies` | Add a new movie |
| GET | `/movies` | Retrieve a list of all movies |
| GET | `/movies/{id}` | Get details of a specific movie |
| POST | `/reviews` | Add a new review |
| GET | `/movies/{id}/reviews` | Get all reviews for a specific movie |

### Usage Example

1. **Add a Movie**
    
    ```bash
    POST /movies
    {
      "title": "Inception",
      "imdbId": "tt1375666",
      "genres": ["Sci-Fi", "Thriller"]
    }
    ```
    
2. **Add a Review**
    
    ```bash
    POST /reviews
    {
      "body": "Amazing movie with a great plot twist!",
      "imdbId": "tt1375666"
    }
    ```
    
3. **Retrieve Reviews for a Movie**
    
    ```bash
    GET /movies/tt1375666/reviews
    ```
    

### Future Enhancements

- **Authentication and Authorization**: Secure the API for specific user actions.
- **Recommendation Logic**: Add recommendation algorithms to suggest similar movies.
- **Enhanced Search**: Allow more complex queries based on genre, release date, etc.
