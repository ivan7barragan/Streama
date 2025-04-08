# Streama
Despliegue de servidor Streama con docker 

# 🎬 Deploy de Streama con Docker (Paso a Paso)

Este repositorio te guía paso a paso para desplegar un servidor [Streama](https://github.com/streamaserver/streama), una plataforma tipo Netflix, usando Docker.

---

## 📋 Requisitos previos

Antes de comenzar, asegúrate de tener instalado:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Git](https://git-scm.com/)

---

## 🚀 Paso a paso

### 1️⃣ Clonar el repositorio (opcional)

Si estás usando un repositorio propio:

```bash
git clone https://github.com/tuusuario/streama-docker.git
cd streama-docker
```

Si no, simplemente crea una carpeta nueva:

```bash
mkdir streama-server
cd streama-server
```

### 2️⃣ Crear el archivo `docker-compose.yml`
Crea un archivo llamado `docker-compose.yml` en la raíz de tu proyecto y añade el siguiente contenido:

```yaml
version: '3.8'

services:
  streama:
    image: streamaserver/streama:latest
    container_name: streama
    ports:
      - "8080:8080"
    volumes:
      - ./data:/streama
    restart: unless-stopped
```

### 3️⃣ Iniciar el contenedor
Ejecuta el siguiente comando en la misma carpeta donde está el docker-compose.yml:

```bash
docker-compose up -d
```

### 4️⃣ Acceder a Streama 

Abre tu navegador y ve a `http://localhost:8080`. Deberías ver la interfaz de Streama.

### 5️⃣ Iniciar sesión
Credenciales por defecto:

Usuario: admin
Contraseña: admin
