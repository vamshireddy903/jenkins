FROM python:3.11-slim

WORKDIR /app

# Install Django and pip dependencies
RUN pip install --no-cache-dir django==3.2

COPY . .

# Don't run migrate during build; run it at container start time
EXPOSE 8000

CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]
