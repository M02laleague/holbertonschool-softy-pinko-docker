# Étape 1 : Utiliser Ubuntu comme image de base
FROM ubuntu:latest

# Étape 2 : Mettre à jour les paquets APT
RUN apt-get update

# Étape 3 : Mettre à niveau les logiciels installés
RUN apt-get upgrade -y

# Étape 4 : Installer Python3 et pip3
RUN apt-get install -y python3 python3-pip

# Étape 5 : Résoudre les problèmes liés à l'environnement EXTERNALLY-MANAGED
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Étape 6 : Installer Flask via pip3
RUN pip3 install flask

# Étape 7 : Définir le répertoire de travail à /app
WORKDIR /app

# Étape 8 : Copier le fichier Python dans l'image Docker
COPY ./api.py /app/api.py

# Étape 9 : Définir la commande par défaut pour exécuter Flask
CMD ["python3", "api.py"]
