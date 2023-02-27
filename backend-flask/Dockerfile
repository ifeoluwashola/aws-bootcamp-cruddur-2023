# Pulling the base Image
#FROM python:3.10-slim-buster

# Setting working Directory
#WORKDIR /backend-flask

#Copy and Install the requirements
#COPY requirements.txt requirements.txt
#RUN pip3 install -r requirements.txt

# Copy the rest of the project
#COPY . .

# Set the Environment Variable
#ENV FLASK_ENV=development

# Exposing port and running the command inside the container
#EXPOSE ${PORT}
#CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

# Build Stage
FROM python:3.10-slim-buster AS builder

WORKDIR /backend-flask

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install --upgrade pip && pip install --user --no-cache-dir -r requirements.txt

# Copy the rest of the project
COPY . .

# Production Stage
FROM python:3.10-slim-buster

WORKDIR /backend-flask

# Copy the installed dependencies from builder stage
COPY --from=builder /root/.local /root/.local
COPY --from=builder /backend-flask .

# Set the Environment Variable
ENV FLASK_ENV=production

# Exposing port and running the command inside the container
EXPOSE 4567
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567"]
