## POSSIVEIS ERROS E COMO RESOLVER

## ERROS DOCKER

(1) - The requested package semge/core 0.0.* exists as semge/core[1.0.3] but these are rejected by your constraint.

    (1.1)Como resolver:
         Acessar arquivo composer.json 
            Alterar em require : "semge/core": "0.0.*" para  "semge/core": "1.0.*"
            Alterar em repositories : "version": "0.0.20" para "version": "1.0.5"
            Alterar em repositories : "url": "http://192.168.6.12/semge-core-1.0.5.zip",


(2) - If it's at a non-standard location, specify the URL with the DOCKER_HOST environment variable.
    (2.2)Como resolver:


#ERROS LARAVEL




