
helm create mychart


rm -rf mychart/templates/*



configmap.yaml
~~~~~~~~~~~~~

apiVersion: v1
kind: ConfigMap
metadata:
  name: mychart-configmap
data:
  myvalue: "Sample Config Map"





helm install helm-demo-configmap ./mychart

helm ls

kubectl get all

helm get manifest helm-demo-configmap

kubectl describe configmaps mychart-configmap
