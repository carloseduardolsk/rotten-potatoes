# Deployment projeto Rotten Potatoes em kubernetes

## Ambiente Rodando 

NAME                          READY   STATUS    RESTARTS   AGE
pod/mongodb-9f45bf784-xm7qt   1/1     Running   0          55s
pod/web-7b95cb9599-wgcfb      1/1     Running   0          55s

NAME                 TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)        AGE
service/kubernetes   ClusterIP   10.43.0.1       <none>        443/TCP        6m18s
service/mongodb      ClusterIP   10.43.114.176   <none>        27017/TCP      55s
service/web          NodePort    10.43.232.65    <none>        80:30000/TCP   55s

NAME                      READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mongodb   1/1     1            1           55s
deployment.apps/web       1/1     1            1           55s

NAME                                DESIRED   CURRENT   READY   AGE
replicaset.apps/mongodb-9f45bf784   1         1         1       55s
replicaset.apps/web-7b95cb9599      1         1         1       55s

