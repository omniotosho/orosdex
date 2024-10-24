# Use an official Python runtime as the base image
FROM python:3.12-slim

# Set the working directory
WORKDIR /api

# Copy requirements file
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 5050

# Define environment variable
ENV FLASK_APP=app.py

# Define the command to run the app
CMD ["gunicorn", "--bind", "0.0.0.0:5050", "app:app"]