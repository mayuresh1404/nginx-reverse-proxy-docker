FROM python:3.11-slim

RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY . /app/

RUN pip install -r requirements.txt

CMD ["python", "app.py"]
