# Kubernetes

# Paso 1: Verifica la instalación de kubectl (ejemplo de salida esperada, la versión puede variar)
kubectl version

# Paso 2: Configura kubectl para tu clúster (el comando específico varía según el proveedor de nube o configuración local)

# Paso 3: Asegúrate de tener tu archivo YAML. Ejemplo: deployment.yaml

# Paso 4: Ejecuta el archivo YAML
kubectl apply -f deployment.yaml

# Paso 5: Verifica que el Deployment se haya creado
kubectl get deployments

## obtener recursos:
'''
kubectl get pods - Lista todos los pods en el namespace actual.
kubectl get services - Lista todos los servicios.
kubectl get deployments - Lista todos los deployments.
kubectl get nodes - Lista todos los nodos del clúster.
'''

## Describir recursos:
'''
kubectl describe pod <nombre-del-pod> - Muestra información detallada sobre un pod específico.
kubectl describe service <nombre-del-servicio> - Muestra información detallada sobre un servicio específico.
'''

## Crear y aplicar configuraciones:
'''
kubectl apply -f <archivo.yaml> - Aplica la configuración definida en un archivo YAML.
kubectl create -f <archivo.yaml> - Crea un recurso a partir de un archivo YAML (usar apply es generalmente preferido).
'''

## Eliminar recursos:
'''
kubectl delete pod <nombre-del-pod> - Elimina un pod específico.
kubectl delete -f <archivo.yaml> - Elimina los recursos definidos en un archivo YAML.
'''

## Ejecutar comandos en contenedores:
'''
kubectl exec -it <nombre-del-pod> -- <comando> - Ejecuta un comando específico dentro de un contenedor en un pod.
Logs:

kubectl logs <nombre-del-pod> - Muestra los logs de un pod específico.
'''

## Port Forwarding:
'''
kubectl port-forward <nombre-del-pod> <puerto-local>:<puerto-remoto> - Permite acceder a un puerto de un pod desde tu máquina local.
Copiar archivos hacia/desde un contenedor:

kubectl cp <archivo-local> <nombre-del-pod>:<ruta-en-el-contenedor> - Copia un archivo desde tu máquina local a un contenedor.
kubectl cp <nombre-del-pod>:<ruta-en-el-contenedor> <archivo-local> - Copia un archivo desde un contenedor a tu máquina local.
'''

## Escalado:
'''
kubectl scale deployment <nombre-del-deployment> --replicas=<n> - Cambia el número de réplicas de un deployment.
'''

## Rollout y gestión de versiones:
'''
kubectl rollout status deployment/<nombre-del-deployment> - Muestra el estado de despliegue de un deployment.
kubectl rollout undo deployment/<nombre-del-deployment> - Revierte el último despliegue de un deployment.
'''