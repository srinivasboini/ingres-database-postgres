# ingres-database-postgres


## Add bitnami repo

```
helm repo add bitnami https://charts.bitnami.com/bitnami  

```


## postgres template using helm

```
helm search repo bitnami/postgresql --versions


 helm template bitnami/postgresql  \
 --set fullnameOverride=postgres \
 --set namespaceOverride=database-ns \
 --set auth.postgresPassword=password \
 --set auth.username=srinivas \
 --set auth.password=password \
 --set auth.database=my_database > postgres.yaml
```