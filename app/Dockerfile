# your code goes here ...
FROM python:3

WORKDIR /usr/src/app

# Copy files from the current directory to /usr/src/app
COPY . /usr/src/app

# Install dependencies
RUN pip install  -r src/requirements.txt

CMD ["python" ,"src/server.py"]
