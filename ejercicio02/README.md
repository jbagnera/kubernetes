# traigo la imagen
docker pull nicopaez/pingapp:3.0.0

# creo un tag a partir de la imagen origen
docker tag nicopaez/pingapp:3.0.0 jbagnera/pingapp:1.0.0

# me logeo
docker login -u jbagnera -p <password>

# pusheo el cambio
docker push jbagnera/pingapp:1.0.0

# para traer la imagen creada
docker pull jbagnera/pingapp:1.0.0
