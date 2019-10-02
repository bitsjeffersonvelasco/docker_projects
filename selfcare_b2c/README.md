# Configuración para selfcare B2C

Esta imagen tine nginx, PHP-fpm 7.2 y NodeJs 10

Este configuración tiene habilitados los siguientes virtual host:
  
```
server_name _;
server_name selfcare.dev.bo;
server_name selfcare.dev.co;
server_name selfcare.dev.cr;
server_name selfcare.dev.hn;
server_name selfcare.dev.ni;
server_name selfcare.dev.py;
```

* Se deben configurar en el hosts de cara sistema operativo segùn se requiera

## Docker-compose comandos:

- `docker-composer up -d`  => se utiliza la primera vez para crear e iniciar los servicios definidos
- `docker-compose start` => se utiliza para inicir los sericios cuando estan detenidos
- `docker-compose stop` => se utiliza para detener los servicios
- `docker-compose ps` => se utiliza para listar los servicios que esta disponibles y ver sus estado
- `docker-compose restart` => se utiliza para reiniciar todos los servicios
- `docker exec "servicio" bash` => se utilizar para ingresar al contenedor del "servicio" especificado ejemplo: `docker-compose exec drupal bash`
- `docker-compose down` => se utilizar para DETENER y ELIMINAR todos los servicios