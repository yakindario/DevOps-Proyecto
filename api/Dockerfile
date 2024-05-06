FROM python:3.10-alpine

ENV FLASK_APP=app.py
ENV FLASK_ENV=development

WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
# Expone el puerto 5000 para acceder a la API
EXPOSE 5000
CMD ["flask", "run","--host=0.0.0.0"]
