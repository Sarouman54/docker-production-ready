#1. Image de base légère
FROM node:18-alpine

#2. Définir le dossier de travail
WORKDIR /app

#3. Optimisation du cache : on copie d'abord les dépendances
COPY package*.json ./
RUN npm install --production

#4. Copie du code source
COPY . .

#5. Sécurité : on crée un utilisateur non-root
USER node

#6. Documentation du port
EXPOSE 3000

#7. Commande de démarrage
CMD ["npm", "start"]