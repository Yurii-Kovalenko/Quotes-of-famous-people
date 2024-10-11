
# Web Service "Quotes of famous people"

## Introduction
**"Quotes of famous people"** is a web service for viewing quotes from famous people. Viewing is possible page by page, as well as by citation tags. It is also possible to view information about the authors of the quotations. It is also possible to add new quotes (authors, tags), but this option is available only after registration on the site.

## Technologies
Project is mainly based on:
- **Web framework:** Django  
- **Frontend:** HTML/CSS, JavaScript  
- **Backend:** Python 

## System Requirements
- Python 3.11
- Django


## Installation
1. **Clone the repository:**
   ```
   git clone https://github.com/Yurii-Kovalenko/Quotes-of-famous-people.git
   ```

2. **Go to the project directory:**
   ```
   cd Quotes-of-famous-people
   ```

3. **Set environment variables:**  
   Create an ```.env``` file(or rename example.env to .env) in the root of the project and add the necessary environment variables. For example:
```
SECRET_KEY=django-insecure ...

DATABASE_ENGINE=
DATABASE_NAME=
DATABASE_USER=
DATABASE_PASSWORD=
DATABASE_HOST=
DATABASE_PORT=


EMAIL_HOST=
EMAIL_PORT=
EMAIL_HOST_USER=
EMAIL_HOST_PASSWORD=
```

   The web service requires access to the Postgresql database, and also to the mail server. The Postgresql database can be made by registering on [https://www.koyeb.com/](https://www.koyeb.com/)(DATABASE_PORT is then unnecessary) or created in Docker(```docker-compose build```, ```docker-compose up```). The mail server can be made by registering on meta.ua or on another similar web service.

4. **Creating a virtual environment:**

   To isolate project dependencies, it is recommended to use a virtual environment.

   Create it:
   ```
   python -m venv venv
   ```
   And activate it:
   ```
   venv\Scripts\activate
   ```

5. **Installing dependencies**

   Install the required libraries from the requirements.txt file:
   ```
   pip install -r requirements.txt
   ```

6. **Go to the directory with manage.py:**
   ```
   cd quotes
   ```

7. **Database settings:**

   Apply migrations to the database:
   ```
   python manage.py migrate
   ```
   Create a superuser to access the Django admin panel:
   ```
   python manage.py createsuperuser
   ```

8. **Starting the server:**
   ```
   python manage.py runserver
   ```
   The web service will be available at: [http://127.0.0.1:8000](http://127.0.0.1:8000).