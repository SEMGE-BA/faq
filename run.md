# How To SEMGE - Laravel

Passo a passo de criação de um projeto Laravel na SEMGE.


#### Dependências

* PHP >= 7.0
* OpenSSL PHP Extension
* PDO PHP Extension
* Mbstring PHP Extension
* Tokenizer PHP Extension
* XML PHP Extension


Entre na pasta workspace
`$	cd /$HOME/workspace`


Crie um novo projeto usando o comando `$	laravel new nome_projeto` ou `composer create-project --prefer-dist laravel/laravel nome_projeto`

Adicione o pacote `semge/core` no composer.json

```json
"require": {
    "php": ">=5.6.4",
    "laravel/framework": "5.3.*",
    "semge/core": "0.0.*",
},

...

"config": {
    "preferred-install": "dist",
    "secure-http": false
},
"repositories": [
    {
        "type": "package",
        "package": {
            "name": "semge/core",
            "version": "0.0.17",
            "dist": {
                "url": "http://192.168.6.25/semge-core-0.0.17.zip",
                "type": "zip"
            },
            "autoload": {
                "classmap": ["src/"]
            }
        }
    }
]

```

Execute o comando `composer update` para atualizar as dependências

Adicione o pacote `gwmoura/crudcmd` - `composer require gwmoura/crudcmd:"dev-master"`

Crie um arquivo chamado `.env.local` e nele coloque tudo que está no `.env` e depois altere para suas configurações locais

#### Executando seu projeto

`php artisan serve --host 0.0.0.0 --port $PORT --env=local`
