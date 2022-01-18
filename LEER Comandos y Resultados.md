# Resultados de los puntos

## ---------------
## Ejecutamos servidor
## ---------------
>node src/main.js -p 8089
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 9856

## ---------------
>node src/main.js -p 8089 -m CLUSTER

Número de procesadores: 8
PID MASTER 11168
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 16368
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 13044
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 1872
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 5824
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 7056
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 2420
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 5324
Servidor HTTP escuchando en el puerto 8089 - PID WORKER 8480


## ---------------
## Ejecutamos nodemon con parametro cluster
## ---------------

>nodemon src/main.js -p 8081 -m CLUSTER
[nodemon] 2.0.13
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node src/main.js -p 8081 -m CLUSTER`
Número de procesadores: 8
PID MASTER 12520
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 9596
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 5324
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 16320
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 8464
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 9440
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 1180
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 10944
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 14296

>tasklist /fi "imagename eq node.exe"

Nombre de imagen               PID Nombre de sesión Núm. de ses Uso de memor
========================= ======== ================ =========== ============
node.exe                      9516 Console                    1    27.500 KB
node.exe                     12520 Console                    1    68.480 KB
node.exe                      9440 Console                    1    68.404 KB
node.exe                      8464 Console                    1    67.772 KB
node.exe                      9596 Console                    1    68.104 KB
node.exe                      1180 Console                    1    68.256 KB
node.exe                      5324 Console                    1    68.020 KB
node.exe                     16320 Console                    1    67.892 KB
node.exe                     10944 Console                    1    68.536 KB
node.exe                     14296 Console                    1    68.136 KB

## ---------------
## Ejecutamos nodemon con parametro fork
## ---------------

> nodemon src/main.js -p 8081 -m FORK

[nodemon] 2.0.13
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node src/main.js -p 8081 -m FORK`
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 2000

> tasklist /fi "imagename eq node.exe"

Nombre de imagen               PID Nombre de sesión Núm. de ses Uso de memor
========================= ======== ================ =========== ============
node.exe                      9852 Console                    1    31.560 KB
node.exe                      2000 Console                    1   100.068 KB

## ---------------
## Ejecutamos con Forever
## ---------------

>forever src/main.js -p 8081 -m CLUSTER
warn:    --minUptime not set. Defaulting to: 1000ms
warn:    --spinSleepTime not set. Your script will exit if it does not stay up for at least 1000ms
(node:8700) Warning: Accessing non-existent property 'padLevels' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:8700) Warning: Accessing non-existent property 'padLevels' of module exports inside circular dependency
Número de procesadores: 8
PID MASTER 14288
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 16260
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 3276
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 13384
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 1656
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 12680
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 8748
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 3132
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 15516

>tasklist /fi "imagename eq node.exe"

Nombre de imagen               PID Nombre de sesión Núm. de ses Uso de memor
========================= ======== ================ =========== ============
node.exe                      8700 Console                    1    30.964 KB
node.exe                     14288 Console                    1    68.376 KB
node.exe                     16260 Console                    1    67.740 KB
node.exe                     12680 Console                    1    68.160 KB
node.exe                      1656 Console                    1    67.800 KB
node.exe                      3276 Console                    1    68.252 KB
node.exe                      8748 Console                    1    67.968 KB
node.exe                     13384 Console                    1    68.000 KB
node.exe                     15516 Console                    1    67.756 KB
node.exe                      3132 Console                    1    68.012 KB

## ---------------
## Cerramos procesos y se activan automaticamente
## ---------------

>forever src/main.js -p 8081 -m CLUSTER
warn:    --minUptime not set. Defaulting to: 1000ms
warn:    --spinSleepTime not set. Your script will exit if it does not stay up for at least 1000ms
(node:2956) Warning: Accessing non-existent property 'padLevels' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:2956) Warning: Accessing non-existent property 'padLevels' of module exports inside circular dependency
Número de procesadores: 8
PID MASTER 14300
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 1588
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 9444
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 8164
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 9488
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 8444
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 13112
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 13532
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 12900
Worker 13112 died 17/1/2022 16:46:33
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 10936
Worker 13532 died 17/1/2022 16:46:42
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 1176

## ---------------
### Listamos con Forever
## ---------------
>forever list

(node:9328) Warning: Accessing non-existent property 'padLevels' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:9328) Warning: Accessing non-existent property 'padLevels' of module exports inside circular dependency
info:    Forever processes running
data:        uid  command                            script                                                                         forever pid   id logfile                        uptime
data:    [0] IAIG "C:\Program Files\nodejs\node.exe" C:\Users\DyA\Desktop\Coder\Clase_15\entrega15\1\src\main.js -p 8081 -m CLUSTER 2956    14300    C:\Users\DyA\.forever\IAIG.log 0:0:2:15.513000000000005


