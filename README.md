# 202401-postgresdocker
Tuto pour dockeriser un projet avec postgres

1. Dans votre répertoire de travail, créez un environnement virtuel et activez-le.

```
git clone https://github.com/Slb59/202401-postgresdocker.git
mkdir .venv
pipenv install
pipenv shell
```

2. Installer Django et démarrer un nouveau projet

```
pipenv install django
django-admin startproject config .
```

3.  Créons une application de tâches et installons Django Rest Framework

```
python manage.py startapp tasks
pipenv install djangorestframework
```

Ajouter l’application tasks et rest_framework à INSTALLED_APPS
Modifier le model et le serializer
Modifier la vue et l'url de l'application tasks
Modifier l'url principale dans config

4. Lancer les migrations et le serveur

```
python manage.py migrate
python manage.py makemigrations
python manage.py runserver
```

5. Configurer postgres

Modifier les settings et .env

```
pipenv install psycopg2
pipenv requirements > requirements.txt
python manage.py makemigrations
python manage.py migrate
```

6. Configurer docker et docker-compose

```
docker compose up --build
```