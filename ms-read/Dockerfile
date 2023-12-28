# Use an official Python runtime as a parent image
FROM python:3.11

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /usr/src/app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

ARG RABBITMQ_URL
ARG RABBITMQ_USERNAME
ARG RABBITMQ_PASSWORD
ARG RABBITMQ_QUEUE
ARG RABBITMQ_PREFETCH

# Define environment variable
ENV RABBITMQ_URL=${RABBITMQ_URL}
ENV RABBITMQ_USERNAME=${RABBITMQ_USERNAME}
ENV RABBITMQ_PASSWORD=${RABBITMQ_PASSWORD}
ENV RABBITMQ_QUEUE=${RABBITMQ_QUEUE}
ENV RABBITMQ_PREFETCH=${RABBITMQ_PREFETCH}

# Run app.py when the container launches
CMD ["python3", "ms-leitura.py"]