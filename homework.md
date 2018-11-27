# SQL Homework

Great news G10! The local cinema are having a Marvel Movie Marathon! They have asked you to help maintain their database of movies with times and attendees.

## To access the database:

First, create a database called 'marvel'

```
# terminal
createdb marvel
```

Next, run the provided SQL script to populate your database:

# terminal

Use the supplied data as the source of data to answer the questions. Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.

## Questions

1.  Return ALL the data in the 'movies' table.

SELECT * FROM movies;

2.  Return ONLY the name column from the 'people' table

SELECT name FROM people;

3.  Oops! Someone at CodeClan spelled Declan's name wrong! Change it to reflect the proper spelling ('CoDeclan Malon' should be 'Declan Malone').

UPDATE people SET name = 'Declan Malone' WHERE name = 'CoDeclan Malon';

SELECT * FROM people;

4.  Return ONLY your name from the 'people' table.

SELECT name FROM people WHERE  name = 'Kevin Frew';


5.  The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.

DELETE FROM movies WHERE title = 'Batman Begins';

SELECT * FROM movies;

6.  Create a new entry in the 'people' table with the name of one of the instructors.

INSERT INTO people (name) VALUES ('Ally');

SELECT * FROM people;

7.  Melinda Matthews has decided to hijack our movie evening, Remove her from the table of people.

DELETE FROM people WHERE name = 'Melinda Matthews';

SELECT * FROM people;

8.  The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.

INSERT INTO movies (title, year, show_time) VALUES ('Avengers: Infinity War', 2018, '00:00');

SELECT * FROM movies;


9.  The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.

UPDATE movies SET show_time = '20:55' WHERE	 title = 'Guardians of the Galaxy 2';

SELECT * FROM movies;


## Extension

1.  Research how to delete multiple entries from your table in a single command.
