# Description de la remise

### Nom complet: Théo Lenglart et Olivier Drapeau
### NIP: 537 406 306 et 
### Liste des codes et descriptions des fonctionnalités sélectionnées:
Exemple:
- (FA2) Intégration du Service Mesh Consul-Connect ==> 5%
- (FA21) Intégration de la fonctionnalité de Service Discovery de Consul-Connect ==> 5%
- (FA22) Observabilité des services et de leurs états (healthcheck) au travers du UI de Consul ==> 5%
- (FA23) Définition d'Intentions limitant la communication entre les services au strict nécessaire ==> 10%
- (FA24) Configuration de Canary Deployment et/ou Blue-green/A-B Deployment ==> 10%

### Directives nécessaires à la correction
Nous utilisons l'environnement Kind pour notre cluster et afin d'installer notre ingress controller, il faut exécuter la commande suivante :
```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
```

Pour lancer notre deployement, il faut exécuter la commande suivante à la racine du projet :
```bash
kubectl apply -f submission/deployment.yaml
```

### Commentaires généraux:
