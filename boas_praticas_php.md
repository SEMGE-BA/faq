# Boas práticas com PHP

### Classes

Use sempre CamelCase ex: `Pessoa`, `ServidorPublico`

### Metódos

Use sempre first lowercase ex: `publicar()`, `andar()`, `pegarDados()`, `criarApelido()`

### Variáveis:
  * sempre em minúculo e snake case ex: `$pagamento_competencia`, `$pessoa`
  * Quando a variável representar uma lista coloque-a sempre no plural ou coloque o sufixo `_lista` ou `_list` ex: `$pessoas`, `$animais`, `$carro_lista`. Dẽ preferẽncia ao plural
  * DÊ NOMES ENTEDÍVEIS, nada de variáveis que não dizem o que são ex:
    ```php
    // Errado

    $ps = Pessoa::all();
    $a1 = Auxiliar::find(1);


    // Correto

    $pessoas_ativas = Pessoa::ativas();
    $qtd_pessoas = Pessoa::count();
    $pessoas = Pessoa::all();
    ```

### Espaços entre namespaces e imports

Dê o espaço de uma linha para diferenciar o name space e os imports próprios dos imports de pacotes externos ex:

```php
<?php

namespace App\Models;

use Illuminati\Facade\Auth;

use App\Sigp\Pessoa;

class Animal
{
    ...
}
```

### Uso das chaves

Para definição de classes de métodos pule uma linha e use as chaves abaixo.

```php
class MinhaClasse
{
    public function gerar()
    {
        ...
    }
}
```

Para `if`, `for`, `while` e etc use chaves na mesma linha.

```php
if($a == $b) {
    foreach($lista as $item){
        // do
    }
} else {
    // ...
}
```

Não use o `if` de uma linha, use sempre as chaves

```php
// Evite
if ( $a == $b )
    // bloco de código


// Forma correta
if($a == $b) {
    // bloco de código
}

```

### IDENTAÇÃO

IDENTE SEMPRE SEU CÓDIGO, ele ficará mais legível e fáil de entender.

```php
// Errado

if ( $a != $b ) {
throw new Exception("Algo errado");
}else{
foreach($lista as $item) {
if( $item->podeExibir() ){
    echo $item->exibir()
}
}
}


// Correto


if ( $a != $b ) {
    throw new Exception("Algo errado");
} else {
    foreach ($lista as $item) {
        if( $item->podeExibir() ){
            echo $item->exibir()
        }
    }
}
```
