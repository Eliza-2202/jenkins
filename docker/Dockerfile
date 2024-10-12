# Dockerfile
FROM python:3.9

# Establecer el directorio de trabajo
WORKDIR /app

# Copiar los archivos de requisitos y el código fuente
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# Exponer el puerto en el que corre la aplicación
EXPOSE 8000

# Comando para correr la aplicación con uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]

