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

Ajouter l’application Tâches à INSTALLED_APPS
Modifier le model