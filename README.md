# Plantillas de Kubernetes

Este repositorio contiene diversas plantillas de Kubernetes para desplegar diferentes componentes y servicios de nuestro proyecto. Cada plantilla está organizada y documentada para facilitar su uso y modificación según las necesidades del proyecto.

## Estructura del Repositorio

El repositorio está organizado de la siguiente manera:

PLANTILLAS-KUBERNETES/

├── api-nombreDelProyecto.yaml

├── hpa_api-nombreDelProyecto.yaml

├── hpa_web-nombreDelProyecto.yaml

├── ingress_api-nombreDelProyecto.yaml

├── ingress_mysql-nombreDelProyecto.yaml

├── ingress_web-nombreDelProyecto.yaml

├── mysql-nombreDelProyecto.yaml

├── mysql-storage-pvc-nombreDelProyecto.yaml

├── mysql-storage-pv-nombreDelProyecto.yaml

├── secret-api-nombreDelProyecto.yaml

├── services_api-nombreDelProyecto.yaml

├── services_mysql-nombreDelProyecto.yaml

├── services_web-nombreDelProyecto.yaml

└── web-nombreDelProyecto.yaml



## Descripción de las Plantillas

### API
- **api-nombreDelProyecto.yaml**: 
  - **Descripción**: Esta plantilla configura el despliegue de la API principal del proyecto.
  - **Uso**: Provee los recursos necesarios para correr la API en un pod.
  - **Explicación del Código**: Define un Deployment con replicas, especifica la imagen del contenedor, puertos y variables de entorno necesarios para la API.

- **hpa_api-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de escalado automático horizontal para la API.
  - **Uso**: Permite ajustar automáticamente el número de pods basados en la carga.
  - **Explicación del Código**: Define un HorizontalPodAutoscaler que ajusta las replicas del Deployment de la API según el uso de CPU.

### Web
- **web-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de despliegue para el servicio web.
  - **Uso**: Provee los recursos necesarios para correr el servicio web en un pod.
  - **Explicación del Código**: Similar a la plantilla de API, pero específica para el servicio web, con su propia imagen de contenedor y puertos.

- **hpa_web-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de escalado automático horizontal para el servicio web.
  - **Uso**: Ajusta automáticamente el número de pods del servicio web basados en la carga.
  - **Explicación del Código**: Define un HorizontalPodAutoscaler para el Deployment del servicio web, ajustando las replicas según el uso de CPU.

### Ingress
- **ingress_api-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de ingress para la API.
  - **Uso**: Maneja el acceso externo a los servicios de la API dentro del cluster.
  - **Explicación del Código**: Define las reglas de ingreso y las rutas que dirigen el tráfico a los servicios de la API.

- **ingress_mysql-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de ingress para MySQL.
  - **Uso**: Maneja el acceso externo a los servicios de MySQL dentro del cluster.
  - **Explicación del Código**: Similar a la plantilla de ingress para la API, pero específica para los servicios de MySQL.

- **ingress_web-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de ingress para el servicio web.
  - **Uso**: Maneja el acceso externo a los servicios web dentro del cluster.
  - **Explicación del Código**: Define las reglas de ingreso y las rutas que dirigen el tráfico a los servicios web.

### MySQL
- **mysql-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de despliegue para el servicio de base de datos MySQL.
  - **Uso**: Provee los recursos necesarios para correr MySQL en un pod.
  - **Explicación del Código**: Define un Deployment para MySQL, incluyendo la imagen del contenedor, puertos, y variables de entorno.

- **mysql-storage-pvc-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración del Persistent Volume Claim para MySQL.
  - **Uso**: Solicita almacenamiento persistente para MySQL.
  - **Explicación del Código**: Define un PersistentVolumeClaim que solicita espacio de almacenamiento en el cluster.

- **mysql-storage-pv-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración del Persistent Volume para MySQL.
  - **Uso**: Define el almacenamiento persistente para MySQL.
  - **Explicación del Código**: Define un PersistentVolume que proporciona el espacio de almacenamiento solicitado por el PVC.

### Servicios
- **services_api-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de servicios para la API.
  - **Uso**: Expone la API dentro del cluster.
  - **Explicación del Código**: Define un Service que expone los pods de la API a través de un puerto específico.

- **services_mysql-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de servicios para MySQL.
  - **Uso**: Expone MySQL dentro del cluster.
  - **Explicación del Código**: Similar al servicio para la API, pero específico para los pods de MySQL.

- **services_web-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de servicios para el servicio web.
  - **Uso**: Expone el servicio web dentro del cluster.
  - **Explicación del Código**: Define un Service que expone los pods del servicio web a través de un puerto específico.

### Secretos
- **secret-api-nombreDelProyecto.yaml**: 
  - **Descripción**: Configuración de secretos para la API.
  - **Uso**: Maneja la configuración de secretos y variables sensibles para la API.
  - **Explicación del Código**: Define un Secret que almacena información sensible como credenciales o claves API.


## Uso

Para desplegar alguna de estas plantillas en tu cluster de Kubernetes, utiliza el siguiente comando:

```bash
kubectl apply -f <nombre-de-la-plantilla>.yaml
```

Por ejemplo:

```bash
kubectl apply -f api-nombreDelProyecto.yaml
```
Asegúrate de tener el contexto correcto de Kubernetes configurado antes de aplicar las plantillas.

Contribución
Si deseas contribuir a este repositorio, por favor sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (git checkout -b feature/nueva-funcionalidad).
3. Realiza tus cambios y haz commit (git commit -am 'Agrega nueva funcionalidad').
4. Haz push a la rama (git push origin feature/nueva-funcionalidad).
5. Abre un Pull Request.

Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

Contacto
Para cualquier consulta o comentario, por favor contacta a wowfoxz@gmail.com.

¡Gracias por utilizar nuestras plantillas de Kubernetes! Esperamos que sean de gran ayuda para tu proyecto.
