# Ejercicio 4:
docker build -t password.jar . --build-arg JAR_FILE=./passwordapi.jar
docker run -d -p 8080:8080 password.jar
docker tag password.jar:latest tlondero/password.jar
docker push tlondero/password.jar:latest

Imagen en dockerhub: https://hub.docker.com/repository/docker/tlondero/password.jar