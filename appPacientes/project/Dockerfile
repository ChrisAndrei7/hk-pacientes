FROM python:3.7.3-stretch

# Set unbuffered output for python
ENV PYTHONUNBUFFERED 1

# Create app directory
WORKDIR /appPacientes

# Install app dependencies
COPY project/requirements.txt .
RUN pip install -r requirements.txt

# Bundle app source
COPY project .

# Expose port
EXPOSE 8003

# entrypoint to run the django.sh file
ENTRYPOINT ["bash", "-e", "./django.sh"]
