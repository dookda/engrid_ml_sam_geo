### structure
```bash
my_fastapi_project/
│
├── app/
│   ├── __init__.py
│   └── main.py  # Your FastAPI application code
│   
│
├── Dockerfile
├── docker-compose.yml
└── .dockerignore
└── requirements.txt
```

### build image
```bash
docker build -t fastapi .
```

### run container 
```bash
docker run -d --name fastapi -p 80:80 fastapi
```

### run exect command in container & hot reload
```bash
docker run --rm -it --name fastapi $(pwd)/app/:/app/ -p 80:80 -v fastapi /start-reload.sh
```

### remove container
```bash
docker rm -f fastapi
```

### push image to docker hub
```bash
docker tag fastapi:latest <your docker hub username>/fastapi:latest
docker push <your docker hub username>/fastapi:latest
```


### save package list to requirements.txt
```bash 
pip freeze > requirements.txt
```
