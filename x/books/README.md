# CS50's Web Programming with Python and JavaScript

## Project 1: Books<br><br>

This is a project for a ***Book Review*** website. 

Users are able to register for this website and then log in using their username and password. Once they log in, they are able to search for books, leave reviews for individual books, and see the reviews made by other people. It also uses the a third-party API by Goodreads, another book review website, to pull in ratings from a broader audience. Finally, users are able to query for book details and book reviews programmatically via this website’s API.

This project has the following main features:

- **Registration:** Users are able to register for this website, providing a username and password.

- **Login:** Users, once registered, are able to log in the website with their username and password.

- **Logout**: Logged in users are able to log out of the site.

- **Import:** Provided for this project is a file called *books.csv*, which is a spreadsheet in *CSV format* of 5000 different books. Each one has an ISBN number, a title, an author, and a publication year. In a *Python* file called *import.py* separate from the web application, there is a program that take the books and import them into a *PostgreSQL database*. Run this program to import the books into the database.

- **Search:** Once a user has logged in, they are taken to a page where they can search for a book. Users are able to type in the ISBN number of a book, the title of a book, or the author of a book. After performing the search, the website displays a list of possible matching results, or a warning message if there are no matches. If the user types in only part of a title, ISBN, or author name, the search page will find matches for those as well.

- **Book Page:** When users click on a book from the results of the search page, they are taken to a book page, with details about the book: its title, author, publication year, ISBN number, and any reviews that users have left for the book on the website.

- **Review Submission:** Users are able to submit a review for a book, consisting of a rating on a scale of 1 to 5, as well as a text component to the review where the user can write their opinion about a book. Users are not able to submit multiple reviews for the same book.

- **Goodreads Review Data:** On the book page, is also displayed (if available) the average rating and number of ratings the work has received from *Goodreads*.

- **API Access:** If users make a *GET request* to the website’s */api/`<isbn>`* route, where `<isbn>` is an ISBN number, the website returns a *JSON response* containing the book’s title, author, publication date, ISBN number, review count, and average score. The resulting *JSON* follows the format:

        {
            "title": "Memory",
            "author": "Doug Lloyd",
            "year": 2015,
            "isbn": "1632168146",
            "review_count": 28,
            "average_score": 5.0
        }

If the requested ISBN number isn’t in the database, the website returns a 404 error.

- **SQL:** The project uses *raw SQL commands* (as via *SQLAlchemy’s execute method*) in order to make database queries.

- **Python:** The list of the *Python packages* that need to be installed in order to run the web application, is added to the *requirements.txt* file.
