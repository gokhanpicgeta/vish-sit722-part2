# Dockerfile for book_catalog microservice

#Using official python runtime
FROM python:3.12-slim

#Set the working directory in the container
WORKDIR /app

#Copy te requirements file to the containers workspace
COPY book_catalog/requirements.txt /app/requirements.txt

#Install the required packages
RUN pip install -r requirements.txt

#Copy the application files to the container
COPY book_catalog /app/

#Expose the port the app runs on
EXPOSE 8081

#Set the database url to access postgress
ENV DATABASE_URL = postgresql://sit722_6_2_vish_user:wBDCot8ZCq6oJxPK4AZkWegjjz7gCfqx@dpg-cr9cmol6l47c73ckri10-a.singapore-postgres.render.com/sit722_6_2_vish

#Run the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8081"]