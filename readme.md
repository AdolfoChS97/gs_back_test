# Test Genios Studio Backend

Esta es una aplicación web desarrollada en Django, que utiliza Docker para la contenedorización y PostgreSQL como base de datos.

## Estructura del Proyecto

```
/proyecto
│
├── app                # Código de la aplicación Django
│   ├── Dockerfile     # Dockerfile para construir la imagen
│   ├── requirements.txt # Dependencias de Python
│   └── ...
│
└── docker-compose.yml # Archivo de configuración de Docker Compose
```

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalados Python, Docker y pip.

### Instalación de Python

1. **Descargar Python**:
   - Ve al [sitio oficial de Python](https://www.python.org/downloads/) y descarga la versión más reciente para tu sistema operativo.

2. **Instalar Python**:
   - Sigue las instrucciones específicas de instalación para tu sistema operativo.

3. **Verificar la instalación**:
   ```bash
   python --version
   ```

### Instalación de pip

`pip` normalmente se incluye con las versiones recientes de Python. Para verificar si tienes `pip` instalado, ejecuta:
```bash
pip --version
```

Si no está instalado, puedes instalarlo utilizando el siguiente comando (si `get-pip.py` no está disponible, descárgalo desde el sitio oficial):
```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
```

### Instalación de Docker

1. **Descargar Docker**:
   - Ve al [sitio oficial de Docker](https://www.docker.com/products/docker-desktop) y descarga Docker Desktop para tu sistema operativo.

2. **Instalar Docker**:
   - Sigue las instrucciones específicas de instalación para tu sistema operativo.

3. **Verificar la instalación**:
   ```bash
   docker --version
   ```

## Configuración del Proyecto

### Clonar el Repositorio

Clona este repositorio en tu máquina local:
```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```

### Construir y Ejecutar el Contenedor

1. **Construir la imagen de Docker**:
   Desde la raíz del proyecto, ejecuta:
   ```bash
   docker-compose build
   ```

2. **Iniciar los contenedores**:
   ```bash
   docker-compose up
   ```

## Acceder a la Aplicación

Una vez que los contenedores estén en funcionamiento, podrás acceder a la aplicación en tu navegador en la siguiente URL:
```
http://localhost:8000
```

## Ejecutar Migraciones

Para aplicar las migraciones de la base de datos, abre una nueva terminal y ejecuta:
```bash
docker-compose exec app python manage.py migrate
```

## Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas, sugerencias o mejoras, no dudes en abrir un issue o un pull request.

## Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE).
