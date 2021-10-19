# phpinfo

```
git clone https://github.com/albertocuesta/phpinfo
cd phpinfo
git checkout main
```
```
php -f src/index.php -S 0.0.0.0:8080
```
```
curl localhost:8080/src/index.php
```

Instrucciones para construir imagen de Docker

```
git checkout santander-openshift
docker build --file Dockerfile --tag albertocuestanoriega/phpinfo:santander .
docker push albertocuestanoriega/phpinfo:santander
```

Instrucciones para ejecutar el contenedor
```
docker run -d --entrypoint /usr/bin/php --name phpinfo -p 8080:8080 --restart always -v ${PWD}/src/index.php:/index.php:ro albertocuestanoriega/phpinfo:santander -f index.php -S 0.0.0.0:8080
```
