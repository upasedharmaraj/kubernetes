
# Sample NGNIX Helm

## Install Dependencies

```
yum install -y socat

```
## Install Chart

```
helm install testchart

export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=testchart,app.kubernetes.io/instance=eponymous-fly" -o jsonpath="{.items[0].metadata.name}")

echo $POD_NAME 

```

## Forward Port

```
kubectl port-forward $POD_NAME 8080:80
  
```

## Check Ngnix running

```
curl http://127.0.0.1:8080

```

