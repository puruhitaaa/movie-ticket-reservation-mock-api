# Public URL
https://odd-cyan-crow-shoe.cyclic.app

# Movie Ticketing System API

This API provides movie, theater, showtime, and reservation data for building a movie ticketing application. It is powered by json-server for rapid prototyping and testing.

## Data Structure

The JSON database used (`db.json`) contains the following resources:

* **movies:** Movie catalog with details.
* **theatres:** Theaters with location information.
* **auditoriums:** Individual auditoriums within theaters.
* **showtimes:** Movie screenings with associated dates and times.
* **seats:** Individual seats within each auditorium. 
* **users:** User profiles (for demonstration)
* **reservations:** Reservations for specific seats at showtimes.

##  Endpoints

**Base URL:**  
Assuming you're running json-server locally on port 3200, the base URL would be: `http://localhost:3200`

###  Resources

- **GET /movies**   
 Retrieves a list of all movies.

- **GET /movies/:id**  
 Retrieves a single movie by its ID.

- **GET /theatres**  
 Retrieves a list of all theaters.

- **GET /theatres/:id**  
 Retrieves a single theater by its ID.

- **GET /auditoriums**  
 Retrieves a list of all auditoriums.

- **GET /auditoriums/:id**  
 Retrieves a specific auditorium by its ID.

- **GET /showtimes**  
 Retrieves a list of all showtimes.

- **GET /showtimes/:id**  
 Retrieves a specific showtime by its ID.

- **GET /seats**  
 Retrieves a list of all seats.

- **GET /seats/:id**  
 Retrieves a specific seat by its ID.

- **GET /users**  
 Retrieves a list of all users.

- **GET /users/:id**  
 Retrieves a single user by its ID.

- **GET /reservations**  
 Retrieves a list of all reservations.

- **GET /reservations/:id**  
 Retrieves a single reservation by its ID.

## Filtering and Relationships

You can filter and explore relationships between resources:

* **Get showtimes for a movie:**
   `GET /showtimes?movie_id=<movie_id>`

* **Get seats for a specific auditorium:**
   `GET /seats?auditorium_id=<auditorium_id>`

* **Get a user's reservations:**
   `GET /reservations?user_id=<user_id>`

## Example Usage (cURL) 

```bash
# Get all movies
curl http://localhost:3200/movies

# Get details of movie with ID 2
curl http://localhost:3200/movies/2

# Get the showtimes for movie with ID 1
curl http://localhost:3200/showtimes?movie_id=1

# Get all seats in auditorium with ID 1
curl http://localhost:3200/seats?auditorium_id=1
```

## Making Changes (CRUD)

json-server supports RESTful interactions for modifying data:

* **POST /movies**  Creates a new movie.
* **PUT /movies/:id**  Updates an existing movie.
* **DELETE /movies/:id**  Deletes a movie.

Similar methods exist for other resources (`/theatres`, `/showtimes`, etc.)

## Important Notes

* This API is intended for development and demonstration purposes. Consider a more robust database solution for production environments.
* Authentication and authorization features are not included in this basic setup. Implement those as needed for a real-world application.

Let me know if you have any other questions.
