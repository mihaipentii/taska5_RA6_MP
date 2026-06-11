# Despliegue Automatizado en AWS EC2

## Arquitectura de la aplicación
- **Servicios:** Servidor Web Apache (HTTPD) de Linux.
- **Puertos:** Puerto `80` (HTTP) abierto para tráfico público.
- **Redes:** Instancia EC2 en AWS Academy con IP pública accesible (`52.90.166.39`).

## Requisitos previos
- Repositorio en GitHub con Secrets configurados `EC2_HOST`, `EC2_USER`, `EC2_SSH_KEY`.
- Instancia EC2 en ejecución con Apache activo.

## Pasos de instalación y puesta en marcha
El proyecto cuenta con un pipeline de CI/CD mediante GitHub Actions. Al realizar un `push` a la rama `main`, el workflow se conecta por SSH al servidor, limpia el directorio de despliegue y reinicia el servidor Apache automáticamente.

## Cómo verificar que funciona correctamente
1. Acceder al navegador web.
2. Introducir la dirección URL: `http://52.90.166.39`
3. Comprobar que la página web carga y muestra el contenido actualizado.