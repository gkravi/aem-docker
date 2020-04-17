# aem-docker

### Setp-1: we have to build our base image i.e ~/aem/Dockerfile. To do so we have to goto the aem directory. 
```
cd aem
```

### Step-2: Run the command to build image 
```
docker build -t aem .
```

### Step-3: To run all the container at once use the command: 
 ```
docker-compose up
```

### Step-4: To run the different instance one by one 
      
```
docker build -t author . 
docker run -p 4504:4504 author
```


Similarly to build other images and execute it use below commands:

### AEM Publish image

```
docker build -t publish .

docker run -p 4505:4505 publish
```

### AEM Author image
```
docker build -t author .

docker run -p 4504:4504 author
```

### AEM Dispatcher image
```
docker build -t dispatcher .

docker run -p 8181:81 dispatcher
```


