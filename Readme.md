# Pipeline de procesamiento Next Procurement

En este git se encuentra el proyecto para la creación de una pipeline para el procesamiento de datos de licitaciones públicas de plataformas como TED y PLACE para su transformación a grafos de conocimiento. Para lograrlo, se ha recuperado parte del trabajo realizado en el proyecto They Buy For You (TBFY). 

Este proceso se ha encapsulado por completo en un contenedor de docker. Se pueden definir con libertad algunos de los valores principales como el endpoint de la pipeline, el puerto de la API, etc en el dokcer-compose.yaml. Otros valores como las reglas para el mapeado del grafo son también fácilmente accesibles.

El proyecto cuenta con un entrypoint en forma de API, a través del cual pueden enviarse todas las peticiones para el procesamiento de los datos, asi como proporcionar los archivos para su procesamiento.

## Instalación

La instalación requiere previamente la instalación de docker.

```
https://docs.docker.com/compose/install/
```

Una vez instalado docker, el proyecto se despliega con el comando 

```bash
docker-compose up --build -d 
```

en el directorio raiz del proyecto.

## Utilización

Para la utilización de la pipeline será necesario que el endpoint donde se desean desplegar los documentos del grafo de conocimiento este operativo. si no se modifica el valor de la variable de entorno PLATFORM_IP la pipeline buscará en localhost el servicio de fuseki para la publicación de los datos, y no se desplegará si no encuentra el servicio. 

Una vez desplegado correctamente, se puede acceder a la interfaz de la api en localhost:5050. Ahí viene toda la información relativa a la utilización de la API.

## Licencia
por confirmar.
