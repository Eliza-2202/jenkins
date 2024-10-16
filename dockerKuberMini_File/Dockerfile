# Usa una imagen base adecuada
FROM tiangolo/uvicorn-gunicorn-fastapi:python3.9

# Establece el directorio de trabajo
WORKDIR /app

# Copia los requisitos y el código de tu aplicación
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

# Expone el puerto que usará la aplicación
EXPOSE 80

# Comando para correr la aplicación
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
