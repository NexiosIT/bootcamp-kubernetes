# Bootcamp-kubernetes

## Requirements

1. Install kubectl
   - https://kubernetes.io/docs/tasks/tools/
2. Past recived configfile into [sendend to Nexios email]:
   - Windows: %USERPROFILE%\.kube\config
   - Mac: ~/.kube/config
   - Linux: ~/.kube/config
3. Test connection with the cluster (default no pods installed)
   - kubectl get pods

### Optional

For the UI-lovers:
=> https://k8slens.dev

## Exercise

1. Create a deployment for your own frontend-chat-app dockerfile
   - Demo repository: 04091998/bootcamp-frontend:v0.0.2
2. Create a service that can access the deployment on port 80
3. Make the service public with ingress
   - The availabel url's are: [NAME].chat.bootcamp.nexiosdevops.be
4. Add let's encrypt to created ingress object
   - staging: letsencrypt-staging
   - production: not available

---

5. Create a secret with an username and password (will be used for MonogDB deployment)
6. Install MonogDB on your namespace
7. Persist the data volume
   - Available storage-class: do-block-storage

---

8. Add a configmap with a connectionstring to the internal database
   - key: you can choose
   - value MONGODB_URI=[mongo-db-connection-string]
9. Install bootcamp-chat-api on your namespace and set the ENV value with the key from the configmap
   - docker-image: 04091998/bootcamp-api:v0.0.1
10. Create a service that can access the deployment on port 3001
11. Make the service public with ingress

- The availabel url's are: api.[NAME].chat.bootcamp.nexiosdevops.be

12. Add let's encrypt to created ingress object
