# spark-operator
spark on k8s

$ helm repo add spark-operator https://googlecloudplatform.github.io/spark-on-k8s-operator
$ kubectl create namesepace spark-operator
$ kubectl create clusterrolebinding <user>-cluster-admin-binding --clusterrole=cluster-admin --user=<user>@<domain>
$ helm install -n spark-operator my-release spark-operator/spark-operator
$kubectl get serviceAccount -n spark-operator
  
Edit service account in spark-pi.yaml that match with your service account above

$ kubectl apply -f examples/spark-pi.yaml
