# DjangoWebApp
A Django-based web app.

## How to host

1. Install the virtual environment provided in Pipfile:
```mysql
pipenv shell
```

2. Activate the virtual environment (in Windows):
```mysql
source $(pipenv --venv)/Scripts/activate
```

3. Open the MySQL terminal, and create a user `admindjango` with password `employee@123!` (this is used in the `settings.py` file)

Activate MySQL terminal
```shell
mysql -u root -p
```

```mysql
CREATE USER 'admindjango'@'localhost' IDENTIFIED BY 'employee@123!'; 
```

Assign privileges:
```mysql
GRANT ALL ON *.* TO 'admindjango'@'localhost'
```

Flush the privileges:
```mysql
FLUSH PRIVILEGES;
```

4. Make migrations

```shell
python3 manage.py makemigrations

python3 manage.py migrate
```

5. Host the service

```shell
python3 manage.py runserver
```

6. Open a browser and go to https://127.0.0.1:3000/ to see the hosted app.