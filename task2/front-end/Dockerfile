FROM nginx:latest

# Copier les fichiers du front-end dans le répertoire approprié
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copier la configuration Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exposer le port 9000
EXPOSE 9000
