FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy only dependencies first (better caching)
COPY requirements.txt /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application source code
COPY app.py /app/

# Expose application port
EXPOSE 5000

# Run the application
CMD ["python", "app.py"]

