# creo un html minombre.html

# levanto la imagen de nginx montando el directorio local con la carpeta que usa nginx
docker run -P -d -v $pwd:/usr/share/nginx/html/  -d nginx

# veo donde quedo apuntando la url:
juan@china:~/repo/kubernetes/ejercicio01 (master) $ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                   NAMES
96db255fd66a        nginx               "/docker-entrypoint.…"   12 minutes ago      Up 12 minutes       0.0.0.0:32774->80/tcp   tender_wozniak

# debería poder verla en http://0.0.0.0:32774/minombre.h

# veo donde quedo apuntando la url:
juan@china:~/repo/kubernetes/ejercicio01 (master) $ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                   NAMES
96db255fd66a        nginx               "/docker-entrypoint.…"   12 minutes ago      Up 12 minutes       0.0.0.0:32774->80/tcp   tender_wozniak

# debería poder verla en http://0.0.0.0:32774/minombre.html
