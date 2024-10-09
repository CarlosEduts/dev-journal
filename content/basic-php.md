---
title: 📜 O Básico que Você Precisa Saber de PHP
description: Uma introdução à linguagem PHP, abordando sintaxe, variáveis, arrays, funções, classes e muito mais.
date: 2024-10-01
draft: false
tags:
  - PHP
  - programação web
  - backend
  - desenvolvimento
aliases:
  - introdução ao PHP
  - fundamentos de PHP
---

PHP (Hypertext Preprocessor) é uma linguagem de programação voltada para o desenvolvimento web. Criada em 1994 por Rasmus Lerdorf, ela é usada principalmente no lado do servidor para criar páginas dinâmicas.

- Inspiração da postagem: [cheatsheets.zip](https://cheatsheets.zip/php).
- Para mais informações, acesse o site oficial: [www.php.net](https://www.php.net/).

## Executando Códigos em PHP

```bash
# Executa um arquivo PHP no terminal
php nome_do_arquivo.php
```

### Estrutura Básica

Para iniciar um código em PHP, utilize as tags de abertura e fechamento:

```php
<?php
// Exibe uma mensagem na tela
echo "Olá, Mundo!";
?>
```

Todo o conteúdo fora dessas tags será tratado como HTML puro.

### Comentários

```php
# Comentário de uma linha

// Comentário de uma linha

/* Comentário de múltiplas linhas, útil para
   descrever blocos de código ou adicionar notas detalhadas */
```

### Variáveis e Constantes

```php
$num = 10;           // Número inteiro
$float = 0.5;        // Número decimal
$string = "Texto";   // Texto ou string
$bool = true;        // Valor booleano (verdadeiro ou falso)
$null = null;        // Valor nulo, indicando ausência de valor

define("CONSTANTE", "Valor fixo");  // Constante, valor imutável
```

### Concatenando Strings

```php
$greeting = "Olá, ";
$name = "Mundo!";

// Concatena usando aspas duplas e variáveis
echo "$greeting $name";

// Concatena usando o operador ponto (.)
echo $greeting . $name;

// Adiciona diretamente uma string ao valor de uma variável
$greeting .= "Mundo!";  // Resultado: "Olá, Mundo!"
```

### Múltiplas linhas de String

```php
$var1 = "Olá, Mundo!"

$var2 = <<<END
	Múltiplas linhas string
	$var1
END;

$var3 = <<<'END'
	Múltiplas linhas string
	$var1
END; # O valor dentro da string não será formatado

```

### Manipulação de Strings

```php
$str = "Olá, Usuário!";

// Indice
//        O | l | á | , |   | U | s | u | á | r | i | o | !
//        0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |10 |11 |12
//       -13|-12|-11|-10|-9 |-8 |-7 |-6 |-5 |-4 |-3 |-2 |-1

echo strlen($str);       # >> 13
echo substr($str, 0, 3); # >> Olá
echo strtoupper($str)    # >> OLÁ, USUÁRIO!
echo strtolower($str)    # >> olá, usuário!

```

### Arrays

```php
// Array numérico com índices automáticos
$numeros = [1, 2, 3, 4];

// Adiciona um número a 5º posição do array
$numeros[4] = 5;

// Deleta a variavel da 2º posição do array (3)
unset($numeros[2]);

// Arrays de strings
$array1 = ["Olá", "Mundo", "!"];
$array2 = array("Olá", "Mundo", "!");

// Array associativo (chave => valor)
$assocArray = ["chave" => "valor"];

// Array aninhado, onde cada elemento é outro array
$arrayAninhado = [
    [1, 2],
    [3, 4]
];
```

### Funções

```php
// Define uma função que soma dois números
function soma($a, $b = 1) {
    return $a + $b;  // Retorna a soma de $a e $b
}

// Chama a função com um argumento (b = 1 por padrão)
echo soma(5);  // Saída: 6
```

### Classes e Objetos

```php
// Define uma classe Pessoa
class Pessoa {
    public $nome;

    // Método construtor que define o nome ao criar o objeto
    public function __construct($nome) {
        $this->nome = $nome;
    }

    // Método para exibir o nome da pessoa
    public function exibirNome() {
        echo "Nome: " . $this->nome;
    }
}

// Cria uma instância da classe Pessoa
$joao = new Pessoa("João");
$joao->exibirNome();  // Saída: Nome: João
```

### Operadores

| Aritmética |               |
| ---------- | ------------- |
| +          | Adição        |
| -          | Subtração     |
| \*         | Multiplicação |
| /          | Divisão       |
| %          | Modulo        |
| \*\*       | Exponenciação |
| Atribuição |               |
| +=         | a = a + b     |
| -=         | a = a - b     |
| \*=        | a = a \* b    |
| /=         | a = a / b     |
| %=         | a = a % b     |

| Comparação |                |
| ---------- | -------------- |
| ==         | Igual          |
| ===        | Idêntico       |
| ≠ / <>     | Não igual      |
| ≠=         | Não idêntico   |
| <          | Menor que      |
| >          | Maior que      |
| ≤          | Menor ou igual |
| ≥          | Maior o igual  |

| Logico   |           |
| -------- | --------- |
| and / && | And (e)   |
| or       | Or (ou)   |
| !        | Not (Não) |

### Condicionais

```php
$a = 10;
$b = 20;

// Compara dois valores e executa diferentes ações
if ($a > $b) {
    echo "a é maior que b";
} elseif ($a == $b) {
    echo "a é igual a b";
} else {
    echo "a é menor que b";
}
```

```php
$x = 0;
switch ($x) {
    case '0':
        print "x é ZERO";
        break;
    case '2':
        print "x é DOIS"
        break;
    default:
		    print "x é diferente de ZERO e DOIS"
}

```

### Loops

```php
// loop while
$i = 1;

while($i <= 5){
		echo $i++; # >> 12345
}

// do while (O loop é execultado ao menos uma vez se a condição não for atendida)
$x = 1;

do {
		echo $x++; # >> 1
} while ($x <= 1);
```

```php
// loop for

// Loop for, repete o código cinco vezes
for ($i = 0; $i < 5; $i++) {
    echo $i;  // Exibe o valor de $i (0 a 4)
}
```

### Tratamento de Exceções

```php
try {
    // Código que pode gerar uma exceção
} catch (Exception $e) {
    // Executado se ocorrer uma exceção
    echo "Erro: " . $e->getMessage();
}
```

Para mais tópicos e referências, consulte a [cheatsheet do PHP](https://cheatsheets.zip/php).
