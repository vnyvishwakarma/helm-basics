# helm chart functions

Below are the URLs

  - https://masterminds.github.io/sprig/
  - https://godoc.org/text/template

 
 projectCode: aazzxxyy
 infra:
   zone: a,b,c
   region: us-e
 
 ```sh
 Zone: {{ quote .Values.infra.zone }}
 Region: {{ quote .Values.infra.region }}
 ProjectCode: {{ upper .Values.projectCode }}
```
 

 