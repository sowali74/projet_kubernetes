# Créer une application react
```

npx create-react-app my-app
```

# Tester l'application
```
cd my-app
npm run start
```

Tips : ctrl + C pour arrêter le serveur

# Créer un build de l'application
```
npm run build
```

# Lier le repository docker minikube à son terminal (si ce n'est pas déjà fait)
Sur Windows :
```
minikube -p minikube docker-env | Invoke-Expression
```
Sur Linux ou Mac :
```
eval $(minikube -p minikube docker-env)
```

# Construire l'image
```
cd ..
docker build . -t react-nginx
```

# Appliquer le déploiement et le service
```
kubectl apply -f react-deployment.yaml
kubectl apply -f react-service.yaml
```

# Vérifier que les pods sont démarrés
```
kubectl get pods
```

# Lancer le service dans mon navigateur
```
minikube service react-service
```