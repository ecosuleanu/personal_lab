# your code goes here ...
# app/Dockerfile

FROM python:3.8-slim

# Set working directory inside the container
WORKDIR /app

# Copy requirements.txt and install dependencies
COPY src/requirements.txt .
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Copy the application code to the working directory
COPY src/ .

# Expose port 8000
EXPOSE 8000

# Command to run the application using gunicorn
CMD ["gunicorn", "-b", "0.0.0.0:8000", "server:app"]