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

# First stage: build the application
#FROM python:3.9-slim-buster AS builder
#WORKDIR /app
#COPY requirements.txt .
#RUN pip install --user -r requirements.txt
#COPY . .
#ENV FLASK_APP=app.py
#ENV FLASK_ENV=production
#RUN flask db upgrade
#RUN flask build

# Second stage: create the final container image
#FROM python:3.9-slim-buster
#WORKDIR /app
#COPY --from=builder /app/dist /app
#CMD ["flask", "run"]