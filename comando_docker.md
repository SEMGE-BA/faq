DOCKER- Listagem de Comandos
_________________________________________________________________________________________________


Criacão e configuração de container


Criar novo contener e deixar parado: (sudo) docker create nomeConteiner

Rodar uma versão específica de um sistema: sudo docker run -it centos:7 

Rodar um contêiner com comando: (sudo) docker run -ti nomeConteiner /bin/bash

Rodar um contêiner em backGround: (sudo) docker run -d nomeConteiner 

Rodar um contêiner: (sudo) docker run -ti nomeConteiner 

Sair do contêiner sem matá-lo : ctrl+p+q

Parar o contêiner: (sudo) docker stop ConteinerId

Para despausar: (sudo) docker unpause ConteinerId

Tirar da pausa : (sudo) docker start ConteinerId

Voltar para container:  (sudo) docker attach conteinerId

Acessar bash do container:  docker exec -it  conteinerId bash

renomear a imagem depois que foi criada: 

Saber status do contêiner : (sudo) docker stats  conteinerId

Processos rodados no contêiner: (sudo) docker top conteinerId 

Logs do contêiner: sudo docker logs contenierId

Remover o container: sudo docker rm contenierId

Remover um contêiner em execução:  sudo docker rm -f contenierId

Criar imagens  de um container: docker commit containerId nomeDaImagen

Remover imagem: docker rmi nomeImange

Remover imagem forcando: docker rmi -f nomeImange

Lista todos os conteiner rodando: sudo docker ps 

Lista todos os conteiner na máquina: sudo docker ps -a

Lista todas a imagens: sudo  docker images 
