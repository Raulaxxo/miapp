# miapp

> **Nota:** Si deseas hacer pruebas o contribuir, realiza un fork de este repositorio desde GitHub.

Este es un repositorio de prueba para desplegar un servicio en Kubernetes usando Minikube.

## Estructura de carpetas

- `nginx/deployment.yml`: Deployment de ejemplo usando la imagen `gcr.io/google-containers/echoserver:2.0`.
- `nginx/service.yml`: Service tipo NodePort para exponer el deployment.

## Despliegue rápido

1. Aplica los manifiestos:
   ```bash
   kubectl apply -f nginx/deployment.yml -n nginx
   kubectl apply -f nginx/service.yml -n nginx
   ```
2. Accede al servicio:
   ```bash
   minikube service nginx-service -n nginx --url
   ```

Esto mostrará la URL para acceder al servicio, donde podrás ver el nombre del pod que responde a cada petición.
