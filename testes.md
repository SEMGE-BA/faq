# Testes

Para executar os testes utilizamos o [PHPUNIT](https://phpunit.de/).

#### Executando os testes

Dentro do seu projeto execute `./vendor/bin/phpunit` em alguns projetos os testes podem ser interrompidos por falta de memória então execute o teste com o parâmetro `memory_limit` ex: `./vendor/bin/phpunit -d memory_limit=-1` para executar os testes sem limite de memória.

Para testes de browser usamos o [`laravel/dusk`](https://laravel.com/docs/5.4/dusk) que por debaixo dos panos usa o selenium, mas sem precisar instalar o JDK ou selenium na máquina. Como testes de browser são muito lentos evitamos utilizar este recurso, focando nos testes unitários com `phpunit`.
