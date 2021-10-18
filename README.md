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
```
