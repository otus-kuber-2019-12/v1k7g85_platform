# v1k7g85_platform
v1k7g85 Platform repository

Kubernetes mysql-operator


[minikube|vp.ilichev@note v1k7g85_platform]$ k get jobs
NAME                         COMPLETIONS   DURATION   AGE
backup-mysql-instance-job    1/1           2s         15h
restore-mysql-instance-job   1/1           47s        15h


[minikube|vp.ilichev@note kubernetes-operators]$ kubectl exec -it $MYSQLPOD -- mysql -potuspassword -e "select * from test;" otus-database
mysql: [Warning] Using a password on the command line interface can be insecure.
+----+-------------+
| id | name        |
+----+-------------+
|  1 | some data-2 |
|  2 | some data-2 |
+----+-------------+