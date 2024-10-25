# Usa una imagen oficial de Python
FROM python:3.9-slim

# Configura el directorio de trabajo en el contenedor
WORKDIR /app

# Copia el archivo de dependencias y luego instálalas
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copia el resto del proyecto
COPY . /app/

# Exponer el puerto que Django usará
EXPOSE 8000

# Comando para ejecutar el servidor de Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
