
## Docker Commands 

Creating a container Image:
```bash
docker build -t user-microservice .
```
or
```bash
docker build . > build.log 2>&1
```

Test image localy
```bash
docker run -p 8080:80 user-microservice
```



Push Image to AWS Lightsail:
aws ecr get-login-password --region region | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com

docker push aws_account_id.dkr.ecr.region.amazonaws.com/my-repo-name:my-tag


## PUSH Docker hub:

1- Create a Docker Hub Account: If you haven't already, sign up for a Docker Hub account at hub.docker.com.

2- Tag Your Image: Before you can push your image to Docker Hub, you need to tag it with your Docker Hub username and repository name. Assuming you have a Docker image named my-image:
```bash
docker tag my-image your-docker-hub-username/my-image
```

3- Login to Docker Hub: Use the docker login command to authenticate with Docker Hub:
```bash
docker login
```

4- Push Your Image to Docker Hub: Once logged in, you can push your image to Docker Hub:
```bash
docker push your-docker-hub-username/my-image
```

5- Verify Image on Docker Hub: Visit hub.docker.com and log in to your Docker Hub account. You should see your image listed in your repository.


## Especifications:
- Marketing de empresas (coffee shop, restaurantes, lugares de eventod)
- Criacao de eventos organizados de forma aleatoria
- display de pessoas com mesmos interesses  que voce (possibilitante amizade)
- criacao de chat entre usuario
- usuario podera pagar para criar evento com pre definicoes e algoritmo ira procurar por pessoas com os interesses baseados na pre definicao do usuario