## ---------------
## PM2
## ---------------
### FORK
>pm2 start src/main.js --name="Server1" --watch -- 8081
[PM2] Starting C:\Users\DyA\Desktop\Coder\Clase_15\entrega15\1\src\main.js in fork_mode (1 instance)
[PM2] Done.
┌─────┬────────────┬─────────────┬─────────┬─────────┬──────────┬────────┬──────┬───────────┬──────────┬──────────┬──────────┬──────────┐
│ id  │ name       │ namespace   │ version │ mode    │ pid      │ uptime │ ↺    │ status    │ cpu      │ mem      │ user     │ watching │
├─────┼────────────┼─────────────┼─────────┼─────────┼──────────┼────────┼──────┼───────────┼──────────┼──────────┼──────────┼──────────┤
│ 0   │ Server1    │ default     │ 1.0.0   │ fork    │ 14620    │ 0s     │ 0    │ online    │ 0%       │ 31.6mb   │ DyA      │ enabled  │
└─────┴────────────┴─────────────┴─────────┴─────────┴──────────┴────────┴──────┴───────────┴──────────┴──────────┴──────────┴──────────┘

### CLUSTER
>pm2 start src/main.js --name="Server3" --watch -i max -- 8083
[PM2] Starting C:\Users\DyA\Desktop\Coder\Clase_15\entrega15\1\src\main.js in cluster_mode (0 instance)
[PM2] Done.
┌─────┬────────────┬─────────────┬─────────┬─────────┬──────────┬────────┬──────┬───────────┬──────────┬──────────┬──────────┬──────────┐
│ id  │ name       │ namespace   │ version │ mode    │ pid      │ uptime │ ↺    │ status    │ cpu      │ mem      │ user     │ watching │
├─────┼────────────┼─────────────┼─────────┼─────────┼──────────┼────────┼──────┼───────────┼──────────┼──────────┼──────────┼──────────┤
│ 0   │ Server3    │ default     │ 1.0.0   │ cluster │ 13040    │ 0s     │ 0    │ online    │ 0%       │ 32.1mb   │ DyA      │ enabled  │
│ 1   │ Server3    │ default     │ 1.0.0   │ cluster │ 7356     │ 0s     │ 0    │ online    │ 0%       │ 31.9mb   │ DyA      │ enabled  │
│ 2   │ Server3    │ default     │ 1.0.0   │ cluster │ 1844     │ 0s     │ 0    │ online    │ 0%       │ 32.0mb   │ DyA      │ enabled  │
│ 3   │ Server3    │ default     │ 1.0.0   │ cluster │ 11316    │ 0s     │ 0    │ online    │ 0%       │ 32.0mb   │ DyA      │ enabled  │
│ 4   │ Server3    │ default     │ 1.0.0   │ cluster │ 10176    │ 0s     │ 0    │ online    │ 0%       │ 31.8mb   │ DyA      │ enabled  │
│ 5   │ Server3    │ default     │ 1.0.0   │ cluster │ 15424    │ 0s     │ 0    │ online    │ 0%       │ 31.9mb   │ DyA      │ enabled  │
│ 6   │ Server3    │ default     │ 1.0.0   │ cluster │ 14300    │ 0s     │ 0    │ online    │ 0%       │ 32.1mb   │ DyA      │ enabled  │
│ 7   │ Server3    │ default     │ 1.0.0   │ cluster │ 13052    │ 0s     │ 0    │ online    │ 0%       │ 31.8mb   │ DyA      │ enabled  │
└─────┴────────────┴─────────────┴─────────┴─────────┴──────────┴────────┴──────┴───────────┴──────────┴──────────┴──────────┴──────────┘

>pm2 stop "Server3"
[PM2] Applying action stopProcessId on app [Server3](ids: [
  0, 1, 2, 3,
  4, 5, 6, 7
])
[PM2] [Server3](1) ✓
[PM2] [Server3](0) ✓
[PM2] [Server3](2) ✓
[PM2] [Server3](3) ✓
[PM2] [Server3](4) ✓
[PM2] [Server3](5) ✓
[PM2] [Server3](6) ✓
[PM2] [Server3](7) ✓
┌─────┬────────────┬─────────────┬─────────┬─────────┬──────────┬────────┬──────┬───────────┬──────────┬──────────┬──────────┬──────────┐
│ id  │ name       │ namespace   │ version │ mode    │ pid      │ uptime │ ↺    │ status    │ cpu      │ mem      │ user     │ watching │
├─────┼────────────┼─────────────┼─────────┼─────────┼──────────┼────────┼──────┼───────────┼──────────┼──────────┼──────────┼──────────┤
│ 0   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 1   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 2   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 3   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 4   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 5   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 6   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
│ 7   │ Server3    │ default     │ 1.0.0   │ cluster │ 0        │ 0      │ 1    │ stopped   │ 0%       │ 0b       │ DyA      │ disabled │
└─────┴────────────┴─────────────┴─────────┴─────────┴──────────┴────────┴──────┴───────────┴──────────┴──────────┴──────────┴──────────┘

