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
- **api-nombreDelProyecto.yaml**: Configuración de despliegue para la API principal del proyecto.
- **hpa_api-nombreDelProyecto.yaml**: Configuración de escalado automático horizontal para la API.

### Web
- **web-nombreDelProyecto.yaml**: Configuración de despliegue para el servicio web.
- **hpa_web-nombreDelProyecto.yaml**: Configuración de escalado automático horizontal para el servicio web.

### Ingress
- **ingress_api-nombreDelProyecto.yaml**: Configuración de ingress para la API.
- **ingress_mysql-nombreDelProyecto.yaml**: Configuración de ingress para MySQL.
- **ingress_web-nombreDelProyecto.yaml**: Configuración de ingress para el servicio web.

### MySQL
- **mysql-nombreDelProyecto.yaml**: Configuración de despliegue para el servicio de base de datos MySQL.
- **mysql-storage-pvc-nombreDelProyecto.yaml**: Configuración del Persistent Volume Claim para MySQL.
- **mysql-storage-pv-nombreDelProyecto.yaml**: Configuración del Persistent Volume para MySQL.

### Servicios
- **services_api-nombreDelProyecto.yaml**: Configuración de servicios para la API.
- **services_mysql-nombreDelProyecto.yaml**: Configuración de servicios para MySQL.
- **services_web-nombreDelProyecto.yaml**: Configuración de servicios para el servicio web.

### Secretos
- **secret-api-nombreDelProyecto.yaml**: Configuración de secretos para la API.

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
5 .Abre un Pull Request.

Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

Contacto
Para cualquier consulta o comentario, por favor contacta a wowfoxz@gmail.com.

¡Gracias por utilizar nuestras plantillas de Kubernetes! Esperamos que sean de gran ayuda para tu proyecto.
