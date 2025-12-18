# Description de la remise

### Nom complet: Théo Lenglart et Olivier Drapeau
### NIP: 537 406 306 et 537159040
### Liste des codes et descriptions des fonctionnalités sélectionnées:
- (FA1) Sécuriser et encrypter les communications au travers de certificats SSL ==> 10%
- (FA21) Intégration du Service Mesh Consul-Connect ==> 5%
- (FA23) Observabilité des services et de leurs états (healthcheck) au travers du UI de Consul ==> 5%
- (FA31) Intégration d’un outil de gestion de journaux (loki) ==> 5%
- (FA32) Intégration de monitoring des ressources physiques (prometheus) ==> 5%

### Directives nécessaires à la correction
Nous utilisons l'environnement Kind pour notre cluster et afin d'installer notre ingress controller, il faut exécuter la commande suivante :
```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
```

Pour lancer notre deployement, il faut exécuter la commande suivante à la racine du projet :
```bash
kubectl apply -f submission
```

### Commentaires généraux:

Nous avons remarqué qu'il y a un problème de cache lorsque nous accédons à l'application sur un navigateur internet. Pour palier à ce problème, nous trouvons qu'il est préférable de tester notre application avec la commande `curl`.  
En effet, après avoir appeler l'url `http://localhost/`, lorsque nous appelons `http://localhost/admin/feedback` le navigateur affiche la page d'accueil. Ce problème ne se produit pas avec des requêtes effectuées en ligne de commande.
