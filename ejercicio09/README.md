1) traigo el descriptor en el que me voy a basar https://gitlab.com/-/snippets/2088421/raw/master/deployment.yaml

2) Lo corrijo con los datos de la imagen que necesito nicopaez/password-api:fabric8-1.5.0
   a) cambio en metadata el name y el label passwordapi 
   b) en spec cambio el número de replicas a 3 y el nombre de la imagen passwordapi
   c) Cambio la etiqueta en selector passwordapi
   d) Genero el template con metadata de la imagen creada passwordapi 
      y containers con la imagen que voy a utilizar como base  nicopaez/password-api:fabric8-1.5.0
      en el puerto 4567

3) aplico el descriptor con  aplicarlo con "kubectl apply -f"

4) Hago kubectl get all para ver los pods que se crearon para luego acceder a uno.

5) Accedo a uno y veo que funcione:
kubectl exec -it pod/password-api-8b7db5f79-hr4sr bash

kubectl exec [POD] [COMMAND] is DEPRECATED and will be removed in a future version. Use kubectl exec [POD] -- [COMMAND] instead.
root@password-api-8b7db5f79-hr4sr:/usr/src/app# curl localhost:3000/password 
{"password":"!530GgRrDd>>"}
