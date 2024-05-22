# Lier le repository docker minikube à son terminal
minikube -p minikube docker-env | Invoke-Expression

# Construire l'image
sudo docker build . -t app-stateless1-nginx

# Créer le déploiement
kubectl apply -f deployment.yaml

# Créer le service
kubectl apply -f service.yaml

# Lancer le service dans mon navigateur
minikube service app-stateless1-service