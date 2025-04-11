FROM python:3.11

# Install distutils (required by Django 3.2)
RUN apt-get update && apt-get install -y python3-distutils

# Install Django
RUN pip install django==3.2

# Copy application code
COPY . .

# Run migrations
RUN python manage.py migrate

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

