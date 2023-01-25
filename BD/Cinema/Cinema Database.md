````sql
DECLARE var_height, var_age INT;

SELECT * FROM actors
WHERE actor_id IN (  ...  );

-- obtain list of actor id's.

height BETWEEN var_height * 0.9 AND var_height * 1.1 -- tolerance

age(birthdate) BETWEEN var_age - 5 AND var-age + 5; -- age()

-- obtain a list of actor id's

WHERE actor_id IN (--,--,--,--)
SELECT actor_id FROM actors
INNER JOIN ...

````


# Database structure.

Main point: Develop a SN to do an automatic casting process.

### Starting point.

A collection of movies.
A list of actors.

--> a new movie
--> Im looking for actors that fit the role of the character.

actor <--> character

***At least***:
- 20 movies
- 20 actors
- 20 character
- 5 genres

## Database tables.

### movies

| table_name          | description               | datatype          |
| ------------------- | ------------------------- | ----------------- |
| movie_id            | To link with othe tables. | INT AUTOINCREMENT |
| movie_name          | Name of the movie.        | VARCHAR(255)      |
| movie_genre         | Genres of the movie.      | VARCHAR(500)      |
| movie_director      | Who directed the movie.   | VARCHAR(255)      |
| movie_income        | How much money.           | INT()             |
| movie_score         | Great or not?             | DECIMAL(3,2)      |
| movie_duration      | Duration of the movie.    | TIME()            |
| movie_certification | 18+?                      | VARCHAR(50)       |

### genres

| table_name | datatype          |
| ---------- | ----------------- |
| genre_id   | INT AUTOINCREMENT |
| genre_name | VARCHAR(255)      |

### actors

| table_name        | datatype          |
| ----------------- | ----------------- |
| actor_id          | INT AUTOINCREMENT |
| actor_forename    | VARCHAR(255)      |
| actor_surname     | VARCHAR(255)      |
| actor_birthday    | DATE              |
| actor_email       | VARCHAR(255)      |
| actor_height      | DECIMAL(2,1)      |
| actor_skin        | VARCHAR(100)      |
| actor_race        | VARCHAR(100)      |
| actor_languages   | VARCHAR(500)      |
| actor_skills      | VARCHAR(500)      |
| actor_salary      | DECIMAL(12,2)     |
| actor_personality | VARCHAR(255)      |
| actor_weight      | DECIMAL(6,2)      |

### characters

| table_name            | datatype            |
| --------------------- | ------------------- |
| character_id          | INT AUTOINCREMENT   |
| character_forename    | VARCHAR(255)        |
| character_surname     | VARCHAR(255)        |
| character_age         | INT(100)            |
| character_personality | VARCHAR(255)        |
| character_height      | DECIMAL(2,1)        |
| character_weight      | DECIMAL(6,2)        |
| character_skin        | VARCHAR(100)        |
| character_race        | VARCHAR(100)        |
| character_movie       | INT / Foreign key / |

## ℹ Completar las siguientes bases de datos:

- [ ] Actores
- [ ] Characters
- [x] Movies



## ✏ Cosas que hacer:

- [ ] Insertar imagenes en el Canvas.

