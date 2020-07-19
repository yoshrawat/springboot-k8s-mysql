# springboot-k8s-mysql

# docker image
```docker build -t yoshrawat/springboot-k8s-mysql```

# docker push
```docker push yoshrawat/springboot-k8s-mysql```

# secret deploy configMap
``` kubectl apply -f src/main/resources/mysql-configmap.yml```
``` kubetctl get configMap```

# secret deploy secret
``` kubectl apply -f src/main/resources/mysqldb-credentials.yml```
``` kubectl apply -f src/main/resources/mysqldb-root-credentials.yml```
``` kubetctl get secrets```

# deploy mysql service
``` kubetctl apply -f src/main/resources/mysql-deployment.yml```
``` kubectl get services```

# deploy spring service
``` kubetctl apply -f src/main/resources/deployment.yml```
``` kubectl get services```



