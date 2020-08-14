# built-in objects

Below are the URLs

  - https://helm.sh/docs/chart_template_guide/builtin_objects/

 ```sh
 projectCode: aazzxxyy
 infra:
   zone: a,b,c
   region: us-e
 

apiVersion: v1
kind: ConfigMap
metadata:
  name: {{ .Release.Name }}-configmap
data:
  myvalue: "Sample Config Map"
```

helm install releasename-test ./mychart

helm get manifest releasename-test

helm install --debug --dry-run dryrun-test ./mychart

kubectl describe configmaps releasename-test-configmap

helm uninstall releasename-test

################################################################

 mychart/values.yaml
 
```sh
costCode: CC98112
costCode: {{ .Values.costCode }}
```
 
helm install --debug --dry-run firstdryrun ./mychart

helm install firstvalue ./mychart

helm get manifest firstvalue

kubectl describe configmaps firstvalue-configmap


################################################################


 helm install --dry-run --debug --set costCode=CC00000 valueseteg ./mychart
 
 helm install valueseteg ./mychart --set costCode=CC00000 

 helm get manifest valueseteg

 kubectl describe configmaps valueseteg-configmap

 helm ls

helm uninstall valueseteg
