FROM python:3.11

# Set working directory inside container
WORKDIR /app

# Copy all files into container
COPY . .

# Install dependencies
RUN pip install --upgrade pip \
    && pip install -r requirements.txt || pip install django==3.2

# Run DB migrations
RUN python manage.py migrate

# Expose port 8000
EXPOSE 8000

# Run the server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]


