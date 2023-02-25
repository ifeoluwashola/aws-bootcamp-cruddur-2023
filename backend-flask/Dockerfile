# Pulling the base Image
FROM python:3.10-slim-buster

# Setting working Directory
WORKDIR /backend-flask

#Copy and Install the requirements
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

# Copy the rest of the project
COPY . .

# Set the Environment Variable
ENV FLASK_ENV=development

# Exposing port and running the command inside the container
EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]