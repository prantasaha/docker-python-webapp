# docker-python-webapp
This is a Docker Container for a web application using FastAPI

## demo app - developing with Docker

This demo app shows a simple web app wich says "Hello world" using 
- main.py with FAST API framework


All components are docker-based


#### To start the application

Step 1: Create virtual environment (I used linux commands.This might vary in windows)

    python3 -m venv venv

Step 2: start Virtual Environment 

    . venv/bin/activate

Step 3: Prequisites for fast API
    
    1. pip install fastapi
    2. pip install uvicorn

Step 4: Now build the docker image

	docker build -t pranta-python-fastapi .

Step 5: Now run the image

	docker run -p 8000:8000 pranta-python-fastapi

Now The webapp should say hello world in the url: http://0.0.0.0:8000/ (to see random items use http://0.0.0.0:8000/items/item_number. Here item_number can be any integer)

I have pushed the image to docker hub. You can directly pull the image my running the following command 
   
   docker pull pranta96/python-fastapi:v1
   
Then start the webapp using following command 

  `sudo docker run -p 8000:8000 pranta96/python-fastapi:v1`
