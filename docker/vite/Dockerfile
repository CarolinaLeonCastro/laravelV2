# Image node.js 18 alpine (plus léger)
FROM node:18-alpine

# Répertoire de travail
WORKDIR /var/www/html

# Ajoute inotify-tools pour un meilleur support du watch
RUN apk add --no-cache inotify-tools

# Augmente les limites inotify
RUN echo "fs.inotify.max_user_watches=524288" >> /etc/sysctl.conf

# Expose explicitement le port
EXPOSE 5173

# Script de démarrage serveur de développement
CMD ["sh", "-c", "npm install && NODE_ENV=development npm run dev"] 