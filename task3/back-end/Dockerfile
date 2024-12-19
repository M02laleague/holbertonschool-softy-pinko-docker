# Utiliser l'image de base Python
FROM ubuntu:latest

# Mettre à jour et installer les dépendances
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip python3-venv

# Créer un environnement virtuel Python
RUN python3 -m venv /env

# Activer l'environnement virtuel et installer Flask et flask-cors
RUN /env/bin/pip install --upgrade pip
RUN /env/bin/pip install flask flask-cors

# Copier le script Python de l'API
WORKDIR /app
COPY ./api.py /app/api.py

# Exposer le port pour Flask
EXPOSE 5252

# Utiliser l'environnement virtuel pour exécuter Flask
CMD ["/env/bin/python", "api.py"]
