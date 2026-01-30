# Dockerfile
# Utilise une image Python légère
FROM python:3.9-slim

# Définit le dossier de travail
WORKDIR /app

# Copie tes fichiers dans le conteneur
COPY . .

# Installe Flask (nécessaire pour ton app)
RUN pip install flask

# Expose le port 5000
EXPOSE 5000

# Commande pour lancer ton application
# Remplace 'teste.py' par ton fichier principal si besoin
CMD ["python", "teste.py"]
