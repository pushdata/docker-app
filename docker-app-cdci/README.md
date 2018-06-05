__Whats done?__

-- Containerized a Web app

-- Two micro-services for this project

-- Setup interaction between these two services

-- Automated building images and spinning up containers




--Integrated everything
------Local dev – Version control repos – Build manager – Docker Registry – Cloud hosted 

--Deployed the bundle on a cloud VM (DigitalOcean)
-- Access application through the VM instantly

__Commands:__

```
docker run –d –name redis redis:3.2.0
docker build –t dockerapp:version
```

Container Linking :
```
docker run –d –p 5000:5000  --link redis dockerapp:v0.2
docker exec –it <containerid> bash
```

Invoking docker app running in Cloud VM :
```
docker-machine create --driver digitalocean --digitalocean-access-token <xxxxx> docker-app-machine
```
