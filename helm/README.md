# Helm

## Install Helm


```
wget https://storage.googleapis.com/kubernetes-helm/helm-v2.11.0-linux-amd64.tar.gz
tar -xzvf helm-v2.11.0-linux-amd64.tar.gz
sudo mv linux-amd64/helm /usr/local/bin/helm

```

## Initialize helm

```
kubectl create -f helm-rbac.yaml
helm init --service-account tiller

```

