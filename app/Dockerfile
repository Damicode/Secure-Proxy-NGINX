# your code goes here ...
FROM python:3

# Set an environment variable with the directory
ENV APP  /app

#make the directory

RUN mkdir $APP
#create a working Directory
WORKDIR $APP

RUN pwd
RUN ls
#EXPOSE 8000
# Copy files from the current directory to /usr/src/app
COPY src/requirements.txt .

# Install dependencies
RUN pip install  -r requirements.txt

#Copy everything else to the image container
COPY . .
RUN pwd
#RUN ls
#CMD [ "uwsgi", "--ini", "app/src/app.ini" ]
#CMD ["python" ,"./src/server.py"]
