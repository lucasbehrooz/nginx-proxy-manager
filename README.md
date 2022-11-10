# Nginx Proxy Manager

Utilizando o Ngrinx como Proxy Reverso

### Pre Requisitos

- Docker
- Docker Compose

1. Primeiro comando
```
docker-compose build
```
2. Segundo comando
```
docker network create nginx
```

3. Terceiro Comando
```
docker-compose up -d
```
4. Acesse o Portal de Administração

http://localhost:81 ou IP do Servidor:81

Faça login com o usuario e senha padrão e em seguida você deve mudar para o de sua preferencia.

```
email: admin@example.com
password: changeme
```


Obs. Todos os containers devem estar na mesma rede que o Nginx


docker run -d --name=website --network=nginx --restart=always mcr.microsoft.com/dotnet/samples:aspnetapp

docker run -d -p 8000:8000/tcp -p 9443:9443/tcp --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest