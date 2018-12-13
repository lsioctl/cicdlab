FROM python:3.4-alpine

# Add our code
ADD . /opt/webapp/
WORKDIR /opt/webapp

RUN pip install -r requirements.txt

# Run the image as a non-root user
RUN adduser -D mywebapp
USER mywebapp

# Expose is NOT supported by Heroku
# EXPOSE 8000 	

# For Dev and CI/CD we have to set 
# $PORT
# For prod Heroku sets it
# It must be an HTTP service
CMD gunicorn --bind 0.0.0.0:$PORT --log-file - --access-logfile - wsgi
