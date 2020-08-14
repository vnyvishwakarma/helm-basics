  projectCode: aazzxxyy
   infra:
     zone: a,b,c
     region: us-e
   
 ```sh  
 {{ if eq .Values.infra.region "us-e" }}ha: true{{ end }}
 ```
 
 
 helm install --dry-run --debug controlif ./mychart
 
 
 helm install controlif ./mychart 
 
 
 helm get manifest controlif
 
 helm uninstall controlif 
 
   
```sh
 //Error
   {{ if eq .Values.infra.region "us-e" }}
     ha: true
   {{ end }}
   
  
    {{ if eq .Values.infra.region "us-e" }}
    ha: true
    {{ end }}
    
    
   
    {{- if eq .Values.infra.region "us-e" }}
    ha: true
    {{- end }}
   
   //Should not be done. Error
   
   {{- if eq .Values.infra.region "us-e" -}}
   ha: true
  {{- end -}}

```