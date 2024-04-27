# Use the official Python image as base
FROM python:3.9

# Set the working directory in the container
WORKDIR /app

# Copy the Flask app files to the container
COPY . .

# Install Flask and other dependencies
RUN pip install --no-cache-dir Flask

# Expose the Flask app port
EXPOSE 5000

# Define the command to run the Flask app when the container starts
CMD ["python", "app.py"]
