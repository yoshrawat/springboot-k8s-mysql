# springboot-k8s-mysql

# docker image
```docker build -t yoshrawat/springboot-k8s-mysql```

# docker push
```docker push yoshrawat/springboot-k8s-mysql```

# secret deploy configMap
``` kubectl apply -f src/main/resources/mysql-configmap.yml```
``` kubectl get configMap```

# secret deploy secret
``` kubectl apply -f src/main/resources/mysqldb-credentials.yml```
``` kubectl apply -f src/main/resources/mysqldb-root-credentials.yml```
``` kubectl get secrets```

# deploy mysql service
``` kubectl apply -f src/main/resources/mysql-deployment.yml```
``` kubectl get services```

# deploy spring service
``` kubectl apply -f src/main/resources/deployment.yml```
``` kubectl get services```

# connect to mysql running  on kubernetes cluster from local machine
```kubectl port-forward app-mysql-3323704556-nce3w 3306:3306```