>pm2 delete "Server3"
[PM2] Applying action deleteProcessId on app [Server3](ids: [
  0, 1, 2, 3,
  4, 5, 6, 7
])
[PM2] [Server3](0) ✓
[PM2] [Server3](1) ✓
[PM2] [Server3](2) ✓
[PM2] [Server3](3) ✓
[PM2] [Server3](4) ✓
[PM2] [Server3](5) ✓
[PM2] [Server3](6) ✓
[PM2] [Server3](7) ✓
┌─────┬───────────┬─────────────┬─────────┬─────────┬──────────┬────────┬──────┬───────────┬──────────┬──────────┬──────────┬──────────┐
│ id  │ name      │ namespace   │ version │ mode    │ pid      │ uptime │ ↺    │ status    │ cpu      │ mem      │ user     │ watching │
└─────┴───────────┴─────────────┴─────────┴─────────┴──────────┴────────┴──────┴───────────┴──────────┴──────────┴──────────┴──────────┘

>pm2 list
┌─────┬───────────┬─────────────┬─────────┬─────────┬──────────┬────────┬──────┬───────────┬──────────┬──────────┬──────────┬──────────┐
│ id  │ name      │ namespace   │ version │ mode    │ pid      │ uptime │ ↺    │ status    │ cpu      │ mem      │ user     │ watching │
└─────┴───────────┴─────────────┴─────────┴─────────┴──────────┴────────┴──────┴───────────┴──────────┴──────────┴──────────┴──────────┘

## ---------------
## NginX
## ---------------
### Primera parte
>node src/main -p 8080
Servidor HTTP escuchando en el puerto 8080 - PID WORKER 12472

>node src/main -p 8081 -m CLUSTER
Número de procesadores: 8
PID MASTER 2452
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 1292
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 10260
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 2488
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 4480
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 3332
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 11112
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 14796
Servidor HTTP escuchando en el puerto 8081 - PID WORKER 7216

Archivo nginx.conf
------------------

worker_processes  1;

events {
    worker_connections  1024;
}

http {
    include       mime.types;
    default_type  application/octet-stream;
    sendfile        on;
    keepalive_timeout  65;

    # primer servidor
    upstream node_app { 
        server 127.0.0.1:8080;
    }
    # segundo servidor 
    upstream node_randoms {
        server 127.0.0.1:8081;
    }

    server {
        listen       80;
        server_name  nginxNode;

        # location / {
        #     root   html;
        #     index  index.html index.htm;
        # }
        
        location /api/randoms {
            proxy_pass http://node_randoms;
        }
        location / {
            proxy_pass http://node_app;
        }

        #error_page  404              /404.html;

        # redirect server error pages to the static page /50x.html
        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   html;
        }
    }
}

## ---------------
## NginX
## ---------------
### Segunda parte: balanceo de carga

>node src/main -p 8080
Servidor HTTP escuchando en el puerto 8080 - PID WORKER 6912

>node src/main -p 8082
Servidor HTTP escuchando en el puerto 8082 - PID WORKER 5656

>node src/main -p 8083
Servidor HTTP escuchando en el puerto 8083 - PID WORKER 6668

>node src/main -p 8084
Servidor HTTP escuchando en el puerto 8084 - PID WORKER 14804

>node src/main -p 8085
Servidor HTTP escuchando en el puerto 8085 - PID WORKER 10188

>tasklist /fi "imagename eq node.exe"

Nombre de imagen               PID Nombre de sesión Núm. de ses Uso de memor
========================= ======== ================ =========== ============
node.exe                      9492 Console                    2    34.536 KB
node.exe                      5656 Console                    2    70.052 KB
node.exe                      6668 Console                    2    69.548 KB
node.exe                     14804 Console                    2    70.856 KB
node.exe                     10188 Console                    2    70.456 KB
node.exe                      6912 Console                    2    69.324 KB

Archivo nginx.conf
------------------
worker_processes  1;

events {
    worker_connections  1024;
}

http {
    include       mime.types;
    default_type  application/octet-stream;
    sendfile        on;
    keepalive_timeout  65;

    # primer servidor
    upstream node_app { 
        server 127.0.0.1:8080;
    }
    # segundo grupo de servidores
    upstream node_randoms {
        server 127.0.0.1:8082;
        server 127.0.0.1:8083;
        server 127.0.0.1:8084;
        server 127.0.0.1:8085;
    }

    server {
        listen       80;
        server_name  nginxNode;
       
        location /api/randoms {
            proxy_pass http://node_randoms;
        }
        location / {
            proxy_pass http://node_app;
        }
    }
}
