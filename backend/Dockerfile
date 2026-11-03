FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .
RUN python -m pip install --upgrade pip && pip install --no-cache-dir --default-timeout=300 --retries=10 -r requirements.txt

COPY backend/ ./

EXPOSE 8000

CMD ["python", "api.py"]