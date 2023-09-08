## Crear una Conexión entre Django y SQL Server usando el driver mssql-django

### OPCIÓN 1

    Atraves de `mssql-django` el cual es una bifurcación de `django-mssql-backend`
    primero instalar pyodbc aqui el enlace
    https://pypi.org/project/pyodbc/
    `pip install pyodbc`

    Luego ir al https://pypi.org/project/mssql-django/
    he instalar `pip install mssql-django`

    `python manage.py makemigrations`
    `python manage.py migrate`

    - Correr el proyecto
      `python manager.py runserver`

Configuración para la conexión a SQL Server
`

    DATABASES = {
        'default': {
            'ENGINE': 'mssql',
            'NAME': 'demo_crud',
            'USER': 'root_python',
            'PASSWORD': '4825',
            'HOST': 'DESKTOP-5NRC837\SQLEXPRESS',
            # 'HOST': '127.0.0.1',
            'PORT': '',
            'OPTIONS': {
                'driver': 'ODBC Driver 17 for SQL Server',
            }
        }
    }

`

#### OPCIÓN 2

    ATRAVES DE `django-mssql-backend`
    https://pypi.org/project/django-pyodbc-azure/
    pip install django-pyodbc-azure

    https://pypi.org/project/pyodbc/

    - pip install pyodbc

    https://stackoverflow.com/questions/54824864/django-python-sql-server-pyodbc-isnt-an-available-database-backend
    https://pypi.org/project/django-mssql-backend/
    pip install django-mssql-backend

`

    DATABASES = {
        'default': {
            'ENGINE': 'sql_server.pyodbc',
            'NAME': 'demo_crud',
            'USER': 'root_python',
            'PASSWORD': '4825',
            'HOST': 'DESKTOP-5NRC837\SQLEXPRESS',
            'PORT': '',
            'OPTIONS': {
                'driver': 'ODBC Driver 17 for SQL Server',
            }
        }
    }

`
