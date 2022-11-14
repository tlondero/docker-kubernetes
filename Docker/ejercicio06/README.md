# Ejercicio 6:

- Se siguen los pasos de la página https://catalog.redhat.com/software/containers/redhat-openjdk-18/openjdk18-openshift/58ada5701fbe981673cd6b10?container-tabs=gti
    - Se loguea en Red Hat y se crea un Registry Service Accounts.
    - docker login registry.redhat.io
    - docker pull registry.redhat.io/redhat-openjdk-18/openjdk18-openshift:1.15-1


- Se repiten los pasos del Ejercicio 4:
    - docker build -t password_e6.jar . --build-arg JAR_FILE=./passwordapi.jar
    - docker run -d -p 8080:8080 password_e6.jar
    - docker tag password_e6.jar:latest tlondero/password_e6.jar
    - docker push tlondero/password_e6.jar:latest

Imagen en dockerhub: https://hub.docker.com/r/tlondero/password_e6.jar