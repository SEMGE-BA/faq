# ERROS DOCKER

* The requested package semge/core 0.0.* exists as semge/core[1.0.3] but these are rejected by your constraint.
   * Como resolver:
      * Acessar arquivo composer.json 
      * Alterar em require : "semge/core": "0.0.*" para  "semge/core": "1.0.*"
      * Alterar em repositories : "version": "0.0.20" para "version": "1.0.5"
      * Alterar em repositories : "url": "http://192.168.6.12/semge-core-1.0.5.zip",


* ERROR: Couldn't connect to Docker daemon at htt+docker://localunixsocket - is it running?
If it's at a non-standard location, specify the URL with the DOCKER_HOST environment variable.
    * Como resolver:


# ERROS LARAVEL




