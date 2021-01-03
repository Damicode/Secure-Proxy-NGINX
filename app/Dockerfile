# your code goes here ...
FROM python:3

# Set an environment variable with the directory
ENV APP  /app

#make the directory

RUN mkdir $APP
#create a working Directory
WORKDIR $APP

RUN pwd
#verify what is in that directory
RUN ls
#EXPOSE 8000
# Copy files from source to the current directory 
COPY src/requirements.txt .

# Install dependencies from the requirements text file
RUN pip install  -r requirements.txt

#Copy everything else to the image container
COPY . .

#RUN ls
#CMD [ "uwsgi", "--ini", "app/src/server.ini" ]
#CMD ["python" ,"./src/server.py"]
