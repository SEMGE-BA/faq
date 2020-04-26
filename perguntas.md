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
       * Adicinar o usuário ao grupo Docker - rode o seguinte comando `sudo usermod -aG docker [nome_do_usuario]` ou `sudo usermod -aG docker $USER` onde `$USER` é a variável de ambiente do linux que traz o nome do usuário logado.

* [Composer\Downloader\TransportException]
  The "http://192.168.6.12/christi/semge-christi-0.0.7.zip" file could not be downloaded: failed to open stream: No route to host
  * Como Resolver: ?




# ERROS LARAVEL

# ERROS DE FERRAMENTAS

* Erro de timezone - ORA-01882: região de fuso horário  não encontrada
  * Sqldeveloper
    * Abrir o arquivo `/opt/sqldeveloper/sqldeveloper/bin/sqldeveloper.conf`
    * Adicionar essa linha `AddVMOption -Duser.timezone="+00:00"`
  * DBEaver
    * Abrir o arquivo `/usr/share/dbeaver/dbeaver.ini`
    * Adicionar a linha `-Duser.timezone=UTC`
