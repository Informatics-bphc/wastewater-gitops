# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the application files
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# Expose port 80 for the web server
EXPOSE 80

# Define the command to run the application
CMD ["gunicorn", "-b", "0.0.0.0:80", "app:app"]
