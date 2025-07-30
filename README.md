# Lab: Flask Pagination
In this lab an API endpoint, originally returning all books, is refactored with pagination to accept the query parameters of `?page` and `?per_page` and return only a subset of the books based on those parameters as well as including metadata such as total, page, and total_pages.

## Getting Started
* Set up your virtual enviroment <br> 

  ```bash
  virutalenv venv
  source venv/bin/activate
  ```
* Install necessary dependencies <br>
  ```bash
  pip install flask-sqlalchemy flask-migrate
  pip install flask-RESTful
  pip install marshmallow
  pip install faker
  ```
* Upgrade and seed the database if necessary <br>
  ```bash
  cd server
  flask db upgrade
  python seed.py
  ```

## Running the Application
Run the flask server: <br>
```bash
python app.py
```
### Example Endpoints
* `/books?page=1&per_page=5` <br>
Returns a list of five books from page 1 (books 1-5 in the database)
* `/books?page=4&per_page=3` <br>
Returns a list of 3 books from page 4 (books 10-12 in the database)
