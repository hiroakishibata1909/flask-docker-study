# Select Ubuntu as Docker OS
FROM ubuntu:latest

# Update package list
RUN apt-get update -y
# Install python and build-essential
RUN apt-get install -y python-pip python-dev build-essential

# Copy current directory resources to /app directory of Ubuntu
COPY . /app
# Specify working directory
WORKDIR /app

# Install Flask
RUN pip install -r requirements.txt

# Execute app.py
ENTRYPOINT ["python"]
CMD ["app.py"]