#new #new/tags #new/pkm #review #sumario
# 1 Introdução

## 1.1 Material

Segue o link do [github Daniel Reis](https://github.com/danielhe4rt). 

Acesse o repositório [php4noobs](https://github.com/danielhe4rt/php4noobs) para acompanhar as aulas. 

O guia introdutório consta no link da udemy [PHP4Noobs - Guia Introdutório para o PHP](https://www.udemy.com/course/php4noobs/).

## 1.2 Sejam bem vindos ao curso de PHP da He4rt Developers.

Ficamos muito felizes de você ter chegado até aqui no nosso curso! Estaremos trabalhando nos próximos passos para que você saia desse curso entendendo o básico para começar a programar na linguagem PHP.

PHP, que foi criada em 1994 por **Rasmus Lerdof**, é uma das linguagens mais utilizadas quando se trata de back-end por conta disso ainda existe uma ótima demanda no mercado de trabalho. Em nosso curso mostraremos as melhores formas para criar micro aplicações (server) que servirão o browser (cliente).

## 1.3 Comunicação

Como iremos inicialmente usar o Github para hospedar o curso, gostariamos de pedir para qualquer dúvida referente à alguma aula ou melhorias, que você crie um **ISSUE** no nosso repositório, para que assim consigamos resolver e manter uma padronização de perguntas/respostas dentro do nosso projeto.

# 2 Editores e Plugins

Como a abordagem do curso será a parte básica do PHP, não será necessário o uso de uma IDE robusta, então utilizaremos o editor de texto VSCode para realizarmos os nossos códigos, existem outras opções como SublimeText, Brackets e etc. Então fique à vontade para utilizar o editor que se sentir mais confortável e realizar os códigos que serão apresentados ao longo do curso.

## 2.1 Editor Visual Studio Code

Vamos começar a equipar nosso editor de texto com o que achamos ser necessário pra ajudar no desenvolvimento ágil com o PHP. Lembrando que esses plugins **NÃO** impactam no desenvolvimento em si, apenas facilitará pro código ser lido e entendido por você.

### 2.1.1 Plugin PHP IntelliSense

O IntelliSense provê uma leitura precisa das classes/funções com seus parâmetros e lhe dá uma melhor visão do que é preciso pra ser chamado, com isso, é possível visualizar uma "documentação" da função sem precisar recorrer à um manual para auxiliar.

### 2.1.2 Plugin PHP

Quando estamos no periodo de aprendizado, não sabemos qual é o padrão ou "jeito" certo de deixar o que escrevemos. E sim, existe uma forma correta, o documento referenciando estas informações pode ser encontrado clicando [aqui](https://github.com/danielhe4rt/php4noobs/blob/master/2-Ambiente/1-Editores-e-plugins.md#), porém, enquanto não chegamos nesse ponto iremos usar um formatador de códigos já existente para auxiliar no desenvolvimento.

# 3 Ambiente

Seguem as configurações dos ambientes Windows, Linux e MacOS com a devida instalação dos editores e variável de ambiente
## 3.1 Ambiente Windows

Para o windows vamos usar o servidor web embutido do PHP, que pode ser usado para o desenvolvimento e testes/estudos.

- Baixe os arquivos zipados da última versão (Thread Safe) do PHP no link: [https://windows.php.net/download](https://windows.php.net/download);
- Descompacte os arquivos que você baixou dentro da pasta `C:\Program Files`;
- Renomeie a pasta que você descompactou para `php`;
- Edite as variáveis de ambiente do Windows;
    - No menu iniciar pesquise por “Exibir configurações avançadas do sistema” abra o utilitário;
    - Na guia “Avançado” clique em “Variáveis de Ambiente“;
    - Em variáveis sistema escolha a opção “Path” e clique em editar;
    - Na nova janela “Editar variável de ambiente” clique no botão novo informe o caminho onde está o PHP “C:\Program Files\php”;
    - Clique no botão “OK”.
- Abra o CMD/Terminal do Windows e digite `php -v`, você verá a versão do PHP instalado no seu Windows.

### 3.1.1 Exemplo - Iniciando o servidor web

- Abra um CMD na pasta que contém seus códigos;
- Digite `php -S localhost:8000`;
- Acesse seu navegador de internet e digite o endereço: `http://localhost:8000`;
- Pronto, seu código está sendo executado no servidor embutido do PHP.

Para mais informações sobre o servidor embutido do PHP consulte o link abaixo:

[Commandline webserver php](https://www.php.net/manual/pt_BR/features.commandline.webserver.php)

## 3.2 Ambiente Linux

Nosso ambiente de desenvolvimento nas distribuições Linux será bem simples de se instalar (Linux tem dessas né).

Vamos instalar o PHP com alguns módulos para ajudar no desenvolvimento posteriormente.

Pra instalar tudo de uma vez, basta rodar o comando abaixo:

- Debian, Ubuntu e distribuições derivadas(apt):

```prompt
sudo apt install php php-mysql php-zip php-curl 
```

- Arch Linux, Manjaro e distribuições derivadas(pacman):

```prompt
sudo pacman -S php
```

após a instalação no arquivo `/etc/php/php.ini` mude a linha `;extension=mysqli` para `extension=mysqli`.

Caso sua distribuição não seja baseada no Debian (apt) você deve usar o gerenciador de pacotes apropriado para a sua distribuição (yum, pacman, zypper, ...).

Após finalizar com sucesso a instalação do PHP e dos módulos, você pode conferir a versão instalada rodando o comando abaixo:

```prompt
$ php -v
```

O retorno do comando acima deve exibir algo parecido com:

```prompt
PHP 8.2.1 (cli) (built: Jan 13 2023 10:43:08) (NTS)
Copyright (c) The PHP Group
Zend Engine v4.2.1, Copyright (c) Zend Technologies
    with Zend OPcache v8.2.1, Copyright (c), by Zend Technologies
```

Para verificar os módulos instalados, basta rodar o comando abaixo:

```prompt
$ php -m
```

Para identificar os arquivos de configuração do PHP (php.ini), basta rodar o comando abaixo:

```prompt
$ php --ini
```

## 3.3 Ambiente MacOS

Para o ambiente MacOS, utilizaremos uma ferramenta chamada Homebrew para instalar o PHP.

Homebrew é um gerenciador de pacotes open-source que simplificaa instalação de uma grande variedade de softwares no ambiente MacOS e Linux.

Nota: As versões mais recentes do MacOS já vêm com o PHP pré-instalado, porém é sempre uma boa idéia atualizá-lo.

### 3.3.1 Passo a passo

- Instale o Homebrew executando o seguinte comando em seu terminal (para mais informações: [https://brew.sh/](https://brew.sh/)):
    
    ```prompt
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
    
- Caso o passo anterior for executado com sucesso, poderá executar o comando:
    
    ```prompt
    $ brew -v
    
    # Resultado esperado
    Homebrew 2.7.5 # Ou qualquer outra versão
    ```
    
- Se desejar instalar a versão do PHP mais recente suportada pelo homebrew, basta executar o seguinte comando:
    
    ```prompt
    # Para installar a versão mais recente
    $ brew install php
    ```
    
- Caso deseje installar uma versão específica, pode pesquisar por todas as versões disponíveis no homebrew:
    
    ```prompt
    $ brew search php
    
    # Resultado
    php@7.2    php@7.3   php@7.4    php...
    
    
    # Instalar versão desejada
    $ brew install php@7.2
    ```
    
- Se todos os passos anteriores foram executados com sucesso, o PHP já está instalado em sua máquina. Para testá-lo, pode executar o seguinte comando no seu terminal:
    
    ```prompt
    $ php -v
    
    # Resultado esperado:
    PHP 8.0.1 (cli) (built: Jan  8 2021 12:35:09) ( NTS )
    Copyright (c) The PHP Group
    Zend Engine v4.0.1, Copyright (c) Zend Technologies
      with Zend OPcache v8.0.1, Copyright (c), by Zend Technologies
    ```
    

Para mais informações sobre como instalar o PHP utilizando homebrew no MacOS:

[https://formulae.brew.sh/formula/php](https://formulae.brew.sh/formula/php)

# 4 Dicas Gerais

Aqui está uma lista de dicas que não necessariamente serão usadas no desenvolvimento com PHP mas contribuem para melhor aprendizado como desenvolvedor.

- Para cada **Error**, **Warning**, **Fatal** ou qualquer bug que apareça no seu console/tela e você não tiver uma solução aparente, é aconselhável que você copie a saída/erro e busque no Google pois outras pessoas claramente já passaram pelo mesmo problema e já pediram ajuda em algum fórum como o **StackOverflow**
    
- Aprenda a pesquisar dúvidas no site **StackOverflow** pois ele é de longe o melhor amigo de qualquer desenvolvedor, seja o mais iniciante até o mais sênior.

# 5 Sintaxe

Como em toda línguagem/idioma, nós temos que entender e compreender como ela é escrita e isso se refere diretamente à gramática e suas regras. Na programação, temos também um conjunto de regras para que algo consiga ser lido e interpretado tanto pelo computador, quanto pela pessoa que estará lendo seu código.

Código é feito de símbolos e caracteres, isso é chamado de sintaxe e neste momento iremos entender as **regras** que devem ser seguidas para você programar no PHP.

## 5.1 Pontuação

Pontuação é algo obrigatório para escrita de textos formais, independente da língua que você estiver praticando e na programação ela também tem um papel fundamental.

Entenda que você estará trabalhando com uma línguagem, (como se fosse português ou inglês) e em ambas a pontuação deve ser respeitada para uma fácil interpretação.

O PHP tem um interpretador que irá checar cada linha escrita com essas pontuações e caso você não siga essa regra de sintaxe, ele irá te retornar uma mensagem de erro indicando a linha e o tipo de "erro gramatical" que você cometeu.

PS: Busque por esse erro no Google pra um melhor resultado.

## 5.2 Ponto e vírgula

Ponto e vírgula é a declaração que uma linha de código foi finalizada no PHP.

Declarações de código em PHP **devem** acabar com ponto e vírgula **(;)** pois é exatamente esse caractere que indica pro interpretador que essa linha de código terminou.

Declarações de código que não terminarem com ; indicam pro interpretador continuar para a próxima linha e caso a linha anterior **não tenha ;** ele emite um erro de sintaxe, também conhecido como **parse error**.

Exemplo Funcionais:

```php
echo "Eu sou um desenvolvedor do coração";

echo "He4rtDevs é o " . "melhor grupo <3";
```

Exemplos não funcionais:

```php
echo "Eu sou um desenvolvedor do coração"
```

```php
echo "He4rtDevs é o " .
     "melhor grupo <3"
```

No segundo exemplo incorreto, usamos um operador de concatenação (.), que serve para "juntar" strings, porém vimos que faltou o ponto e vírgula e isso irá jogar uma exception (excessão) para o usuário assim que essa linha for executada.

## 5.3 Tags do PHP

Para que um script seja executado no PHP, primeiro ele deve identificar se há uma tag de abertura de script

```php
<?php
```

... até encontrar a linha de finalização de código

```php
?>
```

... onde o interpretador identifica que o bloco de código foi finalizado.

Caso você apenas queira imprimir algum dado, dá pra usar a "tag de echo" com alguma variável ou informação que você queira.

```php
<?= "He4rtDevs" ?>
```

Todos os comandos **devem** ser encapsulados por alguma tag de abertura e fechamento do PHP ou ele irá jogar uma exception (excessão) para o usuário.

Se o arquivo a ser lido tiver apenas um script em PHP, ele não necessita da tag de finalização **?>** e em algumas situações, não fechar a tag é considerado boa prática

# 6 Funções de Saída

Após o nosso ambiente montado e configurado com todas as ferramentas necessárias, iremos começar a ver algum código na prática.  
Como iremos usar o nosso console em boa parte do curso, precisaremos de algumas funções para nos auxiliar a visualizar qualquer saída de dados do nosso código. E nessa lição, iremos conhecer essas funções.

### 6.1 Função *echo()*

[Referencia para documentação](https://www.php.net/manual/pt_BR/function.echo.php)

Descrição: Exibe uma ou mais strings e não tem nenhum retorno.  

Quando nós fizermos qualquer tipo de código, precisaremos entender se ele funcionou ou não. Enquanto não chegamos num nível mais profissional com a ferramenta, a função **echo** será nossa melhor amiga para fazer debugging do nosso código.

Veja este primeiro exemplo:

```php
<?php

echo "He4rtDevs";
echo 123456;
```

Vamos executar o arquivo acima para vermos qual é a saída utilizando o comando abaixo:  

```shell
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php saida1.php
He4rtDevs123456
```

### 6.2 Função *var_dump()*

[Referência para documentação](https://www.php.net/manual/pt_BR/function.var-dump)

Descrição: coleta informações sobre a variável inserida.  
  

Como vamos precisar entender que tipo de dados são passados por variáveis e muitas vezes por referência de outras classes, vamos usar bastante a função **var_dump** para entender o que se passa naquele respectivo ambiente. Agora vamos ver um exemplo:

```php
<?php

var_dump("Olá");
var_dump(123);
var_dump(new stdClass());
```

_Arquivo encontrado em: exemplos/saida2.php_

Vamos executar o arquivo acima para vermos qual é a saída utilizando o comando abaixo:  

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php saida2.php
string(4) "Olá"
int(123)
object(stdClass)#1 (0) {
}
```

Podemos ver que ele nos retornou alguns dados sobre o que inserimos dentro da função **var_dump()** e ele descreveu coisas que se fossem passados por referência, não seriam tão óbvias.

# 7 Comentários

Iremos usar um sistema muito interessante para poder nos guiar enquanto programamos. **Comentários** é um dos princípios de qualquer programadeiro que não quer criar algo e esquecer no dia seguinte.

Os comentários não são interpretados quando o código está sendo lido, então você pode usar e abusar dos mesmos pra documentar tudo que você achar necessário. Observe que nem sempre comentar códigos é bom, mas isso é assunto pra outro momento.

Existem duas formas de comentar no PHP, vamos conhecer as duas e entender quando usar cada uma delas.

## 7.1 Comentário de linha única

Os comentários de linha única são iniciados com duas barras " **//** " no nosso querido PHP. Veja o exemplo abaixo:

```php
<?php
// Este é um comentário muito foda q vai explicar tudo abaixo
// Mentira nem vai nada não
echo "He4rtDevs <3";
// Será que isso vai ser interpretado?
// To com fome
```

Os comentários de linha única são iniciados com duas barras " **//** " no nosso querido PHP. Veja o exemplo abaixo:

Você pode executar o exemplo acima com o seguinte comando:  

```shell
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php comentarios1.php
He4rtDevs <3
```

Como podemos observar, não foi mostrado nada fora do esperado. Os comentários são totalmente anulados na hora de qualquer tipo de processamento e só serve de fato para leitura do desenvolvedor.

## 7.2 Comentário de múltiplas linhas

Para comentar múltiplas linhas, é usado um padrão um pouco diferente do que é acostumado.

- Inicia a linha com **/****
- Para cada nova linha é inserido um novo asterisco *****
- Para fechar o comentário é inserido ***/**

Veja o exemplo abaixo:

```php
<?php
/**
 * Script para visualização de comentarios
 * e mostrar o nome do melhor grupo de devs do mundo
 *
 * @author danielhe4rt - hey@danielheart.dev // Opcional
 * @return void // Opcional
 */

echo "He4rtDevs <3";
```

Podemos ver o resultado novamente na execução abaixo onde não é lido nenhum tipo de comentário.

```shell
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php comentarios2.php
He4rtDevs <3
```

# 8 Tipos de dados

Programação é uma constante troca de dados entre a memória e o processador, onde a memória PRECISA saber o que está sendo enviado para reservar espaço, armazenar e enviar ao processador para interpretar o código. Conhecer os tipos de dados padrões vai ajudar você a entender um conceito muito básico da programação de baixo nível (não muito bem aplicada em PHP, masss...): a tipagem.  

Por que você deveria perder tempo com isso já que o PHP não te obriga a fazer essa parte de tipagem?  
Os tipos de dados são MUITO importantes para que sua aplicação não quebre por um erro bobo onde você "deveria tá mandando um número inteiro em vez de um flutuante".  

Vamos entender os tipos escalares do PHP:

## 8.1 Booleanos (*boolean*)

Este é o tipo mais simples. Um booleano expressa um valor de verdade. Ele pode ser **TRUE** ou **FALSE** e são valores [_case-insensitives_.](https://pt.wikipedia.org/wiki/Case-sensitive)  
Vamos usar a função de saida **var_dump()** para entender um pouco de como é interpretado o dado **boolean** no código abaixo:

```php
<?php
var_dump(True);
var_dump(False);
var_dump(true);
var_dump(false);
var_dump(TrUe);
var_dump(fAlSe);
```

Você pode executar o exemplo acima com o seguinte comando:  

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos0.php
bool(true)
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)
```

## 8.2 Inteiros (*integer*)

Um inteiro é um número do conjunto Z = {..., -2, -1, 0, 1, 2, ...}.  
Inteiros podem ser especificados em notação decimal (base 10), hexadecimal (base 16), octal (base 8) ou binária (base 2), opcionalmente precedido de sinal (- ou +).

```php
<?php
echo "Exemplos de números inteiros \n";
var_dump(1234); // número decimal
var_dump(-123); // um número negativo
var_dump(0123); // número octal (equivalente a 83 em decimal)
var_dump(0x1A); // número hexadecimal (equivalente a 26 em decimal)
var_dump(0b11111111); // número binário (equivalente ao 255 decimal)
```

Você pode executar o exemplo acima com o comando abaixo:  

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos1.php
Exemplos de números inteiros
int(1234)
int(-123)
int(83)
int(26)
int(255)
```

## 8.3 Flutuantes (*float*)

Números de ponto flutuante (também conhecidos como "floats", "doubles" ou "números reais"), podem ser especificados utilizando qualquer uma das seguintes sintaxes:

```php
<?php

$a = 1.234;
$b = 1.2e3;
$c = 7E-10;

echo $a . "\n";
echo $b . "\n";
echo $c . "\n";
```

Você pode executar o exemplo acima com o seguinte comando:  

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos2.php
1.234
1200
7.0E-10
```

## 8.4 *String*

Uma string é uma série de caracteres, onde 1 caractere é o mesmo que 1 byte para armazenamento na memória. Isso significa que o PHP possui suporte a um conjunto de apenas 256 caracteres, e, portanto, não possui suporte nativo a Unicode. Veja mais detalhes do tipo string:

Uma string é um conjunto de caracteres, formando uma frase e/ou palavra ou até mesmo um caractere único.

Uma string pode ser especificada de quatro formas diferentes, porém só iremos usar duas. Sendo elas com:

- Aspas Simples;
- Aspas Duplas.

Nós já passamos por uma string nos exemplos anteriores de output com **echo** então vai ser mais fácil o entendimento. Segue o exemplo abaixo:

```php
<?php

echo "He4rtDevs <3";
echo "Melhor grupo do mundo para devs iniciantes";
```

Vamos analisar o exemplo abaixo:

```shell
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos3.php
He4rtDevs <3Melhor grupo do mundo para devs iniciantes
```

Podemos ver que a linha não foi quebrada e isso não irá acontecer se você não usar uma sequência de escape, na qual já apareceu em um exemplo nesta sessão. A sequência **\n** significa que a partir deste ponto será uma nova linha no nosso console e pode ser colocado em qualquer parte da string. Segue o exemplo abaixo:

```php
<?php

echo "He4rtDevs <3\n";
echo "Melhor grupo do mundo para devs iniciantes";
```

OU

```php
<?php

echo "He4rtDevs <3";
echo "\n";
echo "Melhor grupo do mundo para devs iniciantes";
```

Vamos ver o resultado, onde é esperado que seja quebrada a linha e separado o conteúdo das strings.

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos4.php
He4rtDevs <3
Melhor grupo do mundo para devs iniciantes
```

Com essa base você já consegue fazer vários exemplos com strings e sempre tendo uma saída com uma fácil legibilidade.

## 8.5 *Arrays* (vetores)

Um array no PHP é na verdade um mapa ordenado. Um mapa é um tipo que relaciona valores à chaves. Este tipo é otimizado para vários usos diferentes: ele pode ser tratado como um array, uma lista (vetor), hashtable (que é uma implementação de mapa), dicionário, coleção, pilha, fila e provavelmente mais. Assim como existe a possibilidade dos valores do array serem outros arrays, árvores e arrays multidimensionais.

Um array pode ser criado com o construtor de linguagem **array()** ou por `[]`. Ele leva qualquer quantidade de pares separados por vírgula chave => valor como argumentos.

```php
array(
    chave  => valor,
    chave2 => valor2,
    chave3 => valor3,
    ...
)
```

Caso você não queira uma "chave", ele utilizará o mapa incremental padrão de vetores, começando pelo 0,1,2,3... Veja os exemplos abaixo:

```php
<?php

$array1 = array(
    "dev" => "danielhe4rt",
    "group" => "he4rtdevs"
);

// Ou se você quiser um jeito mais simples de instanciar um array:

$array2 = [
    "dev" => "danielhe4rt",
    "group" => "he4rtdevs"
];

var_dump($array1);
var_dump($array2);
```

Vejamos o resultado abaixo:

```shell
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos5.php
array(2) {
  ["dev"]=>
  string(11) "danielhe4rt"
  ["group"]=>
  string(9) "he4rtdevs"
}
array(2) {
  ["dev"]=>
  string(11) "danielhe4rt"
  ["group"]=>
  string(9) "he4rtdevs"
}
```

Mostramos dois jeitos de declarar arrays e os dois estão **certos**, porém usando `[]` é um jeito mais simples de expressar um array.

Agora vamos para outro exemplo de como ficaria se você não colocasse chaves nos seus arrays:

```php
<?php

$array1 = array(
    "danielhe4rt",
    "he4rtdevs"
);

// Ou se você quiser um jeito mais simples de instanciar um array:

$array2 = [
    "danielhe4rt",
    "he4rtdevs"
];

var_dump($array1);
var_dump($array2);
```

Testando a saída:

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos6.php
array(2) {
  [0]=>
  string(11) "danielhe4rt"
  [1]=>
  string(9) "he4rtdevs"
}
array(2) {
  [0]=>
  string(11) "danielhe4rt"
  [1]=>
  string(9) "he4rtdevs"
}
```

Vamos comparar o resultado abaixo com o nosso último teste acima e anotar algumas diferenças:

- No primeiro usamos chaves como string
- No segundo usamos chaves incrementais padrões de um array

Ao colocar um dado dentro de um array sem uma chave, ele automaticamente atribui o primeiro valor incremental, sendo ele iniciado **sempre** do 0.

Agora vamos entender como mostrar a saída de um vetor. Vamos declarar dois vetores e trabalhar com eles:

```php
<?php

$array1 = [
    'dev' => 'danielhe4rt',
    'group' => 'he4rtdevs'
];

$array2 = [
    'danielhe4rt',
    'he4rtdevs'
];

// Array associativo
echo $array1['dev'] . "\n";
echo $array1['group'] . "\n";

// Array não associativo
echo $array2[0] . "\n";
echo $array2[1] . "\n";
```

Saída:

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php tipos7.php
danielhe4rt
he4rtdevs
danielhe4rt
he4rtdevs
```

Com isso podemos entender que é possível acessar tanto com a posição do nosso vetor quanto a uma chave específica atribuída.

# 9 Variáveis

Pra começar, todos sabemos que para guardar informação as linguagens de programação utilizam variáveis certo? na maioria das linguagens você precisa especificar o tipo de variável antes de declara-lá, PHP é diferente.

No PHP existe a "tipagem dinâmica", onde você pode criar a variável sem precisar declarar seu tipo(float, string, int) e também você pode alterar o tipo de variável enquanto o programa roda, não importando o tipo anterior. Antes de alguns exemplos, vamos determinar algumas regras para nomeação de variáveis.

- Toda variável no PHP é declarada por **$** e em seguida o nome da variável;
- O jeito correto e válido para declarar o nome de uma variável no PHP é iniciar por sublinhado (também chamado de underscore) ou letra, seguido de qualquer letra, números ou sublinhados;
- As variáveis no PHP são [_case-sensitives_](https://pt.wikipedia.org/wiki/Case-sensitive), então, $He4rt não é o mesmo que $he4rt;
- O $this é uma variável que não pode ser atribuída, você irá entender o que significa $this nos próximos módulos do curso;
- Você pode juntar duas variáveis, strings ou qualquer tipo com a concatenação, que é usado o sinal ( . ) entre os elementos (exemplo abaixo).

Lembrando que para atribuirmos um valor à uma variável passamos o sinal de ( = ) e o seu valor.

```php
<?php
//Mostrando o case sensitive
$He4rt = 'Eu ';
$he4rt = 'amo ';
$he4rT = 'a He4rt ';
$HE4RT = 'Developers';
echo $He4rt . $he4rt . $he4rT . $HE4RT;
?>
```

Saída:

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php variaveis1.php
Eu amo a He4rt Developers
```

### 9.1 Observações sobre variáveis

- Como vocês podem ver, o PHP por possuir [_case-sensitive_](https://pt.wikipedia.org/wiki/Case-sensitive), as variáveis `$He4rt`,`$he4rt`,`$he4rT` e `$HE4RT` não são a mesma coisa;
- É preciso sempre utilizar ponto e vírgula no final de cada declaração ( ; ), se porventura você esquecer, irá dar erro;
- Lembrando que é sempre bom se antenar as boas práticas, use variáveis que façam sentido com o código escrito, não utilize nomes como $a, $b, $c e se torne um programador alfabético.

Como foi explicado antes, variáveis podem mudar o valor no tempo de execução, ou seja, durante a execução do código. Vamos para mais um exemplo:

```php
<?php
$idade = '18 Anos';
echo "Me chamo João e tenho " .$idade . "\n";
$idade = '19 Anos';
echo "Porém fiz aniversário e agora tenho " .$idade;
?>
```

Saída:

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php variaveis2.php
Me chamo João e tenho 18 Anos
Porém fiz aniversário e agora tenho 19 Anos
```

# 10 Operadores Aritméticos

Quando falamos de linguagens de programação, podemos esperar que existam os operadores aritméticos como em todas as outras linguagens. Vamos conhecer quais são eles:

- Adição `+`
- Subtração `-`
- Multiplicação `*`
- Divisão `/`
- Módulo (resto de uma divisão) `%`

## 10.1 Adição

Realiza a soma de duas ou mais variáveis.

```php
<?php

$a = 10; //a = 10
$b = 20; //b = 20
$soma = $a + $b; //Realizando a soma com sinal de + das variáveis $a e $b
echo $soma . "\n";
```

Saída

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php operadoresA2.php
30
```
## 10.2 Subtração

Realiza a subtração de duas ou mais variáveis.

```php
$a = 100; //a = 100
$b = 50; //b = 50

$subtracao = $a - $b; //Realizando a subtração com sinal de - das variáveis $a e $b

echo $subtracao . "\n";
```

Saída:

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php operadoresA3.php
50
```
## 10.3 Multiplicação

Multiplica duas ou mais variáveis.

```php
$a = 500; //a = 500
$b = 50; // b = 50

$multiplicacao = $a * $b; // Realizando a multiplicação com sinal de * das variáveis $a e $b

echo $multiplicacao . "\n";
```

Saída

```prompt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/3-Basico/exemplos$ php operadoresA4.php
25000
```

## 10.4 Divisão

Divide duas ou mais variáveis.

```php
$a = 100; //a = 100
$b = 2; // b = 2

$divisao = $a / $b; // Realizando a divisão com sinal de / das variáveis $a e $b

echo $divisao;
```

Saída

```txt
50
```

## 10.5 Módulo

O operador `%` Retorna o resto de uma divisão.

```html
$a = 3; //a = 3
$b = 2; // b = 2

$resto = $a % $b; // Irá efetuar a divisão de $a por $b e depois retornar o resto da divisão

echo $resto;
```

Saída

```txt
1
```

# 11 Considerações sobre Expressões

No PHP também é possível fazer diversas operações matemáticas na mesma linha(como uma expressão), veja exemplos abaixo.

## 11.1 Expressão com parênteses para priorizar operações

```php
//Exemplo em que utilizamos várias operações matemáticas na mesma linha
echo (50 + 10 - 30) * (5.2 / 2);
/*
Como podem ver, a expressão acima contém parênteses, significa qual expressão será executada primeiro.
A primeira expressão resulta em 30 pois é efetuada a soma de 50 + 10 e depois a subtração de - 30.
O resultado de 30 será multiplicado pela segunda expressão ( divisão de 5.2 / 2 ) que é igual a (2.6).
30 * 2.6 = 78, que será nosso resultado.
*/
```

Resultado

```txt
78
```
## 11.2 Expressão sem parênteses com prioridade esquerda-direita

```php 
//Veja o que acontece quando utilizamos varias operações matemáticas sem parênteses:
echo 50 + 10 - 30 * 5.2 / 2;
//Prioridade de operações na direção da esquerda para a direita priorizando potência, multiplicação ou divisão e depois subtração ou soma na ordem em que aparecerem
```

Resultado
```txt
-18
```
## 11.3 Expressão com variáveis criadas em saída *echo()*

```php
//É possivel também criar variáveis dentro de parênteses e fazer operações com a mesma.
$a = 2;
echo $a * ($b = 3 );
```

Resultado
```txt
6
```

## 11.4 Operador subtração em variáveis

O operador subtração `-`, antes de uma varíavel ou número transforma o número ou variável para o oposto, se for negativo vira positivo, se for positivo vira negativo.

```php
<?php
$num1 = 77; //Variável num igual a 77 positivo
$num2 = -$num1; //Variável num2 vai ser igual ao oposto de num(77), ou seja, 77 negativo

echo $num1 . "\n";
echo $num2 . "\n";
```

## 11.5 Potência: base e expoente

O operador exponencial `**`, retorna o resultado de uma variável elevada a outra, implementada a partir do PHP 5.6.

```php
$a = 10; // a = 5
$b = 2; // b = 5

$exponencial = $a ** $b; //Aqui fazemos que a variável $a = 10 seja elevada a $b = 2, ou seja, 10x10 = 100

echo $exponencial;

```

## 11.6 Precedência dos operadores aritméticos em php

Na ordem da esquerda para a direita 
`**` potenciação 
`*`, `/` multiplicação ou divisão na ordem em aparecerem
`%` módulo (resto)
`+`, `-` soma ou subtração na ordem em que aparecerem

Supondo que temos a expressão 
`a ** b + (a + a1 / b * c % d)`
Primeiro será efetuada a potenciação (`**`), a divisão (`/`), depois a multiplicação (`*`), depois o módulo (`%`) e depois o restante (`+-`)

# 12 Operadores Bitwise (bit a bit)

Operadores Bitwise permitem a avaliação e modificação de bits específicos em um tipo inteiro.

- E `&`
- OU `|`
- OU exclusivo `^`
- Não `~`
- Deslocar à esquerda `<<`
- Deslocar à direita `>>`

Os operadores bitwise: `&` , `|` , `^` comparam dois valores inteiros utilizando suas representações binárias, e retornam um novo valor. Cada bit será comparado e a formação desse novo valor depende do operador que você usar.

## 12.1 Operador E "&"

Retorna `1` **se ambos** os bits comparados forem iguais a `1`, caso contrário, retorna `0`.

```php
<?php

echo 9 & 7;

// 9 em binário é: 00001001
// 7 em binário é: 00000111
// resultado:      00000001

//Retorna: "1" que é o binário 00000001 
```

## 12.2 Operador OU "|"

Retorna `1` **se um dos** bits comparados for igual a `1`, caso contrário, retorna `0`.

```php
<?php

echo 9 | 7;

// 9 em binário é: 00001001
// 7 em binário é: 00000111
// resultado:      00001111

//Retorna: "15" que é o binário 00001111 
```

## 12.3 Operador OU exclusivo "^"

Retorna `1` **se ambos os** bits comparados forem diferentes, caso contrário, retorna `0`.

```php
<?php

echo 9 ^ 7;

// 9 em binário é: 00001001
// 7 em binário é: 00000111
// resultado:      00001110

//Retorna: "14" que é o binário 00001110 
```

## 12.4 Operador Não "~"

Tem a função de `Inverter bits`. O bit que era 0 se torna 1; e o bit que era 1 se torna 0.

```php
<?php

$a = -9;
$a = ~$a;

echo $a;

//diferente dos outros exemplos aqui representamos o valor com 20 bits
// -9 em binário é:                 11111111111111110111
// após a operação o é resultado:   00000000000000001000

//Retorna: "8" que é o binário 00000000000000001000
```

## 12.5 Operador deslocar à esquerda <<

Desloca os bits de $a, $b passos para a esquerda (cada passo significa "multiplicar por dois"); Ou seja, `$a << 7`, é o mesmo que multiplicar `$a` por 2 `sete vezes`.

```php
<?php

$a = 9;
$b = 7;
echo $a << $b;

//Retorna: "1152" que é o resultado de 9*2*2*2*2*2*2*2
```

## 12.6 Operador Deslocar à direita `>>`

Desloca os bits de `$a, $b passos para a direita (cada passo significa "divide por dois")`; Ou seja, `$a << 7`, é o mesmo que dividir `$a` por 2 `sete vezes`.

```php
<?php

$a = 9;
$b = 7;
echo $a >> $b;

//Retorna: "0" que é o resultado de 9/2/2/2/2/2/2/2
//Se você fizer a operação acima na calculadora o resultado vai ser igual a 0.0703125
//o PHP retorna o valor inteiro nesta operação
```

## 12.7 Notas sobre bits

Bit é a menor unidade de informação na computação e pode ser 0 (zero) ou 1 (um), ligado ou desligado;

- Um byte tem 8 bits;
- Nao se preocupe com os operadores bit a bit por hora, basta que você conheça eles;

# 13 Operadores de atribuição

Uma abribuição é uma maneira de guardar um valor na memória e referenciá-lo com um identificador, por exemplo: uma variável ou uma constante.

## 13.1 Atribuição =

O operador básico de atribuição no PHP é =, **não pense nele como "igual a", pense como "recebe o valor de"**. Então `$a = 3;` significa que a variável `$a` recebe o valor `3`.

```php
<?php

$resultado = 10;

echo $resultado;

//Retorna: "10"
```

### 13.1.1 Formas abreviadas de atribuição

#### 13.1.1.1 Soma +=

```php
<?php

$resultado = 10;
$resultado +=10;

echo $resultado;

//Retorna: "20"
```

#### 13.1.1.2 Subtração -=

```php
<?php

$resultado = 10;
$resultado -=5;

echo $resultado;

//Retorna: "5"
```

#### 13.1.1.3 Multiplicação *=

```php
<?php

$resultado = 10;
$resultado *=10;

echo $resultado;

//Retorna: "100"
```

#### 13.1.1.4 Divisão /=

```php
<?php

$resultado = 10;
$resultado /=2;

echo $resultado;

//Retorna: "2"
```

#### 13.1.1.5 Módulo (retorna o resto da divisão) %=

```php
<?php

$resultado = 10;
$resultado %=2;

echo $resultado;

//Retorna: "0"
```

##  13.2 Operador de incremento ++ e decremento --

O PHP suporta operadores de incremento e decremento, a ordem do operador é importante aqui. Colocar um `++` antes de uma variável em um `echo` incrementa a variável em um `antes da avaliação`. Colocar o operador após a variável incrementa `após a avaliação`. A mesma regra serve para o operador de decremento `--`.

```php
<?php

$variavelInteira = 10;

echo 'O valor da variável foi incrementado e agora é  = ' . ++$variavelInteira . PHP_EOL;
echo 'O valor da variável foi incrementado, mas ainda não mudou então continua sendo = ' . $variavelInteira++ . PHP_EOL;
echo 'O valor da variável agora é  = ' . $variavelInteira . PHP_EOL;

/** -- Retorna
O valor da variável foi incrementado e agora é = 11
O valor da variável foi incrementado, mas ainda não mudou então continua sendo = 11
O valor da variável agora é = 12
**/
```

## 13.3 Notas sobre concatenação e quebra de linha

- Algumas linguagens usam o sinal `+`, para concatenar;
- Quando não precisar interpretar variáveis use aspas simples `''`, isso poupa processamento;
- `PHP_EOL` é uma constante do PHP que serve para quebrar linhas.

# 14 Comparação de Valores

O PHP suporta várias opções de comparação de valores, vamos aprender sobre elas agora mesmo. Mas antes de começar, entenda que:

- `true` significa verdadeiro e `false` é falso;
- Um `1` é a mesma coisa que `true`;
- Zero `0` é a mesma coisa que `false`;
- `PHP_EOL` é uma constante do PHP que serve para quebrar linhas.

Agora sim, vamos aos comparadores de valor no PHP.

## 14.1 Igualdade ==

O operador igual duplo == compara dois valores e retorna true, se forem iguais, e false se os valores forem diferentes.

```php
<?php

echo (0 == false) . PHP_EOL; //true
echo ('123' == 123) . PHP_EOL; //true
echo ('um' == 1) . PHP_EOL; //false
echo (123.0 == 123) . PHP_EOL; //true

/**
retorna: 1
         1
          
         1
**/
```

## 14.2 Diferença !=

Um ponto de exclamação `!` com um sinal de igual "=" e pronto, dá isso aqui `!=`. Com esse operador você pode testar se os valores são diferentes. Se os valores forem diferentes o retorno é `true`, se forem iguais o retorno é `false`

```php
<?php

echo (0 != false) . PHP_EOL; //false
echo ('123' != 123) . PHP_EOL; //false
echo ('um' != 1) . PHP_EOL; //true
echo (123.0 != 123) . PHP_EOL; //false

/**
retorna:  
          
         1
         
**/
```

## 14.3 Identico ===

O PHP também pode testar se um valor é igual e do mesmo [tipo](https://github.com/danielhe4rt/php4noobs/blob/master/3-Basico/3-Tipos-de-dados.md), você pode chamar isso de: "testar se o valor é idêntico".

```php
<?php

echo (0 === false) . PHP_EOL; //false
echo ('123' === 123) . PHP_EOL; //false
echo ('um' === 1) . PHP_EOL; //false
echo (123.0 === 123) . PHP_EOL; //false

//É tudo falso :(, por isso não retorna nada
```

## 14.4 Não identico !==

É possível testar também se o valor não é idêntico, basta usar o operador `!==`, chame isso de: "testar se o valor não é idêntico", e novamente o PHP vai verificar o [tipo](https://github.com/danielhe4rt/php4noobs/blob/master/3-Basico/3-Tipos-de-dados.md) do valor.

```php
<?php

echo (0 !== false) . PHP_EOL; //true
echo ('123' !== 123) . PHP_EOL; //true
echo ('um' !== 1) . PHP_EOL; //true
echo (123.0 !== 123) . PHP_EOL; //true

/**
retorna: 1 
         1
         1
         1
**/
```

## 14.5 Maior/menor que

O PHP suporta quatro operadores maiores/menores que:

- `<` menor que;
- `>` maior que;
- `<=` menor ou igual a;
- `>=` maior ou igual a.

```php
<?php

echo (2 < 3) . PHP_EOL; //true
echo (2 > 3) . PHP_EOL; //false
echo (2 <= 3) . PHP_EOL; //true
echo (2 >= 3) . PHP_EOL; //false

/**
retorna: 1 
         
         1
         
**/
```

## 14.6 Notas sobre comparação de valores

```txt
O PHP tenta converter os valores na comparação de igual duplo "==", e diferente !=;

Por isso que a string '123'' é igual == ao número 123 e o retorno é true, mas não é idêntica ===;

Na comparação de idênticos === o PHP não tenta converter os valores;

Por isso, quando você tenta comparar se a string '123' é idêntica === ao número 123, o retorno é false, ou seja, diferente.
```

# 15 Combinação/concatenação de strings

Concatenar significa **juntar as coisas**, no PHP existe um operador que faz isso, é o ponto `.` e é possível utilizar este operador de forma abreviada também, vamos aprender como ele funciona:

## 15.1 Só concatenando com `.`

```php
<?php

$euQuero = 'Eu quero ser um programador' . ' PHP';

echo $euQuero;

//Retorna: "Eu quero ser um programador PHP"
```

## 15.2 Concatenando de forma abreviada com `.=`

```php
<?php

$euQuero = 'Eu quero ser um programador';
$euQuero .= ' PHP';

echo $euQuero;

//Retorna: "Eu quero ser um programador PHP"
```

## 15.3 Concatenando variáveis `.`

```php
<?php

$euQuero = 'Eu quero ser um programador';
$php = ' PHP';

echo $euQuero . $php;

//Retorna: "Eu quero ser um programador PHP"
```

## 15.4 Notas sobre concatenação

- Algumas linguagens de programação usam o sinal `+`, pra concatenar;

# 16 Operadores de Arrays

O PHP manda muito bem quando se trata de processamento de arrays/matrizes. Existem muitas funções internas para auxiliar nisso. Vejamos os operadores que podemos usar ao fazer **operações com arrays:**

## 16.1 União `+`

Você pode unir um ou mais valores de arrays.

```php
<?php

$array1 = [0 => 'PHPBA', '1' => 'PHPSP', 2 => 'PHPSE'];
$array2 = [3 => 'he4rtdevs'];

print_r($array1 + $array2);

/**
Retorna:

Array
(
    [0] => PHPBA
    [1] => PHPSP
    [2] => PHPSE
    [3] => he4rtdevs
)
**/
```

## 16.2 Igualdade ==

```php
<?php

$array1 = [0 => 1];
$array2 = [0 => 1];

echo $array1 == $array2;

//Retorna: 1, significa que os valores dos arrays são iguais
```

## 16.3 Diferença `!=` ou `<>`

```php
<?php

$array1 = [0 => 1];
$array2 = [0 => 2];

echo $array1 != $array2;

//Retorna: 1, significa que os valores dos arrays são diferentes
```

## 16.4 Idêntico ===

```php
<?php

$array1 = [0 => 1];
$array2 = [0 => 1];

echo $array1 === $array2;

//Retorna: 1, significa que os valores dos arrays são iguais e do mesmo tipo (número inteiro)
```

## 16.5 Não idêntico `!==`

Verifica se valores dos arrays não são idênticos (valor e tipo do valor).

```php
<?php

$array1 = [0 => 1];
$array2 = [0 => '1'];

echo $array1 !== $array2;

//Retorna: 1, significa que os valores dos arrays não são iguais e/ou não são do mesmo tipo (número inteiro)
```

## 16.6 Notas sobre operadores de arrays

- No PHP, o índice de um array começa a partir de zero `0`;
- Um retorno zero significa falso;
- Arrays e matrizes são a mesma coisa;
- A função `print_r()` é muito útil para testar arrays;

# 17 Operadores lógicos

Operadores lógicos operam com valores [booleanos](https://github.com/danielhe4rt/php4noobs/blob/master/3-Basico/3-Tipos-de-dados.md). Por isso, eles convertem valores para um **Booleano** antes de tentar a operação.

## 17.1 E && and

Verdadeiro `true`, se ambos os operandos (valores a serem testados), forem verdadeiros.

```php
<?php

$a = true;
$b = true;

var_dump($a && $b);

//Retorna: bool(true)
```

## 17.2 OU `or`, `||`

Este operador lógico é conhecido como: **OU Inclusivo**, e vai retornar `true` se um dos operandos for verdadeiro, ou ambos.

```php
<?php

$a = false;
$b = true;

var_dump($a || $b);

//Retorna: bool(true)
```

## 17.3 XOR `^`, `xor`

Este operador lógico é conhecido como: **OU Exclusivo**, e vai retornar `true` se um dos operandos for verdadeiro, **mas não ambos**.

```php
<?php

$a = true;
$b = true;

var_dump($a ^ $b);

//Retorna: int(0) zero, ou seja, falso, pois ambos os operandos é verdadeiro;
```

```php
<?php

$a = true;
$b = false;

var_dump($a ^ $b);

//Retorna: int(1), ou seja, true, pois apenas um dos operandos é verdadeiro;
```

## 17.4 NÃO `!`, `not`

É um operador de negação.

```php
<?php

$a = true;

var_dump(!$a);

//Retorna: bool(false), aqui negamos uma variável verdadeira e ela se tornou falsa.
```

## 17.5 Notas sobre operadores lógicos

Os símbolos `&&`, `||` e `^` têm maior ordem de precedência, e são avaliados primeiro que `and`, `or`, e `xor`. Na prática eles fazem a mesma coisa, mas os símbolos sempre vão ser avaliados primeiro nas expressões, evite mistura-los.

- Nos exemplos deste tópico usamos a função `var_dump()` 
- Lembre-se que: `0` é `false` (falso) e `1` é `true` (verdadeiro).

# 18 Operador de Execução

Os backticks ` `` `, também conhecidos como _backquotes_, executam o conteúdo como um comando shell e são equivalentes a `shell_exec()`. `exec()`, `shell_exec()` e `system()`, todos são capazes de executar comandos no nível do shell.

```php
<?php

$output = `ls -al`;
echo "<pre>$output</pre>";
```

Um **comando shell** é uma ou mais palavras que representam uma instrução enviada pelo usuário e seus programas para o kernel através de um interpretador de comandos.

# 19 Estruturas de Controle

Estruturas de controle remetem a decisões de um trecho de código que deverá ser executado baseado em um teste lógico. Para verificar se a resposta é **VERDADEIRA** ou **FALSA**, você precisará usar alguma das estruturas de controle de decisão.

Vamos exemplificar com [pseudocódigo](https://pt.wikipedia.org/wiki/Pseudoc%C3%B3digo):

```txt
- Vá até o seu portão.
- Tente trancar o portão.
- Se você tiver a CHAVE, faça:
    - Tranque Portão.
- Se NÃO:
    - Busque a chave;
    - Volte ao portão;
    - Tranque o portão.
```

```txt
- Ligue o interruptor.
- Se a LÂMPADA NÃO acender, faça:
    - Procure uma lâmpada nova;
    - Remova a lâmpada queimada;
    - Insira a nova lâmpada.
```

Foram dados exemplos de como funcionariam estruturas de condições, agora vamos analisar cada uma delas.

## 19.1 Condição if/else

A estrutura condicional `if` recebe um valor e resolve, colocando a resposta como um valor **BOOLEANO**. Ou seja: você poderá retornar apenas um valor **VERDADEIRO**, representado por **if (condição)** ou **FALSO**, representado por **else** (como os exemplos de SE dados acima).

Estrutura de código para a condição **IF/ELSE**:

```php
if (condition) {
    // condição verdadeira
    // faça algo
} else {
    // condição falsa
}
```

[Link para documentação - IF](https://www.php.net/manual/pt_BR/control-structures.if.php) 
[Link para documentação - ELSE](https://www.php.net/manual/pt_BR/control-structures.else.php)

A estrutura acima representa exatamente como será feito em código, abaixo alguns exemplos:

### 19.1.1 Validação maioridade

```php
$idade = 17;

if ($idade >= 18) {
    echo "Você é maior de idade";
} else {
    echo "Você é menor de idade";
}
// Result: "Você é menor de idade"
```

### 19.1.2 Comparação simples com strings

```php
$grupo = "ZezinhoDevs";

if ($grupo == "He4rtDevs") {
    echo "Sim, esse é o melhor grupo de devs do brasil";
} else {
    echo "Isso nem existe velho tá maluco";
}
// Result: "Isso nem existe velho tá maluco"
```

### 19.1.3 Retratando checagem de autenticação

```php
$estouLogado = true;

if ($estouLogado) {
    echo "Continue acessando sua aplicação";
} else {
    echo "Redirecionando para o login";
}
// Result: "Continue acessando sua aplicação"
```

### 19.1.4 Condição com dois parâmetros

```php
$usuario = "danielhe4rt";
$senha = "secret123";

if ($usuario == "danielhe4rt" && $senha == "secret123") {
    echo "Olá danielhe4rt, seja bem vindo";
} else {
    echo "Credenciais incorretas";
}
// Result: "Olá danielhe4rt, seja bem vindo"
```

## 19.2 Condição if/else if/else

Quando vemos algum tipo de condição de if/else, o IDEAL é que sejam duas possibilidades de escolha. Porém, toda linguagem de programação existe a condicional extra chamada **else if**, na qual adiciona mais uma possibilidade de retorno **VERDADEIRA** para a condição.

Na prática, você pode ter N checagens para interpretar uma resposta retornando **VERDADEIRO**, até chegar na condição **FALSO**. Entenda o exemplo abaixo:

```php
if (first condition) {
    // condição verdadeira
} else if(second condition) {
    // condição verdadeira
} else if(third condition) {
    // condição verdadeira
} else {
    // condição falsa
}
```

Você pode adicionar quantos Else if's você quiser no código, mas lembre-se de terminar usando else para ter uma interpretação de condição FALSA.

[Link para documentação](https://www.php.net/manual/pt_BR/control-structures.elseif.php)

Abaixo alguns exemplos:

```php
$userDaniel = "danielhe4rt";
$passDaniel = "secret123";

$userCaio = "caioarruda";
$passCaio = "caiozin123";

if ($userDaniel == "danielhe4rt" && $passDaniel == "secret123") {
    echo "Olá danielhe4rt, seja bem vindo";
} else if ($userCaio == "caiozin" && $passCaio == "321321") {
    echo "Olá caiozin, seja bem vindo";
} else {
    echo "Credenciais incorretas";
}
```

```php
$userDanoel = "danoelCoracion";
$passDanoel = "Pssword";

$userArthur = "arthurabreu00";
$passArthur = "tutututututsussuussusw";

if ($userDanoel == "danoelCoracion" && $passDanoel == "Pssword") {
    echo "Olá danoelCoracion, seja bem vindo";
} elseif ($userArthur == "arthurdeabreu" && $passArthur == "321321") {
    echo "Olá Arthur, seja bem vindo";
} else {
    echo "Credenciais incorretas";
}
```

## 19.3 Condição switch-case

O construtor **switch** parece bastante com a lógica do if/else if, porém há uma estrutura melhor para comportar o que você deseja colocar como valores predefinidos.

A declaração tem como base uma condição e N casos de uso dependendo do valor inserido na condição, e é finalizado após a palavra reservada **break** ser acionada, que pode ser interpretado como o fim de um bloco de código...

Caso não haja nenhuma opção elegível dentro dos casos citados, você pode usar a opção **default** para retornar um valor padrão.

Um bom exemplo de quando usar o **switch case** é quando você está em um jogo/chat e há comandos onde um bot te responde baseado no que você inseriu no chat.

Estrutura do switch-case:

```php
switch (cond) {
    case val1:
        // faça algo
        break;
    case val2:
        // faça algo
        break;
    case val3:
        // faça algo
        break;
    defaut:
        // faça algo quando nenhuma das opções for selecionada
        break;
}
```

```php
$comando = "!he4rt";

switch($comando){
    case "!site":
        echo "Link: https://heartdevs.com";
        echo "Esse é o site oficial";
        break;
    case "!he4rt":
        echo "Entre no nosso discord: https://discord.com/he4rt";
        echo "Esse é o discord oficial";
        break;
    case "!comandos":
        echo "Segue a lista de comandos";
        echo "!he4rt !site";
        break;
    default:
        echo "nada acontece feijoada";
        break;
}
// return Entre no nosso discord: https://discord.com/he4rt Esse é o discord oficial
```

```php
$comando = "!teste";

switch($comando){
    case "!site":
        echo "Link: https://heartdevs.com";
        echo "Esse é o site oficial";
        break;
    case "!he4rt":
        echo "Entre no nosso discord: https://discord.com/he4rt";
        echo "Esse é o discord oficial";
        break;
    case "!comandos":
        echo "Segue a lista de comandos";
        echo "!he4rt !site";
        break;
    default:
        echo "nada acontece feijoada";
        break;
}
// return Nada acontece feijoada
```

## 19.4 Condição match

O Match é uma novidade do PHP 8, com ela ganhamos uma nova opção para fazer comparações multiplas, além dos classico if e else e do switch, visto anteriomente.

O **match** apróxima-se bastante do switch, em sua lógica. Onde ele pecorre as opções e retorna a primeira que é compativel com suas condicionais. As diferenças entre eles é sua sintaxe mais elegante e suas operações sempre, são acompanhadas pela comparação com os tipos `"==="`.

Outra vantagem do **match**, é a relização de operações, entre cenário positivos (Exemplo 02), onde podemos fazer novas comparações, para encontrar um resultado esperado.

[Link para documentação](https://www.php.net/manual/en/control-structures.match.php)

Exemplo 1

```php
$comando = "!he4rt";
echo match($comando) {
    "!site" => "Link: https://heartdevs.com",
    "!he4rt", "!discord" => "Entre no nosso discord: https://discord.com/he4rt",
    default => "nada acontece feijoada"
}; // "Entre no nosso discord: https://discord.com/he4rt"
```

Exemplo 2

Caso, não seja uma opção assertiva, sempre caíra no 'default':

```php
echo match("heart devs") {
    "!site" => "Link: https://heartdevs.com",
    "!he4rt", "!discord" => "Entre no nosso discord: https://discord.com/he4rt",
    default => "nada acontece feijoada"
}; // "nada acontece feijoada"
```

Exemplo 3

Neste exemplo, vamos classificar a idade do usuario. Em vez de escrevermos um switch ou if/else gigansteco, podemos reduzir esta logica a apenas 6 linhas.

```php
$idade = 21;
$result = match (true) {
    $idade >= 65 => 'Idoso',
    $idade >= 25 => 'Adulto',
    $idade >= 18 => 'Jovem adulto',
    default => 'Criança',
};

echo $result; // "Jovem Adulto"
```

## 19.5 Condição ternário

O operador ternário ajuda na escrita de condições if/else diminuindo para uma única linha. Ou seja, será algo para ser usado quando você tem uma fácil comparação e um retorno SIMPLES.

O operador ternário leva alguns símbolos para substituir o uso de parênteses e chaves, sendo eles o **?** e **:**

O Sinal de **?** sinaliza para o interpretador que tudo que for escrito anteriormente, será a condição a ser executada.

Após o sinal de **?** e entre o sinal de **:** é o que irá retornar se a condição for verdadeira e após o sinal de **:** é o que irá retornar caso a condição for falsa.

Abaixo alguns exemplos:

```txt
Modelos de ternário

condition ? case true : case false;
```

Exemplo 1

```php
$nickname = 'danielhe4rt';

$who = $nickname == "jorge123" ? "é o jorge online" : "não é o jorge online";

echo $who; //  não é o jorge online
```

Exemplo 2

```php
$modoTeste = true;

return $modoTeste  ? "MODO DESENVOLVIMENTO ATIVADO" : "MODO DESENVOLVIMENTO DESATIVADO";
// return MODO DESENVOLVIMENTO ATIVADO
```

## 19.6 Coalescência nula

O operador de coalescência nula (**??**) fornece uma forma conveniente de retornar o valor antes do sinal de **??** caso o valor exista e não seja **NULL** ou retorna o valor após o sinal de **??**.

É especialmente útil quando queremos retornar um valor padrão caso uma chave não exista em um array associativo, pois é um ótimo substituto para o operador ternário ou uma estrutura de if/else nesses casos.

[Link para documentação](https://www.php.net/manual/pt_BR/language.operators.comparison.php#language.operators.comparison.coalesce)

```php
$descricaoPorCodigo = array(
    1 => 'Este usuário já existe.',
    2 => 'Senha incorreta.',
    3 => 'Este usuário está bloqueado.',
);

// Exemplo utilizando operador ternário - Retorna 'Alguma coisa deu errado', pois a chave 5 não existe
return isset($descricaoPorCodigo[5]) ? $descricaoPorCodigo[5] : 'Alguma coisa deu errado.';

// A lógica acima pode ser simplicada utilizando o operador de coalescência nula
return $descricaoPorCodigo[5] ?? 'Alguma coisa deu errado.';
```


`isset` verifica a existência de uma variável ou uma chave e retorna um valor boleano. Se a variável/chave existir e **não possuir** o valor igual a `NULL` o resultado retornado será `TRUE`, caso for `NULL` ou não existir, o resultado retornará `FALSE`.

# 20 Estruturas de Controle Loops

As estruturas de controle relacionadas a Loops tendem a ter regras para continuar executando instruções do código até que essa regra seja quebrada.

Em outras palavras, você tem uma condição que é interpretada como um valor lógico que é checada e enquanto ela for verdadeira, o bloco de código é executado até que o valor a ser checado mude para falso.

## 20.1 For

O laço `for` funciona baseado em três argumentos dentro de parênteses, separados por vírgulas como uma condição para ser executado até que essa condição acabe.

Quando vemos uma condição que leva três argumentos no inicio, parece um pouco estranho. Mas vamos entender primeiro como funciona e como se aplica.

Quando falamos dos argumentos, temos que entender primeiramente que o FOR trata-se de um loop baseado num incrementador/decrementador até que a condição seja realizada.

```php
for (valor inicial; condição; incremento/decremento) {
    // Faça algo maneiro aqui
}

for ($i = 0; $i < 10; $i++) {
    // Faça algo maneiro aqui
}
```

Agora falaremos dos parâmetros do for:

1. **Primeiro parâmetro** **índice inicial** no qual você quer trabalhar
	Esse índice é um número inteiro onde você trabalhará com incrementação ou decrementação.

2. **Segundo parâmetro** **condição** para que o laço seja finalizado.
	Se você tem um índice como primeiro parâmetro, a cada vez que esse loop rodar você terá incrementado ou decrementado, fazendo a mesma pergunta da condição até que ela seja satisfeita.

3. **Terceiro parâmetro** **incrementador/decrementador**
	Esse parâmetro será responsável por dizer ao loop se ele vai incrementar ou decrementar o índice do laço.


Se você tem um índice como primeiro parâmetro, a cada vez que esse loop rodar você terá incrementado ou decrementado, fazendo a mesma pergunta da condição até que ela seja satisfeita.

Exemplo 1. Contando até 10

```php
$contador = 10;
echo "Script pra contar até" . $contador . PHP_EOL;
for($i = 1; $i <= $contador; $i++){
    echo $i . "... ";
}
echo PHP_EOL . "Script finalizado!";

// Resultado
// "Script pra contar até 10"
// "1... 2... 3... 4... 5... 6... 7... 8... 9... 10..."
// "Script Finalizado!"
```

Exemplo 2. Tabuada do 5

```php
$multiplicador = 5;
echo "Script pra imprimir a tabuada do $multiplicador" . PHP_EOL;
for($i = 1; $i <= 10; $i++){
    echo $multiplicador . " x " . $i  . " = " . ($multiplicador * $i) . PHP_EOL;
}
echo "Script finalizado!";

// Resultado
// "Script pra imprimir a tabuada do 5"
// "5 x 1 = 5"
// "5 x 2 = 10"
// "5 x 3 = 15"
// "5 x 4 = 20"
// "5 x 5 = 25"
// "5 x 6 = 30"
// "5 x 7 = 35"
// "5 x 8 = 40"
// "5 x 9 = 45"
// "5 x 10 = 50"
// "Script Finalizado!"
```

## 20.2 While

A estrutura de condição while leva uma condição booleana no começo que é executada eternamente enquanto o valor passado for verdadeiro.

Ele só tem uma condição a ser lida e vai ficar em execução até que essa condição seja declarada como falsa.

```php
while(condição){
    // faça algo maneiro
}
```

Vamos dar os mesmos exemplos da condição **for** só que com o laço **while**:

Exemplo 1. Contando até 10:

```php
$continuaLoop = true;
$i = 1;
echo "Script pra contar até 10"  . PHP_EOL;
while ($continuaLoop){
    echo $i . "... ";
    if ($i == 10){
        $continuaLoop = false;
    }
    $i++;
}
echo PHP_EOL . "Script finalizado!";

// Resultado
// "Script pra contar até 10"
// "1... 2... 3... 4... 5... 6... 7... 8... 9... 10..."
// "Script Finalizado!"

```

Vocês perceberam que foi utilizado mais código fazendo com o while do que com o for? Isso é por quê quando tratamos de situações incrementais, o laço for é a melhor solução pra isso. Porém, nada te impede de fazer a mesma coisa junto ao while.

Você também pode usar a expressão **while($i++ < $contador)** mas raramente é usado pra algo em códigos que serão utilizados em produção.

## 20.3 Foreach

O laço de repetição **foreach** é usado para iterar arrays ou objetos. O foreach funciona passando por cada elemento do array e atribuindo à ele variáveis do escopo da estrutura, para uma melhor manipulação dos elementos.

O foreach acontece enquanto houver iteráveis dentro do array e pode parar com a condição **break**, caso não, ele continua até o final do array.

A estrutura do foreach leva dois ou três parâmetros para ser iterado, com a possiblidade de não declarar o valor do índice. Entenda abaixo:

```php
$names = ["waasleey", "leozin044", "rychillie", "jpbrabo"];
// Iteração sem a indíce
foreach($names as $name){
    echo $name . " ";
}
// Retorno: waasley leozin044 rychillie jpbrabo

// Iteração com a indíce
foreach($names as $key => $name){
    echo $key . "." . $name . " ";
}
// Retorno: 0.waasley 1.leozin044 2.rychillie 3.jpbrabo
```

Como primeiro parâmetro, o foreach espera um array ou objeto onde ele possa percorrer os índices.

Como segundo parâmetro, será o nome da váriavel que receberá o valor da iteração. Porém caso você queira colocar o índice e valor da iteração, você deverá atribuir mais uma variável com o sinal de **igual maior =>**, colocando o nome da variável de índice atrás da seta e a variável com o valor a da iteração após a seta.

```php
foreach ($array as $iteracao => $valor)
```

Não necessáriamente precisamos colocar o indíce, pois caso não seja usado para algo dentro do loop, só irá consumir mais um espaço na memória.

Exemplo 1. Iterando um objeto

```php
$pessoa = new StdClass;
$pessoa->nome = "danielhe4rt";
$pessoa->idade = 21;
$pessoa->trabalho = "Fullstack Developer";

foreach ($pessoa as $chave => $valor) {
    echo "$chave: $valor" . PHP_EOL;
}
// Resultado:
// nome: danielhe4rt
// idade: 21
// trabalho: Fullstack Developer
```

Exemplo 2. Iterando um objeto com chaves e valores

```php
$pessoa = [
    "nome" => "danielhe4rt",
    "idade" => 21,
    "trabalho" => "Fullstack Developer"
];
foreach ($pessoa as $chave => $valor) {
    echo "$chave: $valor" . PHP_EOL;
}

// Resultado:
// nome: danielhe4rt
// idade: 21
// trabalho: Fullstack Developer
```

Exemplo 3. Iterando um objeto com chaves e valores:

```php
$pessoa = [
    "danielhe4rt",
    21,
    "Fullstack Developer"
];
foreach ($pessoa as $chave => $valor) {
    echo "$chave: $valor" . PHP_EOL;
}

// Resultado:
// 0: danielhe4rt
// 1: 21
// 2: Fullstack Developer
```

Exemplo 4 Iterando um objeto com chaves e valores

```php
$pessoa = [
    "danielhe4rt",
    21,
    "Fullstack Developer"
];
foreach ($pessoa as $valor) {
    echo "$valor" . PHP_EOL;
}

// Resultado:
// danielhe4rt
// 21
// Fullstack Developer
```

## 20.4 Controlando suas repetições

Bom, agora que entendemos sobre loops, podemos encontrar algumas situações, onde queremos controlar o fluxo de interação. Seja pulando uma interação especifica, ou simplesmente interromper sua execução. Para estes casos temos o `continue` e o `break`.
### 20.4.1 Continue 

O cotinue, é uma espécime de "comando", que damos para nossa repetição "pular" aquela interação, em especifico.

Vamos imaginar uma situação onde queremos imprimir apenas, números pares, podemos a utilizar para imprimir apenas eles.

Exemplo 1. Imprimindo numeros pares

```php
for ($numero = 0; $numero < 5; $numero++) {
    if($numero % 2 === 1){
        continue;
    }

    echo $numero . " é par.";
    // Resultado:
    // 0: 0 é par
    // 2: 2 é par 
    // 4: 4 é par
}
```

### 20.4.2 Break

O `break` assim como o `continue`, é um comando para o controle do fluxo de repetição. Porém sua função é de interromper a interação por completo, normalmente é utilizado quando o loop já satisfez sua funcionalidade e não tem necessidade de ir até o final.

Exemplo 1. Loops Infinitos

```php
while(true){
    echo "Olá seja bem vindo, qual mensagem deseja enviar?"  . PHP_EOL;
    echo "1. Bom dia" . PHP_EOL;
    echo "2. Boa tarde". PHP_EOL;
    echo "3. Boa noite" . PHP_EOL;
    echo "0. SAIR" . PHP_EOL;
    
    // Nota: a função readline, é apenas uma maneira de coletar a informação vinda de um usuario. 
    $resposta = readline ('Digite uma opção: '); // digitei: 1
    
    if($resposta == '1') {
        echo 'Bom dia' . PHP_EOL;
    } else if($resposta == '2') {
        echo 'Boa tarde' . PHP_EOL;
    } else if ($resposta == '3') {
        echo 'Boa noite' . PHP_EOL;;
    }else if($resposta == '0') {
        echo 'Bye!' . PHP_EOL;
        break;
    }
}
```

Perceba que no exemplo acima, assim que o úsuario digitar 0 o programa irá ser "finalizado".

Na sessão anterior [Estruturas de controle de condições](https://github.com/danielhe4rt/php4noobs/blob/master/3-Basico/13-Estruturas-de-controle-cond.md). Nós lhe apresentamos a estrutura `switch` e juntamente a ela já haviamos lhe apresentado o comando `break`. Porém, em uma situação diferente, dentro do switch, neste caso o mesmo não irá ter efetividade sobre o loop.

Exemplo 2. Trocando if/else por switch

```php
while(true){
    echo "Olá seja bem vindo, qual mensagem deseja enviar?"  . PHP_EOL;
    echo "1. Bom dia" . PHP_EOL;
    echo "2. Boa tarde". PHP_EOL;
    echo "3. Boa noite" . PHP_EOL;
    echo "0. SAIR" . PHP_EOL;
    $resposta = readline ('Digite uma opção: '); 

    switch($resposta){
        case '1':
            echo 'Bom dia' . PHP_EOL;
            break;
        case '2':
            echo 'Boa tarde' . PHP_EOL;
            break;
        case '3':
            echo 'Boa noite' . PHP_EOL;
            break;
        case '0':
            break; // Isso me parece um pouco estranho, não ??????
        break;
    }
}
```

O código acima entrará em _loop infinito_, o comando `break` sempre será utilizado para sua função dentro do switch case, mas **não interromperá** o loop, então _CUIDADO_.

# 21 Namespaces

Namespaces no PHP servem para encapsular códigos e eliminar a possibilidade de colisão de nomes. É uma forma de agrupar classes, interfaces, funções, métodos, constantes, entre outros que estão relacionadas.

Uma **declaração** começa com a palavra-chave `namespace` e termina com um ponto e vírgula.

Declarando um namespace

```php
<?php

namespace Controllers;

class IndexController
{
    //aqui vai o conteúdo/definição da classe
}
```

Observe no exemplo acima, que a declaração de `namespace` é a primeira linha de código em um arquivo. Todo o código que vem depois é encapsulado no namespace `Controllers`.

## 21.1 Sub namespace

Também é possível escrever sub-namespaces. Tudo o que está definido no exemplo abaixo fará parte do namespace `Controllers\Admin`

```php
<?php

namespace Controllers\Admin;

class AdminController
{
    //aqui vai o conteúdo/definição da classe
}
```

## 21.2 A instrução `use`

Uma vez que você declarou namespaces em seu sistema é possível importar classes, traits, etc. Para isso basta usar a instrução `use`.

A instrução `use` substitui a necessidade das variações de `require` e `include` para importação de arquivos de código. Cada namespace deve ter sua própria instrução `use`.

1. Importando códigos com a instrução use

```php
<?php

namespace Controllers;

use Symfony\Component\Console\Input\{InputInterface, InputOption};
use Symfony\Component\Console\Output\OutputInterface;
use Zend\Twitter;
```

## 21.3 Alias em namespaces: as

O uso de um namespace também permite [_alias_](https://pt.wikipedia.org/wiki/Alias_\(comando\)). Isso é feito usando a palavra-chave `as` para reduzir o namespace ou para evitar colisões devido a nomes iguais.

1. Exemplo de uso de alias em namespaces: 

```php
<?php

namespace Controllers;

use Zend\Twitter as Twit;

```

## 21.4 Notas sobre namespaces 

- Vimos algumas coisas aqui que estão relacionadas a orientação a objetos, não se preocupe com isso agora, teremos uma sessão só pra tratar disso.

- Namespaces são [_case-insensitive_](https://pt.wikipedia.org/wiki/Case-sensitive), significa que tanto faz escrever com letras maiúsculas ou minúsculas, mas fique atento aos padrões de PSRs, falaremos sobre isso também.

# 22 Session

Trabalhar com o conceito de sessões permite que um conjunto de dados, possam ser utilizados pelos os usuários durante todo o tempo em que acessa e navega dentro da aplicação web sendo persistidos. Então dessa forma, é possível, por exemplo, verificar se o usuário está logado ou não no site, pegar um conteúdo que está dentro de uma carrinho de compras, ou até controlar permissões de execução do usuário, e muito mais.

- Session é uma variável superglobal, é uma array associativo que basicamente, são estruturas onde cada elemento que esta dentro do array, é identificado por uma chave única.

## 22.1 `*session_start()*`

A função session_start() permite iniciar uma nova sessão ou até resumir (continuar) uma sessão que já existe.

1. Iniciar uma sessão

```php
<?php
  session_start(); //Uma nova sessão de usuário é iniciada.
?>
```

O retorno da função

- TRUE sessão iniciada com sucesso.
- FALSE sessão deu falha em iniciar.

## 22.2 `$_SESSION`

Aqui nesse exemplo vamos trabalhar com duas páginas php. Na primeira página, vamos iniciar uma sessão e em seguida, passar os valores para as duas variáveis de sessão criadas.

1. Declarando a sessão `$_SESSION`

```php
<?php
  // Página 1

  session_start();

  // Exibir um texto na tela do usuário
  echo "Esta é a página 01, onde a sessão será criada";

  // Vamos criar uma sessão com o nome da variável aula e hora
  $_SESSION["aula"] = "PHP";
  $_SESSION["hora"] = time();

  // Link para a página 02:
  echo '<br /><a href="pagina2.php">Clique para ir à página 02</a>';

?>

```

Após carregar a página 01, a sessão é criada e as variáveis de sessão ‘aula’ e ‘hora’ são declaradas e inicializadas. Elas poderão ser acessadas na página 02, clicando-se no link fornecido.

A seguir está o código do arquivo pagina2.php:

```php 
<?php
// E esta é a página 02, onde recuperaremos as variáveis de sessão

session_start();

date_default_timezone_set('America/Sao_Paulo');

echo 'Agora estamos na página 02<br />';
echo "Estamos na aula de " . $_SESSION['aula'] . "<br>";

echo "E agora são " . date('H:i:s', $_SESSION['hora']) . " horas";

?>
```

Neste exemplo, a sessão é criada logo que o usuário carrega a página 01. Porém, é muito comum que se deseje criar uma nova sessão apenas quando algum evento específico ocorrer, como o clique em um botão de formulário.

# 23 Introdução a Orientação a Objetos

## 23.1 O que é?

A OO como se costuma chamar, é um dos paradigmas de programação suportados pelo PHP.

### 23.1.1 Paradigmas de programação

- Procedural;
- Funcional;
- Lógico;
- **Orientação a Objetos;**
- Concorrente;
- Reativo.

### 23.1.2 O que são paradigmas de programação?

Bom, na programação paradigmas são formas de se fazer algo, um padrão, uma conduta. No PHP, costuma-se escrever códigos usando os paradigmas Procedural e/ou Orientado a Objetos. Mesmo que na teoria a OO foi o sucessor do paradigma procedural, na prática é comum misturar os dois.

#### 23.1.2.1 Um pouco sobre estes paradigmas

- O Procedural consiste em:
    - Chamada de procedimentos para manipulação de dados, interpretação sequencial etc.

- Orientação a Objetos:
    - Estrutura de dados com atributos e métodos. Na OO é necessário pensar diferente, fazendo abstrações da realidade para o código (neste caso transformando coisas e objetos do mundo real em Classes no PHP).

## 23.2 Orientação a Objetos de forma resumida

Em OO a estrutura do dado possui métodos(funções) dentro deles, ou seja o dado é quem tem seus respectivos métodos e atributos. Diferente do procedural onde se chama funções para manipulação de dados já existentes;

## 23.3 Pilares da Orientação a Objetos

- Abstração
    - Entidade: A partir de uma observação, "pegar" um objeto do mundo real e entender como traduzir este objeto para o seu código;
    - Identidade: Atribuição de uma identidade única a cada objeto originado da entidade;
    - Atributos: Características;
    - Métodos: Ações a serem realizadas.

- Encapsulamento
    - Ter detalhes de implementação escondidos e mostrar somente quando necessário a partir dos "métodos mágicos" (conteúdo para os próximos capítulos).
    - Determinar o que será enxergado e o que não será. O encapsulamento portanto é uma forma de dar visibilidade(public, private, protected) para esses atributos e métodos de acordo com as nossas necessidades.

- Herança
    - É basicamente reaproveitamento de código. Objetos(Classes) que herdam de outros, e/ou um conjunto de objetos ligados que geram outro determinado objeto.
    - Ou seja, a partir da composição de objetos mais simples gerar objetos mais complexos.

- Polimorfismo: Multiplas formas
    - Atribuição de conceitos concretos a outros mais genéricos.
    - Exemplo:
        - Objeto carro pode apontar hora para o objeto ferrari, hora outra para o objeto Uno.

### 23.3.1 Classe vs Objeto

- classe: Estrutura que definirá seus objetos personalizados
    
    - Anatomia: `<?php class Nome { //corpo }`
    - Membros: - Atributos - Dados - Comportamentos - Métodos(funções) 
    - Para acessar um membro use '->' ou '::'(Falaremos disso mais a frente);
        
    Basicamente a classe define um tipo ou uma estrutura de dados, tipo este de acordo com suas necessidades. Uma classe representa no código uma abstração da realidade. É trazer conceitos da vida real para dentro do seu software.


- Objeto: Toda instância de uma classe é um objeto mas nem todo objeto é uma instância.
    
    - Quando um dado é gerado a partir de uma classe, este dado é chamado de objeto.

# 24 Classes

## 24.1 O que são

As classes são responsáveis por criarem estruturas e comportamentos para conceitos das aplicações e do mundo real, elas são compostas basicamente por propriedades e métodos. As propriedades funcionam como característias de um objeto (representa uma analogia aos objetos do mundo real/virtual) e os métodos representam suas funcionalidades. Podemos ter um exemplo de um jogador de qualquer jogo virtual, onde ele se registra, tem uma quantidade X de dinheiro, e caso queira pode trocar de senha, veja este exemplo:

```php
// Player.php
class Player {

    public string $username; // propriedade/atributo
    private string $password; // propriedade/atributo
    protected float $money; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $username, string $password, float $money)
    {
        $this->username = $username; // Setter do Construtor
        $this->password = password_hash($password, PASSWORD_ARGON2I); // Setter do Construtor
        $this->money = $money; // Setter do Construtor
    }

    /**
     * Metodo: canBuy - Checa se o jogador tem dinheiro suficiente para comprar um item
     * @param itemPrice float
     * @return bool 
     */

    public function canBuy(Item $item): bool 
    {
        return $this->getMoney() >= $item->getPrice();
    }

    /**
     * Metodo: updatePassword (Setter) - Altera a senha do jogador
     * @param oldPassword string
     * @param newPassword string
     * @return void 
     */

    public function updatePassword(string $oldPassword, string $newPassword): void
    {
        if (!password_verify($oldPassword, $this->password)) {
            throw new Exception('A senha anterior está incorreta.');
        }

        $this->password = password_hash($newPassword, PASSWORD_ARGON2I);
    }

    /**
     * Método: getMoney (Getter) - retorna a quantidade de dinheiro do jogador
     * @return float
     */
    public function getMoney(): float 
    {
        return $this->money;
    }
}
```

```php
// Item.php
class Item {

    private string $name; // propriedade/atributo
    private float $price; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $name, float $price)
    {
        $this->name = $name;
        $this->price = $price;
    }

    /**
     * Método: getName (Getter) - retorna o nome do item
     * @return string
     */
    
    public function getName(): string
    {
        return $this->name;
    }

    /**
     * Método: getPrice (Getter) - retorna o preço do item
     * @return float
     */
    public function getPrice(): string 
    {
        return $this->price;
    }
}
```

Uma boa prática e um jeito de não tomar tapa na cara dos seus colegas do projeto é manter **uma classe por arquivo**, por motivos de localização e indexação de arquivos. Se você ver o coleguinha colocando mais de uma classe por arquivo pode mete a mão na cara desse maluco >:@

## 24.2 Como usar?

As classes devem ser instânciadas para serem usadas, uma instância deve ser criado através da sintaxe:

```php
$woodenSword = new Item('Wooden Sword', 800);

$silverSword = new Item('Silver Sword', 5640);

$danielhe4rt = new Player('danielhe4rt','secret123', 1000);
```

 >Nota: podemos notar que quando instanciamos a classe Item e a Player, houveram paramêtros sendo passados. Essa sequência de parametros é devido ao método CONSTRUTOR que colocamos na classe.

Seus métodos e atributos podem ser chamados e acessados através do operador '->' (também conhecido pelos devs BR's como setinha :p). 

Sintaxe:

```php
//Atributo:
echo "Nome de usuário: " . $danielhe4rt->username;

//Métodos:
echo "Saldo: "  . $danielhe4rt->getMoney();

if ($danielhe4rt->canBuy($woodenSword)) {
    echo $danielhe4rt->username . ', você pode comprar a' . $woodenSword->name . '!';
} else {
    echo $danielhe4rt->username . ', caraio tiozão ce tá liso hein? Vai ter como comprar a ' . $woodenSword->name . ' não!';
}

if ($danielhe4rt->canBuy($silverSword)) {
    echo $danielhe4rt->username . ', você pode comprar a' . $silverSword->name . '!';
} else {
    echo $danielhe4rt->username . ', caraio tiozão tem nem pra espada de madeira e quer a ' . $silverSword->name . ' num fode né!';
}
```

# 25 Construtores e destrutores

## 25.1 O que são?

Os construtores e destrutores são metódos mágicos que executam determinadas tarefas assim que a classe é instânciada e antes de ser removida da memória.

## 25.2 Construtores

Os construtores são especificados por um metódo chamado `__construct` e são executados sempre que a classe é chamada. Você pode por exemplo, atribuir valores não-primitivos a atributos da classe antes de executar qualquer ação, o que não seria possível sem um construtor.

Vamos imaginar a classe `Player`, que contem os atributos base de um personagem de um jogo: `username`, `password`, `money`. Quando criamos um novo objeto de uma classe e você tem um construtor, ele é tido como uma "função" que recebe os parâmetros. Olhe a classe abaixo:


```php
// Player.php

class Player
{

    public string $username; // propriedade/atributo
    private string $password; // propriedade/atributo
    protected float $money; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $username, string $password, float $money)
    {
        $this->username = $username; // Setter do Construtor
	        $this->password = password_hash($password, PASSWORD_ARGON2I); 
	        // Setter do Construtor
        $this->money = $money; // Setter do Construtor
    }
}
```

Note que o construtor é uma função que recebe parâmetros na ordem que você quiser. E quando vamos instância-lá, usamos a palavra reservada `new` e o nome da classe `Player` e os parametros `('danielhe4rt','secret123', 1000)` na ordem que foram declaradas no escopo do construtor e atribuimos a uma variavel. Fica assim:

```php
$danielhe4rt = new Player('danielhe4rt', 'secret123', 1000);
```

Se você não passar algum dos parâmetros ou colocá-los fora de ordem, seu código apontará um erro falando que falta argumentos ou que os dados passados não **seguem os mesmos tipos** (lembre-se de tipar os parametros de suas funções).

Caso você queira deixar um argumento opcional, você deverá atribuir um valor padrão pra eles. Se liga:

```php
// Player.php

class Player
{

    public string $username; // propriedade/atributo
    private string $password; // propriedade/atributo
    protected float $money; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $username, string $password, float $money = 1500.0)
    {
        $this->username = $username; // Setter do Construtor
        $this->password = password_hash($password, PASSWORD_ARGON2I); // Setter do Construtor
        $this->money = $money; // Setter do Construtor
    }
}
```

```php
// Instancia sem o valor do atributo money
$danielhe4rt = new Player('danielhe4rt', 'secret123');
```

Ele não foi necessário porquê falamos em nosso construtor que:

- Se não for passado o valor do atributo money, coloque-o como **1500.0** (valor padrão).
- Se for passado o valor do atributo money, sobrescreva o valor padrão de **1500.0** pelo valor passado na variavel.

Uma coisa bem importante sobre os atributos padrões em construtores é que eles devem ser declarados da direita para a esquerda. Entenda o caso abaixo:

```php
// Player.php

class Player
{

    public string $username; // propriedade/atributo
    private string $password; // propriedade/atributo
    protected float $money; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $username = 'danielhe4rt', string $password, float $money = 1500.0)
    {
        $this->username = $username; // Setter do Construtor
        $this->password = password_hash($password, PASSWORD_ARGON2I); // Setter do Construtor
        $this->money = $money; // Setter do Construtor
    }
}
```

```php
// Instancia sem o valor do atributo username
$danielhe4rt = new Player('secret123', 99999);
```

Esse código acima geraria um erro assim que a classe for lida pois se há mais de 1 argumento e o primeiro dos argumentos tiver um valor padrão e o segundo não, ele **não saberá como interpretar** já que a declaração começa da esquerda para a direita.

Como poderiamos fazer esse cenário dar certo? Colocando os valores padrões a direita do escopo do construtor e os que não tiverem valores padrões à esquerda.

```php
// Player.php

class Player
{

    public string $username; // propriedade/atributo
    private string $password; // propriedade/atributo
    protected float $money; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $password, string $username = 'danielhe4rt', float $money = 1500.0)
    {
        $this->username = $username; // Setter do Construtor
        $this->password = password_hash($password, PASSWORD_ARGON2I); // Setter do Construtor
        $this->money = $money; // Setter do Construtor
    }
}
```

```php
// Instancia sem o valor do atributo username e o money
$danielhe4rt = new Player('secret123');

$danielhe4rt->username; // danielhe4rt
$danielhe4rt->money; // 1500.0
```

Construtores são bem simples assim que você entende algumas regras e há muito mais a ser explorado, mas vamos manter isso simples!

## 25.3 Destrutores

Já os destrutores agem no momento oposto aos construtores, bem antes da classe ser removida da memória, sendo atribuídas `null` ou usando `unset`. Suas ações devem ser definidas no metódo `__destruct`.

```php
class Player
{

    public string $username; // propriedade/atributo

    /**
     * Método mágico: construtor
     */
    public function __construct(string $username)
    {
        $this->username = $username; // Setter do Construtor
        echo "Jogador Cadastrado!";
    }

    /**
     * Método mágico: destrutor
     */
    public function __destruct() 
    {
        echo "Conta do jogador " . $this->username . " encerrada!";
    }
}
```

Note que deixei a classe bem sucinta e coloquei um echo para quando a classe é construida e quando a variável que recebe o objeto é removida da memória para dar um exemplo de como acontece o processo. Se liga:

```php
$danielhe4rt = new Player('danielhe4rt');
// Jogador Cadastrado!

unset($danielhe4rt);
// Conta do jogador danielhe4rt encerrad!

```

## 25.4 Notas sobre Construtores e destrutores

Ambos os metódos demostrados acima não devem retornar ou especificar tipo de retorno(apesar deste ser `void` por padrão).

Classes que herdam outras usarão o construtor da classe-pai caso não definam um construtor próprio.

# 26 Herança

Como já foi dito, a herança é um dos pilares da Progamação Orientada a Objetos. Com ela é possível fazer o reuso de classes que contém atributos e metódos em comum.

Vamos usar como exemplo a relação de um pai e um filho, e seus idiomas nativos, onde o filho irá herdar as características de seu pai. Naturalmente, o pai sabe falar uma linguagem e eventualmente seu filho também aprenderá ela por meio do convívio.

```php

class Pai
{
    public $nome = 'João';

    public $idioma = 'Português';

    public function apresentar()
    {
        echo "Olá, meu nome é {$this->nome} e meu idioma nativo é {$this->idioma}!" . PHP_EOL;
    }
}

class Filho extends Pai {
    public $nome = 'Enzo';
}

```

Neste exemplo, a classe Filho herda a propiedade `idioma` e o metódo `apresentar` da classe Pai. Mesmo não tendo implementado-as em seu corpo, ela tem acesso a elas porque as herdou.

```php
$pai = new Pai();
$pai->apresentar(); //Olá, meu nome é João e meu idioma nativo é Português!

//O filho herda as propriedades do pai
$filho = new Filho();
$filho->apresentar; //Olá, meu nome é Enzo e meu idioma nativo é Português!
```

Como pode ver, apesar do Filho herdar as propriedades do Pai, é possível que estas sejam modificadas, como foi feito com a propiedade `nome`.

A herança em geral, e principalmente a vertical, gera uma relação de razão onde ambos os termos são convertíveis, pois é uma demarcação de categoria pelo gênero próximo e pela diferença específica.

No exemplo acima, podemos deixar essa relação mais clara se substituirmos a palavra-chave `extends` por `é um`.

`Filho "é um" Pai`

Essa relação pode ser verdadeira com algumas premissas:

1. Premissa maior: Que o filho seja Pai
2. Premissa menor: Que o filho não seja pai do seu pai

Nenhuma dessas premissas pode ser estritamente respeitada nessa relação se considerarmos somente a interface:

```php
(fn (Pai $o): Filho => $o)(new Filho);
```

## 26.1 Notas sobre Herança

- Use composição ao invés de herança sempre que possível.
- No PHP não é possível herdar mais de uma classe, para isso são usadas as classes intermediarias, interfaces ou traits.
- Você poderá aprender mais sobre a palavra chave `public` no capitulo sobre [modificadores de acesso](https://github.com/danielhe4rt/php4noobs/blob/master/4-Intermedi%C3%A1rio/4-Modificadores-de-acesso.md)

# 27 Modificadores de Acesso

## 27.1 O que são

Os modificadores de acesso são palavras-chave reservadas para definir quais metódos e/ou propriedades podem ser acessadas à partir de um ponto especifíco do seu código.

## 27.2 Quais são?

No PHP, existem 3 níveis de visibilidade: **public**, **protected** e **private**.

## 27.3 public

O nível de visibilidade public é o padrão de todas as propriedades de uma classe, fazendo-as serem acessíveis dentro do escopo da própria classe e por quaisquer classes externas, não somente as que herdam a classe pai.

Por exemplo, temos uma classe Pessoa, com uma propriedade nome e um metódo apresentar, ambas as propriedades podem ser utilizadas fora da classe.

```php
<?php

class Pessoa {
    public $nome = 'João';
    
    public function apresentar()
    {
        echo "Meu nome é {$this->nome}";
    }
}

$pessoa = new Pessoa();
echo $pessoa->nome . PHP_EOL; //Output: João
$pessoa->apresentar() . PHP_EOL; //Output: Meu nome é João
```

## 27.4 protected

## 27.5 private

```php
<?php

class Pai {

    protected $nomePai = 'João';

    private $cpf = '999.999.999.99';

    public function apresentar()
    {
        echo "Meu nome é {$this->nomePai} e meu CPF é: {$this->cpf}";
    }

    private function mostrarCpf()
    {
        echo $this->cpf;
    }

}

class Filho extends Pai {

    public $nome = 'Pedro';

    public function mostrarCpfPai()
    {
        echo "O CPF do meu Pai é: " . $this->cpf; //Propriedade inexistente
    }
}

$pai = new Pai();
$pai->cpf . PHP_EOL; //Erro fatal
$pai->mostrarCpf() . PHP_EOL; //Erro fatal
$pai->apresentar() . PHP_EOL; //Ok

$filho = new Filho();
$filho->mostrarCpfPai(); //Erro fatal
```

# 28 Métodos Getters

## 28.1 O que são?

Os métodos getters servem para pegar a referência de um valor (geralmente de uma propriedade).

## 28.2 Por que usar?

Como vimos anteriormente em [4.4 - Modificadores de Acesso](https://github.com/danielhe4rt/php4noobs/blob/master/4-Intermedi%C3%A1rio/4-Modificadores-de-acesso.md), temos os modificadores de acesso, e nem sempre queremos deixar as nossas propriedades e métodos públicos, mas se deixarmos privados como vamos acessar seu valor? podemos usar um getter. Veja o exemplo abaixo.

```php
 class exemplo
  {
    private $propriedadePrivada = "Esta propriedade não pode ser alterada nem lida diretamente";
    public $propriedadePublica = "Esta propriedade pode ser alterada e lida diretamente";
    
    
    //Esse método retorna o valor da $propriedadePrivada
    public function getterParaAPropriedadePrivada()
    {
      return $this->propriedadePrivada;
    }
  }
```

No exemplo acima nós criamos duas propriedades, uma privada e uma pública. A propriedade pública pode ser lida e ter seu valor alterado, já a propriedade privada pode ser lida usando o método `getterParaAPropriedadePrivada()`, porém não pode ser alterada.

## 28.3 Como usar?

Podemos usar uma palavra reservada do php `this` para referênciar uma propriedade da nossa classe, Veja o exemplo abaixo.

![[oop-this-propertie.png]]

Podemos criar uma função que retorna a referência desejada usando a palavra `this`.

## 28.4 Getters em métodos estáticos 

Ok criamos getters para as nossas propriedades, Porém esses getters só funcionam em métodos não estáticos, pois a palavra `this` não se aplica em métodos estáticos, para isso temos a palavra `self`.

![[oop-self-propertie.png]]

Em essência nós usamos a palavra `this` para acessar o estado interno de um objeto, e a palavra `self` para acessar membros de uma definição de classe.

```php
  class Exemplo
  {
     private static $propriedadePrivada = "Esta propriedade não pode ser alterada nem lida diretamente";
     public static $propriedadePublica = "Esta propriedade pode ser alterada e lida diretamente";
     
     
     //Esse método retorna o valor da $propriedadePrivada
     public static function getterParaAPropriedadePrivada()
     {
       return self::$propriedadePrivada;
     }
  }
```

# 29 Métodos Setters 

## 29.1 O que são?

Setters são métodos usados para alterar valor de propriedades que não podem ser alteradas diretamente.

## 29.2 Como usar?

Como mostrado em [[#28.3 Como usar?|28.3 Como usar]], podemos usar as palavras reservadas do php `this` e `self` para manipular propriedades privadas. Antes vimos como ler o valor, agora vamos ver como alterar o valor, Veja o exemplo abaixo.

1. Não Estático
```php
    class Exemplo
    {
        private $propriedadePrivada = "Esta propriedade não pode ser alterada ou lida diretamente";

        //Este método define um valor para $propriedadePrivada
        public function SetterParaPropriedadePrivada($novoValor)
        {
            $this->propriedadePrivada = $novoValor;
        }
    }
```

1. Estático
```php
    class Exemplo
    {
        private static $propriedadePrivada = "Esta propriedade não pode ser alterada ou lida diretamente";

        //Este método define um valor para $propriedadePrivada
        public static function SetterParaPropriedadePrivada(string $novoValor)
        {
            self::$propriedadePrivada = $novoValor;
        }
    }
```

Dessa maneira podemos alterar o valor de uma propriedade sem permitir sua leitura (caso você queira permitir a leitura e alteração de valor, é recomendado o uso dos modificadores de acesso `public` ou `protected` no lugar de getters e setters).

# 30 Interfaces

Neste tópico abordaremos o assunto do que são interfaces no PHP e como implementá-las

## 30.1 O que são interfaces?

Bom, para entendermos interfaces, vamos pegar uma definição da própria página do PHP:

>Interfaces de objetos permitem a criação de códigos que especificam quais métodos uma classe deve implementar, sem definir como esses métodos serão tratados.

_**Mas então, o que isso significa?**_

- Significa que interfaces são nada mais, nada menos do que modelos de métodos que podemos implementar em uma classe (ou até mesmo estende-lá em outra interface como veremos mais a seguir), e que ao fazer essa implementação a classe passa a ser obrigada à conter os métodos declarados na interface, resultando em um erro caso não seja feito;

- Em outras palavras, podemos entender interfaces como um contrato, a partir do momento que você assina esse contrato (implementa ele), você passa a ser obrigado a seguir as especificações previstas nele, o descumprimento delas seria punitivo (que no nosso caso seria um erro fatal do código).

## 30.2 Como implementar uma Interface?

Ao trabalharmos com interfaces, usaremos principalmente duas palavras reservadas próprias para o seu uso: `interface` e `implements` , onde:

- **interface:** Palavra reservada para definir a criação de uma interface;
- **implements:** Operador usado para realizar a implementação de interfaces;

Veremos sobre sua síntaxe no código abaixo:

```php
  // sintaxe para a criação:
  interface ProvedorPagamentoInterface
  {
      // declaração de métodos
  }
  
  // sintaxe para a implementação:
  class PaypalProvider implements ProvedorPagamentoInterface
  {
      // métodos e atributos da classe
  }
```

Agora para você entender melhor sobre seu uso, daremos alguns exemplos de como utilizar:

- **Implementação correta de uma interface:**

```php
 // criamos a interface HelloWorld:
  interface HelloWorld 
  {
	  // definimos que as classes que implementarem essa interface, deverá conter o método público helloWorld:
	    public function helloWorld(): void
  }


  // criamos a classe Saudar e definimos que ela irá implementar a interface HelloWorld:
  class Saudar implements HelloWorld
  {
	  public function helloWorld()
	  {
		  echo "Olá mundo!";
	  }
  }

  // instanciamos um objeto através da classe criada e o atribuimos para a váriavel cumprimentos:
  $cumprimentos = new Saudar();
  // acessamos e executamos o método recebido ao objeto:
  $cumprimentos->helloWorld();
```

O output do código acima será: `Olá mundo!`

- **Implementação errada de uma interface:**

```php
  // criamos a interface HelloWorld:
    interface HelloWorld 
    {
	    // definimos que as classes que implementarem essa interface, deverá conter o método público helloWorld:
	       public function helloWorld();
    }

  // criação da classe Somar e definimos que ela irá implementar a interface HelloWorld:
    class Somar implements HelloWorld
    {
	      public function somar($n1, $n2)
	      {
		        return $n1 + $n2;
	      }
    }

  // instanciamos um objeto através da classe criada e o atribuimos para a váriavel metodosMatematicos:
    $metodosMatematicos = new Somar();
  // acessamos e executamos o método recebido ao objeto:
    echo $metodosMatematicos->somar(1,2);
```

Note que agora nosso código possui dois erros. O primeiro erro é semântico, onde estamos implementando uma interface com o método helloWorld em uma classe criada para o intuito de realizar somas, onde não faria tanto sentido a classe possuir esse método. E o segundo erro é que definimos a implementação da interface em uma classe que não contém o método definido na mesma, devido a isso é gerado um erro fatal pelo interpretador que impossibilita de executar o programa, tendo o seguinte output: `Fatal error: Class Somar contains 1 abstract method and must therefore be declared abstract or implement the remaining methods...`

** Implementação de duas interfaces:**

Para implementarmos duas ou mais interfaces em uma mesma classe usaremos uma vírgula `,` para separarmos elas:

```php
  // criamos a interface Nome e definimos os métodos para ela:
    interface Nome 
    {
        public function setNome($nome);
        public function getNome();
    }

  // criamos a interface Idade e definimos seu métodos:
    interface Idade 
    {
        public function setIdade($idade);
        public function getIdade();
    }

  // criamos a classe Pessoa e definimos que ela deverá conter os métodos definidos nas interfaces Nome e Idade:
    class Pessoa implements Nome, Idade 
    {
        private $nome;
        private $idade;
        
        public function getNome()
        {
            return $this->nome;
        }

        public function setNome($nome)
        {
            $this->nome = $nome;
        }

        public function getIdade()
        {
            return $this->idade;
        }

        public function setIdade($idade)
        {
            $this->idade = $idade;
        }

        public static function apresentarPessoa($pessoa)
        {
            echo "Olá, eu me chamo {$pessoa->getNome()} e tenho {$pessoa->getIdade()} anos.";
        }
    }

  // instanciamos um novo objeto através da classe Pessoa:
    $novaPessoa = new Pessoa();
  // atribuimos valores aos seus atributos com os setters:
    $novaPessoa->setNome('João');
    $novaPessoa->setIdade(36);
  // acessamos e executamos o método estático para apresentação de pessoas:
    Pessoa::apresentarPessoa($novaPessoa);
```

A execução do código acima irá gerar o seguinte output: `Olá, eu me chamo João e tenho 36 anos.`

- **Implementação interfaces estendíveis:**

Interfaces estendíveis são interfaces que recebem métodos por herança de outra através do operador `extends` (usado também em heranças de classes), veja um exemplo:

```php
  // definimos a interface CalculosBasicos e seus métodos:
    interface CalculosBasicos
    {
        public function somar($n1, $n2);
        public function subtrair($n1, $n2);
    }

  // definimos a interface Matematica, seu métodos e que ela será um interface estendida de CalculosBasicos,
  // a partir de agora a classe que implementar Matematica deverá possuir tanto métodos definidos na própria
  // interface, quanto métodos definidos em Calculos Basicos;
    interface Matematica extends CalculosBasicos
    {
        public function calcularHipotenusa($cateto1, $cateto2);
    }

  // definimos uma classe Matematico que implementa a interface estendível Matematica:
    class Matematico implements Matematica
    {
        public function somar($n1, $n2)
        {
            return $n1 + $n2;
        }

        public function subtrair($n1, $n2)
        {
            return $n1 - $n2;
        }

        public function calcularHipotenusa($cateto1, $cateto2)
        {
          // calculamos a hipotenusa e devolvemos seu valor
            $hipotenusa = ($cateto1**2 + $cateto2**2)**0.5;
            return $hipotenusa;
        }
    }
  
  // instanciamos um objeto e acessamos seu atributos
    $professor = new Matematico();
    echo $professor->somar(2,4)."-"; // 6
    echo $professor->subtrair(12, 10)."-"; // 2
  // usamos o método number_format para mostrar apenas 2 casas decimais do resultado
    echo number_format($professor->calcularHipotenusa(12, 15), 2); // 19.21

```

Ao rodar o código acima, deverá sair o seguinte output: `6-2-19.21`.

- **Usando constantes em interfaces:**

Apesar de não ser possível definir atributos para uma classe através de uma interface, o PHP permite a criação de constantes nessas estruturas, e caso essa constante não seja redeclarado, classes que implementarem essa interface também vão conseguir acessar essa constante, exemplo:

```php
  interface Exemplo 
  {
    const testando = 'Valor em Exemplo';
  }

  echo Exemplo::testando.' - ';

  class ClasseTeste implements Exemplo
  {
    // ...
  }

  echo ClasseTeste::testando;
```

O código acima terá o output: `Valor em Exemplo - Valor em Exemplo`.

# 31 Funções / Métodos

Quando falamos em funções para pessoas que não são programadoras, com toda certeza a primeira coisa que vem na cabeça são aquelas contas super difíceis de se aplicar da matemática onde são usadas variáveis e nunca retornam um resultado legível para as pessoas que não entendem do assunto, certo?

Bom, é isso que eu penso e até entender o que era de fato, foi sempre isso aí. E agora vou te ajudar a desmistificar essa maravilha da programação, então vem comigo.

## 31.1 O que é uma função?

Em poucas palavras: **Função é um bloco de código reutilizável** onde você pode atrelar uma responsabilidade única.

Ficou confuso? Vamos entender sobre o que é preciso pra se escrever uma função:

- Palavra reservada **function**;
- Um nome para a função (como se fosse uma variável);
- Parâmetros (opcional);
- Um bloco de código.

Com isso ai podemos escrever uma função bem simples e começar a entender a metodologia da coisa toda.

## 31.2 Escrevendo a primeira função

Vamos escrever uma função simples e analisar os elementos citados acima no bloco abaixo.

```php
function recepcionar ($nomePessoa)
{
    echo 'Olá ' . $nomePessoa;
}

recepcionar('danielhe4rt');
```

Olhando bem por cima, podemos ver os pontos citados porém vamos listar pra ficar o mais claro possível:

- Palavra reservada function;
- Nome da função (recepcionar);
- Parâmetros: $nomePessoa (opcionais);
- Bloco de código {tudo que estiver entre as chaves}.

Para executar uma função, basta digitar o seu nome e adicionar os parâmetros caso tenha e tá pronto a funçãozinha!

Vamos ver o exemplo acima em funcionamento:

```txt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/4-Intermediario/exemplos$ php funcoes0.php
Olá danielhe4rt
```

## 31.3 Nomes de funções

Ao criar uma função, assim como uma variável ela deve ser objetiva no que ela deve fazer para que você não se perca em algum momento durante o desenvolvimento.

Pra isso, temos que evitar nomes de funções:

- resposta()
- essecodigotaumamerda()
- fgts()
- fixaBug()

Sim, coisas como essa realmente acontecem em cenários reais e você tem o DEVER de seguir um padrão de desenvolvimento pra ajudar tanto a você que está trabalhando no projeto quanto as próximas pessoas que forem mexer no seu código.

Tá, mas como podemos padronizar essas funções? Vamos falar primeiro sobre convenções de nomenclatura como **PascalCase, snake_case e camelCase**.

### 31.3.1 PascalCase

PascalCase se trata de capitalizar todas as primeiras letras de palavras que você for colocar em algum nome, removendo os espaços. Vamos entender escrevendo algumas funções abaixo:

```php
function RecepcionarUsuario()
{
}

function AlterarUsuario()
{
}

function DeletarUsuarioAutenticado()
{
}
```

Essa padronização é bastante usada, porém não é a recomendação para escrita de funções e sim para classes.

### 31.3.2 snake_case

O snake_case consiste em escrever a variável sem capitalização e separando as palavras por **"_"**.

Exemplos:

```php
function recepcionar_usuario()
{
}

function alterar_usuario()
{
}

function deletar_usuario_autenticado()
{
}
```

Esta padronização, já foi mais popular no passado, mas provavelmente em sua jornada como programador PHP, irá se deparar com diversas vezes com este padrão, visto que temos ainda grandes ecossistemas como Wordpress que o utiliza como o seu padrão. Dentro da linguagem ainda há DIVERSAS, funções nativas utilizando este padrão, segue um breve exemplo:

```php
 preg_replace("(\w+)", "He4rth Developers", "Devs");
 is_int(10);
```

O snake_case, deve ser utilizado para variáveis e funções. Deve se tomar cuidado para não misturá-lo, com outras padronizações.
### 31.3.3 camelCase

Esse é o padrão usado pela comunidade em quesito de funções, sendo ela escrita com a primeira palavra sem capitalização e seguindo das próximas com capitalização.

Vamos pros exemplos:

```php
function recepcionarUsuario()
{
}

function alterarUsuario()
{
}

function deletarUsuarioAutenticado()
{
}
```

Como padrão de comunidade, camelCase deve ser seguido à risca para criação de funções e é extremamente importante para padronização de código dentro de empresas. Logo, isso vai ser usado em um cenário real e seria bom você já estar acostumado/preparado.

PS: seria muito interessante também você padronizar nomes de funções/variáveis em **inglês** e já ir se acostumando com esse tipo de nome de função.

## 31.4 Parametrização

Parâmetros são váriaveis que deixam sua função flexível para o seu uso. Eles são opcionais, porém é quase certeza que você vai usar funções parametrizadas e vamos entender um pouco sobre.

Pense no parâmetro como uma entrada dentro de uma variável que sua função irá receber e processar, tal como nossa primeira função **recepcionar()** que recebe o parâmetro **$nomePessoa** e printa ela na tela junto com mais algumas coisas.

**Parâmetro com valor Padrão**

```php
function greetings($name)
{
    echo "Hello " . $name;
}

greetings('DanielHe4rt');
```

Caso eu não passe nenhum parâmetro dentro da chamada de **greetings()** ele irá dar erro e dizer que é algo **necessário** para que a aplicação continue sendo executada. Pra evitar que algo do tipo aconteça caso for um parâmetro que possa ser opcional, você deve atribuir um valor inicial sendo **$name = "danielhe4rt"**.

Olha o exemplo abaixo:

```php
function greetings($name = 'danielhe4rt')
{
    echo 'Hello ' . $name;
}

greetings();
```

```txt
danielhe4rt@he4rt:~/dev/he4rt/php4noobs/4-Intermediario/exemplos$ php funcoes1.php
Hello danielhe4rt
```

Executando o código podemos que não houve um valor passado pelo usuário e ele simplesmente consumiu o que estava por padrão. Lembre-se de usar parâmetros opcionais apenas quando você tiver a EXTREMA CERTEZA que eles podem ser opcionais para não bugar nenhuma aplicação em produção.

Tipagem de parâmetros
Vamos falar sobre o assunto que toda comunidade de desenvolvedores aborda quando o assunto é PHP: tipagem.

O PHP não te obriga a colocar os tipos de dados que devem ser usados em funções, porém à partir da versão 7 eles deram essa opção de tipagem.

Quando falamos em tipagem, pensamos logo em linguagens altamente tipadas como Java, C, C# etc. Essas linguagens te pedem que você declare as variáveis já com algum tipo pré-definido. Já no PHP vocẽ só coloca um $ e um nome e pronto.

Agora vamos entender os tipos que você pode usar nas funções, sendo eles: string, int, bool, array, float e classes.

Vamos pros exemplos e esclarecer essa bagunça acima:

```php
function greetings(string $name, bool $welcome = false)
{
    if ($welcome) {
        echo 'Hello ' . $name;
    } else {
        echo 'Get the fuck out of here ' . $name;
    }

}

greetings('DanielHe4rt', true);
```

No exemplo, foram usadas duas variáveis com seus respectivos tipos atribuidos, sendo:

- `$name` - uma String;
- `$welcome` - um Booleano;

Agora que você atribuiu tipos, você sabe exatamente o que essa função espera que você envie e o seu desenvolvimento vai ser mais semântico e legível tanto por você quando para outras pessoas.

O que eu pensava sobre isso:

"...mas sou eu que estou desenvolvendo, eu sei o que isso significa".

Hoje eu entendo que código não é escrito apenas para um compilador/interpretador mas sim para outros desenvolvedores que irão dar manutenção em algum momento no seu código.

## 31.5 Funções Anônimas

[Documentação](https://www.php.net/manual/pt_BR/functions.anonymous.php)

No PHP, também podemos criar função sem nome especifico, elas normalmente são utilizadas, como [**callback**](https://github.com/danielhe4rt/php4noobs/blob/master/99-Functions/1-Funcoes.md###callbacks) de alguma outra ação.

É Importante saber, que as funções anônimas, enxergaram apenas escopo próprio, e não herdam automaticamente o escopo anterior, por este motivo não se deve utilizar `$this` ou `globals` por exemplo, para realizar alguma ação dentro da função.

Mas afinal, como vamos utilizar no dia a dia, para a sua utilização como callback, como citado anteriormente , vamos utilizar de exemplo a sua utilização na função `array_filter()` :

```php
// Buscando e criando um novo vetor(array) apenas com números, pares entre 1,2,3,4.
$numerosPares = array_filter([1,2,3,4], function($numero)
{
    return $numero % 2 == 0;
}); // Resultado: [2,4]
```

Támbem pode-se atribuir uma função anônima, a uma variavel, como:

```php
$funcaoExemplo = function($nome)
{
printf("Melhor grupo de desenvolvedores é a: %s\r\n", $nome);
};

$funcaoExemplo('He4rtDevs'); //Resultado:  O Melhor grupo de desenvolvedores é a He4rtDevs
```

Para a função utilizar alguma variavel do escopo anterior, é necessário passar o complemento `use()`, como o exemplo a seguir:

```php
$mensagem = "He4rtDevs";
$exemplo = function () use ($mensagem)
{
    echo $mensagem;
};
$exemplo(); // Resultado: He4rtDevs
```

**Callbacks**

Bom com alguns conceitos explicados, pode ter ficado com um nó na cabeça, mas afinal o que é um **CALLBACK**?

Resumidamente, é um nome para uma função, que vai ser passada como paramêtro dentro de outra função, ou seja, para que ela seja executada é necessário que a função a qual ela pertence seja chamada, calma... Vamos aos exemplos.

Primeiramente, vamos tentar algo mais simples, por exemplo podemos passar uma função da propria linguagem para execução de uma tarefa:

```php
    array_map('trim',['  oi tudo bem ? ', ' Como vai você?', 'Beleza ?  ']); 
  - // Resultado: ['oi tudo bem?', 'Como vai você ?', 'Beleza ?']
```

Bom, explicando de uma maneira, mais declarativa, podemos interpretar, como quando sua mãe fala explicitamente para você: - "Filho, por favor lave a louça para mim, enquanto vou ao mercado. Se fizer lhe dou um doce. Se não, vou te colocar de castigo."

```php
function pedirParaLavarLouca($filho, $callback)
{
    $resultado = lavouLouca();

    if($resultado === true) {
        echo $callback('pirulito', null);  // Resultado: Ebaaa Joãozinho, ganhou um pirulito.
    } else {
        echo $callback(null, '1 Semana sem video game'); // Resultado: Que pena! Joãozinho vai ficar 1 Semana sem video game.
    }
}

function lavouLouca()
{
    return true;
}

$filho = 'Joãozinho';
pedirParaLavarLouca($filho, function($doce, $castigo) use ($filho)
{
    if($doce !== null) {
        return "Ebaaa $filho, ganhou um $doce."; 
    } else if($castigo !== null) {
        return "Que pena! $filho vai ficar $castigo.";
    }
});
```

## 31.6 Funções de Exemplo 

Abaixo estão algumas funções usando o que aprendemos até o momento sobre esse tópico.

Soma de dois números:

```php
function twoNumbersSum(int $x, int $y)
{
    return $x + $y;
}

$result = twoNumbersSum(5,13);

echo 'Result: ' . $result;
// Result: 18
```

Fake Login

```php
function authenticateUser(string $username, string $password)
{
    $database = [
        'username' => 'danielhe4rt',
        'password' => '5b3097aa10de9db25cebe494beee6c28' // He4rtDevs
    ];

    if ($database['username'] != $username) {
        return 'This user doesnt exists';
    }
    if ($database['password'] != md5($password)) {
        return 'Wrong password';
    }

    return 'Login Successful';
}
```

# 32 Funções de manipulação de String

Nesse tópico, iremos abordar algumas funções importantes para manipulação de string e deixar links úteis para você pesquisar mais sobre caso queira.

## 32.1 strlen

A função **`strlen()`** conta a quantidade de caracteres dentro de uma string.

[Link para documentação](https://www.php.net/manual/pt_BR/function.strlen.php)

Retornos Esperados:

- **Sucesso**: int
- **Erro**: null

Exemplos

Exemplo #1 CountingNameCharacters

```html
$name = 'danielhe4rt';

echo 'O nome tem ' . strlen($name) . ' caracteres';
// Resultado
// O nome tem 11 caracteres
```

## 32.2 str_repeat

A função **`str_repeat()`** repete uma quantidade de vezes uma string que você tenha em mente.

Argumentos/Parâmetros:

- String a ser repetida;
- Quantidade de vezes a ser repetido.

[Link para documentação](https://www.php.net/manual/pt_BR/function.str-repeat.php)

Exemplos

Exemplo #1 Melhor Grupo <3

```php
$string = 'He4rtDevs ';
$qtd = 3;

$repeat = str_repeat($string, $qtd);

echo 'Melhor grupo é claramente ' . $repeat;

// Result
// Melhor grupo é claramente He4rtDevs He4rtDevs He4rtDevs
```

## 32.3 str_replace

A função **`str_replace()`** substitui caracteres de uma string e te retorna uma nova string.

Argumentos/Parâmetros:

- String ou array de parâmetros a serem substituídos;
- String que irá repor os caracteres substituídos;
- String a ser examinada.

[Link para documentação](https://www.php.net/manual/pt_BR/function.str-replace.php)

Exemplos

Exemplo #1 BetterLang

```php
$string = 'JS é a melhor linguagem';

echo str_replace('JS','PHP', $string);
// Resultado:
// PHP é a melhor linguagem
```

Exemplo #2 CursedWords

```php
$string = 'Palavras que devem ser censuradas: Java, BBB, Boninho, BBBot';

echo str_replace(['Java','BBB','BBBot'],'****', $string);

// Resultado:
// Palavras que devem ser censuradas: ****, ****, Boninho, ****
```

Exemplo #3: BetterCursedWords

```php
$string = 'Palavras que devem ser censuradas: Java, BBB, Boninho, BBBot';

$cursedWords = ['Java','BBB','BBBot'];

foreach ($cursedWords as $word) {
    $string = str_replace($word, str_repeat('*', strlen($word)), $string);
}

echo $string;
// Resultado:
// Palavras que devem ser censuradas: ****, ***, Boninho, *****
```

## 32.4 substr

A função **`substr()`** retorna uma parte dos caracteres de uma string, podendo usar parâmetros de início ou início e fim.

O segundo e terceiro parâmetro são identificadores que se baseiam no tamanho da string.

Argumentos/Parâmetros:

- String a ser inspecionada;
- Identificador inicial da string a ser pega;
- Identificador final da string a ser pega;

[Link para documentação](https://www.php.net/manual/pt_BR/function.substr.php)

Exemplos

Exemplo #1 Usando um início negativo

```php
$rest = substr('abcdef', -1);    // retorna "f"
$rest = substr('abcdef', -2);    // retorna "ef"
$rest = substr('abcdef', -3, 1); // retorna "d"
```

Exemplo #2 Usando um length negativo

```php
$rest = substr('abcdef', 0, -1);  // retorna "abcde"
$rest = substr('abcdef', 2, -1);  // retorna "cde"
$rest = substr('abcdef', 4, -4);  // retorna false
$rest = substr('abcdef', -3, -1); // retorna "de"
```

## 32.5 strpos

A função **`strpos()`** retorna a posição numérica da primeira ocorrência do item buscado. A Primeira posição da string é igual á 0, seguindo assim em diante. Como se fosse um vetor (array).

Argumentos/Parâmetros:

- String a ser buscada. (String maior, completa)
- String com o conteúdo que quero buscar.
- (Opcional) Procurar na String a partir da posição x.

Retornos Esperados:

- **Sucesso**: string
- **Erro**: false (boolean)

[Link para documentação](https://www.php.net/manual/pt_BR/function.strpos.php)

Exemplos

Exemplo #1 Procurando por um caractere específico:

```php
    $stringCompleta = 'developers';
    $buscandoPor    = 'e';
    $posicao        = strpos($stringCompleta, $buscandoPor); // retorna 1
```

Exemplo #2 Caso a função não encontre nenhuma ocorrência.

```php
    $stringCompleta = 'developers';
    $buscandoPor    = '4devs';
    $posicao = strpos($stringCompleta, $buscandoPor); // retorna false
```

Exemplo #3 Procurando uma ocorrência, a partir de uma posição:

```php
    $stringCompleta = 'developers';
    $buscandoPor    = 'e';
    $posicaoInicial = 4; // ou seja, buscando a partir de ..."lopers".
    $posicao = strpos($stringCompleta, $buscandoPor, $posicaoInicial); // retorna 7
```

## 32.6 trim

A função **`trim()`** remove espaços adjacentes (do lado esquerdo e direito). Esta função é muito utilizada, para tratar a entrada de dados do usuário.

Argumentos/Parâmetros:

- String a ser limpa.
- Tipo de espaço a ser retirado (Não precisamos, nos preocupar por agora).

Retornos Esperados:

- **Sucesso**: string

[Link para documentação](https://www.php.net/manual/pt_BR/function.trim.php)

Exemplos

Exemplo #1 Espaçamento com espaço.

```php
$string  = '  He4rt Developers ';
trim($string); // retorna He4rt Developers (sem espaços)
```

Exemplo #2 Espaçamento com tab.

```php
$string  = '    He4rt Developers  ';
trim($string,'\t'); // retorna He4rt Developers (sem espaços)
```

Esta função ainda há duas variantes que são o [**`ltrim()`**](https://www.php.net/manual/pt_BR/function.ltrim.php), que retira apenas os espaços ao início (esquerda) da string. O outro é o [**`rtrim()`**](https://www.php.net/manual/pt_BR/function.rtrim.php) que remove o espaço ao final da string.

## 32.7 strtoupper

A função **`strtoupper()`** converte todos os caracteres para maiúsculas. Esta função é muito utilizada, para tratar a entrada de dados do usuário ou destacar uma mensagem, para apresenta-la de forma mais amigável.

Argumentos/Parâmetros:

- String a ser transformada.

Retornos Esperados:

- **Sucesso**: string

[Link para documentação](https://www.php.net/manual/pt_BR/function.strtoupper.php)

Exemplos

Exemplo #1

```php
$string  = 'Developers';
strtoupper($string); // retorna DEVELOPERS
```

## 32.8 strtolower

A função **`strtolower()`** converte todos os caracteres para minúsculo. Esta função é muito utilizada, para tratar a entrada de dados do usuário ou destacar uma mensagem, para apresenta-la de forma mais amigável.

Argumentos/Parâmetros:

- String a ser transformada.

Retornos Esperados:

- **Sucesso**: string

[Link para documentação](https://www.php.net/manual/pt_BR/function.strtolower.php)

Exemplos

Exemplo #1

```php
$string  = 'DEVelopers';
strtolower($string); // retorna developers
```

## 32.9 str_contains

A função **`str_contains()`** Verifica se uma string está contida na outra. Muito utilizada para identificar se neste texto X, há palavra Y ? Argumentos/Parâmetros:

- (string) Palheiro.
- (string) Agulha

Retornos Esperados:

- **Contido**: true
- **Não contido**: false

[Link para documentação](https://www.php.net/manual/pt_BR/function.str-contains.php)

Exemplos

Exemplo #1

```php
$palheiro = 'He4rt devs é o melhor grupo';
$agulha = 'devs';
$contem  = str_contains($palheiro, $agulha); // retorna true
```

Exemplo #2

```php
$string  = 'He4rt devs é o melhor grupo';
$buscandoPor = 'developers';
$contem = str_contains($stringCompleta, $buscandoPor); // retorna false
```

Exemplo #3

Uma String vazia sempre está contida em qualquer string

```php
$string  = 'He4rt devs é o melhor grupo';
$buscandoPor = '';
$contem = str_contains($stringCompleta, $buscandoPor); // retorna true
```

## 32.10 str_starts_with

A função **`str_starts_with()`** Verifica se uma string _COMEÇA_ com outra string. Argumentos/Parâmetros:

- (string) Palheiro.
- (string) Agulha

Retornos Esperados:

- **Contido**: true
- **Não contido**: false

[Link para documentação](https://www.php.net/manual/pt_BR/function.str-starts-with.php)

Exemplos

Exemplo #1

```php
$string = 'He4rt devs é o melhor grupo';
$buscandoPor = 'He4rt';
$contem  = str_starts_with($string, $buscandoPor); // retorna true
```

Exemplo #2

```php
$string  = 'He4rt devs é o melhor grupo';
$buscandoPor = 'devs';
$contem = str_starts_with($stringCompleta, $buscandoPor); // retorna false
```

Exemplo #3

Uma String vazia sempre está contida em qualquer string

```php
$string  = 'He4rt devs é o melhor grupo';
$buscandoPor = '';
$contem = str_starts_with($stringCompleta, $buscandoPor); // retorna true
```

## 32.11 str_ends_with

A função **`str_ends_with()`** Verifica se uma string _TERMINA_ com outra string. Argumentos/Parâmetros:

- (string) Palheiro.
- (string) Agulha

Retornos Esperados:

- **Contido**: true
- **Não contido**: false

[Link para documentação](https://www.php.net/manual/pt_BR/function.str-starts-with.php)

Exemplos

Exemplo #1

```php
$string = 'He4rt devs é o melhor grupo';
$buscandoPor = 'grupo';
$contem  = str_ends_with($string, $buscandoPor); // retorna true
```

Exemplo #2

```php
$string  = 'He4rt devs é o melhor grupo';
$buscandoPor = 'devs';
$contem = str_ends_with($stringCompleta, $buscandoPor); // retorna false
```

Exemplo #3

Uma String vazia sempre está contida em qualquer string

```php
$string  = 'He4rt devs é o melhor grupo';
$buscandoPor = '';
$contem = str_ends_with($stringCompleta, $buscandoPor); // retorna true
```

## 32.12 preg_replace

A função **`preg_replace()`** substitui caracteres de uma string e te retorna uma nova string baseado em um Regex.

Argumentos/Parâmetros:

- String ou array de parâmetros a serem substituídos;
- Regex que irá repor os caracteres substituídos;
- String a ser substituida.

[Link para documentação](https://www.php.net/manual/pt_BR/function.preg-replace.php)

Exemplos

Exemplo #1 Remove Some Word

```php
$string = 'Meu pé está quente';

echo preg_replace('/pé/', '', $string);
// Resultado:
// Meu está quente
```

Exemplo #2 Remove HTML Tags

```php
$string = '<html><div><span>Hello World</span></div></html>';

echo reg_replace('/<[^<>]+>/', '', $string);

// Resultado:
// Hello World
```

Exemplo #3 Remove Special Characters

```php
$string = 'Meu pé está quente';

preg_replace(array("/(á|à|ã|â|ä)/","/(Á|À|Ã|Â|Ä)/","/(é|è|ê|ë)/","/(É|È|Ê|Ë)/","/(í|ì|î|ï)/","/(Í|Ì|Î|Ï)/","/(ó|ò|õ|ô|ö)/","/(Ó|Ò|Õ|Ô|Ö)/","/(ú|ù|û|ü)/","/(Ú|Ù|Û|Ü)/","/(ñ)/","/(Ñ)/"),explode(" ","a A e E i I o O u U n N"), $string);

echo $string;
// Resultado:
// Meu pe esta quente
```

## 32.13 ucfirst

A função **`ucfirst()`** altera a primeira letra da string para maiúscula.

Argumentos/Parâmetros:

- String a ser transformada.

[Link para documentação](https://www.php.net/manual/pt_BR/function.ucfirst)

Exemplos

Exemplo #1

```php
$string  = 'daniel';
ucfirst($string); // retorna Daniel
```

# 33 Funções de manipulações de Arrays

Nesse tópico, iremos abordar algumas funções importantes para manipulação de arrays e deixar links úteis para você pesquisar mais sobre caso queira.

## 33.1 implode

A função **`implode()`** retorna uma string à partir de uma array, juntando todos os vetores em ordem crescente com um delimitador selecionado.

[Link para documentação](https://www.php.net/manual/pt_BR/function.implode)

Exemplos

```php
$array = array('lastname', 'email', 'phone');
$comma_separated = implode(',', $array);

echo $comma_separated; // lastname,email,phone
```

## 33.2 array_push

A função **`array_push()`** insere um novo elemento no final de um array.

Argumentos/Parâmetros:

- Array no qual você quer inserir um novo elemento;
- Novo elemento.

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-push)

Exemplos

Exemplo #1 Melhores Comunidades

```php
$communities = []; // []

array_push($communities, 'He4rtDevs');

print_r($communities); // ['He4rtDevs']

array_push($communities, 'CodigoFalado');

print_r($communities); // ['He4rtDevs', 'CodigoFalado']
```

Exemplo #2 Array de Arrays

```php
$communities = [
    'communities' => [
        'He4rtDevs',
        'CodigoFalado',
        'php.net',
        'TwitchTV'
    ]
];

array_push($communities, ['Links' => ['https://heartdevs.com'] ]);
// Resultado
// $communities = [
//     'communities' => [
//         'He4rtDevs',
//         'CodigoFalado',
//         'php.net',
//         'TwitchTV'
//     ],
//     'links' => [
//         'https://heartdevs.com'
//     ]
// ];


array_push($communities['links'], 'https://codigofalado.com.br');

// Resultado
// $communities = [
//     'communities' => [
//         'He4rtDevs',
//         'CodigoFalado',
//         'php.net',
//         'TwitchTV'
//     ],
//     'links' => [
//         'https://heartdevs.com',
//         'https://codigofalado.com.br',
//     ]
// ];
```

## 33.3 array_search

A função **`array_search()`** procura um elemento dentro do valor e retorna sua chave caso encontrado.

Argumentos/Parâmetros:

- Elemento que você deseja buscar no array;
- Array a ser pesquisado.

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-search)

Exemplos

Exemplo #1 Melhores Comunidades

```php
$communities = ['php.net','CodigoFalado','TwitchTV','He4rtDevs']; // []

$result = array_search('CodigoFalado', $communities); // Return 1
$result = array_search('He4rtDevs', $communities); // Return 3
$result = array_search('foguete roxo', $communities); // Return false
```

## 33.4 array_diff

A função **`array_diff()`** compara um ou mais arrays e retorna os elementos que divergem tendo o primeiro array como referência.

Argumentos/Parâmetros:

- Primeiro array a ser comparado;
- Segundo array a ser comparado;
- N arrays a serem comparados.

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-diff)

Exemplos

Exemplo #1 Cores maneiras

```php
$colorPallete1 = ['yellow', 'pink', 'purple', 'red'];
$colorPallete2 = ['yellow', 'pink', 'brown', 'blue'];

$result = array_diff($colorPallete1, $colorPallete2);
// Result
// [
//    'purple',
//    'red'
// ]
```

Exemplo #2 Cores maneiras 2.0

```php
$colorPallete1 = ['black', 'pink', 'purple', 'red'];
$colorPallete2 = ['yellow', 'pink', 'brown', 'blue'];
$colorPallete3 = ['yellow', 'white', 'brown', 'blue'];

$result = array_diff($colorPallete1, $colorPallete2, $colorPallete3);
// Result
// [
//    'black',
//    'purple',
//    'red'
// ]
```

## 33.5 array_sum

A função **`array_sum()`** soma todos os valores dentro de um array.

Argumentos/Parâmetros:

- Primeiro array a ser comparado.

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-sum.php)

Exemplos

Exemplo #1 Numeros inteiros

```php
$numbers = [1, 5, 3, 4, 7, 1];
$result = array_sum($numbers); // Result 21
```

Exemplo #2 Números flutuantes

```php
$numbers = [1.5, 6, 2, 8.3, 0.3];
$result = array_sum($numbers); // Result 18.1
```

## 33.6 array_replace

A função **`array_replace()`** substitui valores do primeiro array passado usando os próximos como critério de comparação. Os arrays que irão ser passados deverão conter a chave de qual elemento será substituído seguido do seu valor. Os parâmetros após o primeiro são infinitos.

Argumentos/Parâmetros:

- Primeiro array a ser comparado;
- 1o Array com mudanças a serem feitas;
- 2o Array com mudanças a serem feitas.
- ...

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-replace)

Exemplos

Exemplo #1 Números inteiros

```php
$names = ['danielhe4rt', 'geekcom','Loooooogan_','MaeHe4rt'];
$nick1 = [2 => 'Loogan_'];
$nick2 = [2 => 'kjkGustavo', 3 => 'JuhBotelho'];

$result = array_replace($names, $nick1, $nick2);

// Result
// [
//    'danielhe4rt',
//    'geekcom',
//    'kjkGustavo',
//    'JuhBotelho',
// ]
```

## 33.7 array_map

A função **`array_map`** compõe o grupo das excelentes funções de transformação no PHP. Espera 1 callback e 1 ou N arrays como argumento. Pode ser utilizado no lugar de um foreach por exemplo e deixa explicito que um novo array será gerado.

Argumentos/Parâmetros:

- Função que será executada para cada elemento do array (Recebe como parâmetro o elemento que está sendo iterado)
- Array a ser iterado
- ...

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-map)

Exemplos

Exemplo #1 Função nativa

```php
$languages = array_map('strtoupper', ['php', 'elixir', 'clojure']);

// Result
//
// [
//  "PHP",
//  "ELIXIR",
//  "CLOJURE"
// ]
```

Exemplo #2 Função personalizada

```php
$languages = array_map(function($language) {
    return md5(ucfirst($language));
}, ['php', 'elixir', 'clojure']);

// Result
// 
// [
//  "2ec543bde83a1a3ed7eb0676e664a8bc",
//  "a12eb062eca9d1e6c69fcf8b603787c3",
//  "3ce4a9c4043142965234ee0c40cef1d0"
// ]
```

Exemplo #3 Combinação de arrays

```php
$languages = array_map(function($language1, $language2) {
    return sprintf('%s - %s', ucfirst($language1), ucfirst($language2));
}, ['php', 'elixir', 'clojure'], ['haskell', 'c#', 'java']);

// Result
//
// [
//  "Php - Haskell",
//  "Elixir - C#",
//  "Clojure - Java"
// ]
```

## 33.8 array_filter

Similar à função anterior o **`array_filter`** cria um novo array mas dessa vez esperando uma condição. É de fato um filtro.

Argumentos/Parâmetros:

- Array a ser iterado
- Função que será executada para cada elemento do array (Recebe como parâmetro o elemento que está sendo iterado)
- ...

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-filter)

Exemplos

Exemplo #1 Retornar somente valores que forem diferente de dada condição

```php
$drinks = array_filter(['tequila', 'vodka', 'whisky'], function($drink){
    return $drink != 'tequila';
});

// Result
//
// [
//  'vodka',
//  'whisky'
// ]
```

Exemplo #2 Retornar somente números (utilizando função nativa como callback)

```php
$numbers = array_filter(['teste', 123456, '123', 0, 'lisp'], 'is_numeric');

// Result
// [
//  123456,
//  123,
//  0
// ]
```

## 33.9 array_reduce

A função **`array_reduce`** reduz um array de N elementos para 1 único elemento. Muito útil para cálculos ou operações que resultam em um único valor

Argumentos/Parâmetros:

- Array a ser iterado
- Função que será executada para cada elemento do array (Recebe uma variável acumuladora e o elemento que está sendo iterado)

[Link para documentação](https://www.php.net/manual/pt_BR/function.array-reduce)

Exemplos

Exemplo #1 Soma de todos os itens de um array

```php
$total = array_reduce([10, 20, 10], function($somatoria, $valor){
    $somatoria += $valor;
    return $somatoria;
});

// Result
//
// 40
```

## 33.10 explode

A função **`explode()`** retorna um array de strings à partir de uma string, separando essa string a partir de uma condição

[Link para documentação](https://www.php.net/manual/pt_BR/function.explode)

Exemplos

Exemplo #1 RandomExample

```php
$string = "Eu gostaria de separar essa string em espaços";
$arraySeparado = explode(' ', $string);

print_r($arraySeparado); // Array ( [0] => Eu [1] => gostaria [2] => de [3] => separar [4] => essa [5] => string [6] => em [7] => espaços )
```

# 34 Funções de manipulação de arquivos

Nesse tópico, iremos abordar algumas funções importantes para manipulação de arquivos e deixar links úteis para você pesquisar mais sobre caso queira.

## 34.1 fopen

A função **fopen()** abre um buffer de arquivo baseado em um **diretório** e **modo** passado por parametros.

Argumentos/Parâmetros:

- Diretório onde você deseja buscar o arquivo;
- Modo de leitura/escrita.

| Modo | Descrição                                                                                                                                                                                                                                                                                    |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 'r'  | Abre somente para leitura; coloca o ponteiro do arquivo no começo do arquivo.                                                                                                                                                                                                                |
| 'r+' | Abre para leitura e escrita; coloca o ponteiro do arquivo no começo do arquivo.                                                                                                                                                                                                              |
| 'w'  | Abre somente para escrita; coloca o ponteiro do arquivo no começo do arquivo e reduz o comprimento do arquivo para zero. Se o arquivo não existir, tenta criá-lo.                                                                                                                            |
| 'w+' | Abre para leitura e escrita; coloca o ponteiro do arquivo no começo do arquivo e reduz o comprimento do arquivo para zero. Se o arquivo não existir, tenta criá-lo.                                                                                                                          |
| 'a'  | Abre somente para escrita; coloca o ponteiro do arquivo no final do arquivo. Se o arquivo não existir, tenta criá-lo.                                                                                                                                                                        |
| 'a+' | Abre para leitura e escrita; coloca o ponteiro do arquivo no final do arquivo. Se o arquivo não existir, tenta criá-lo.                                                                                                                                                                      |
| 'x'  | Cria e abre o arquivo somente para escrita; coloca o ponteiro no começo do arquivo. Se o arquivo já existir, a chamada a fopen() falhará, retornando FALSE e gerando um erro de nível E_WARNING. Se o arquivo não existir, tenta criá-lo. Isto é equivalente a especificar as flags O_EXCL   |
| 'x+' | Cria e abre o arquivo para leitura e escrita; coloca o ponteiro no começo do arquivo. Se o arquivo já existir, a chamada a fopen() falhará, retornando FALSE e gerando um erro de nível E_WARNING. Se o arquivo não existir, tenta criá-lo. Isto é equivalente a especificar as flags O_EXCL |

[Link para documentação](https://www.php.net/manual/pt_BR/function.fopen)

Exemplos

Exemplo #1 Abrindo um arquivo (?)

```php
// test.txt (vazio)
$directory = "test.txt";
$file = fopen($directory, "a+");
// Result: buffer ativo com o seu arquivo para ser escrito é isso nd d+
```

## 34.2 fclose

A função **fclose()** fecha um buffer de arquivo. Essa função deve ser usada em todo fim de leitura/escrita de arquivos para evitar vazamento de memória (memory leak).

Argumentos/Parâmetros:

- Buffer da função fopen() ou fsockopen();

[Link para documentação](https://www.php.net/manual/pt_BR/function.fclose)

Exemplos

Exemplo #1 Fechando um arquivo (?)

```php
// test.txt (vazio)
$directory = "test.txt";
$buffer = fopen($directory, "a+");
// Result: buffer ativo com o seu arquivo para ser escrito é isso nd d+

fclose($buffer);
// Result: arquivo devidamente finalizado.
```

## 34.3 fwrite

A função **fwrite()** escreve em um buffer de algum arquivo passado como parâmetro.

Argumentos/Parâmetros:

- Buffer da função fopen() ou fsockopen();
- String a ser escrita.

[Link para documentação](https://www.php.net/manual/pt_BR/function.fwrite)

Exemplos

Exemplo #1 Abrindo, escrevendo e fechando um arquivo (?)

```php
// test.txt (vazio)
$directory = "test.txt";
$string = "He4rtDevs melhor grupo!";
$buffer = fopen($directory, "a+");
// Result: buffer ativo com o seu arquivo para ser escrito é isso nd d+

fwrite($buffer, $string);
// test.txt:
// He4rtDevs melhor grupo!

fwrite($buffer, "To falando sério");
// test.txt:
// He4rtDevs melhor grupo!
// To falando sério

fclose($buffer);
// Result: arquivo devidamente finalizado.
```

## 34.4 feof

A função **feof()** checa se o buffer aberto está na última linha do arquivo, se existir uma próxima linha ele retorna verdadeiro e caso estiver no final ele retorna falso.

Essa função é usada para auxiliar em leitura de arquivos. Em maiores casos serão usados junto com o fread ou algo que mude o ponteiro do arquivo e comumente serão vistos em laços **while**.

Argumentos/Parâmetros:

- Buffer da função fopen() ou fsockopen();

[Link para documentação](https://www.php.net/manual/pt_BR/function.feof)

Exemplos

Exemplo #1 Checando se o arquivo está na última linha

```php
// test.txt (2 linhas)
// Primeira linha do arquivo
// Segunda Linha do arquivo

$fileName = "test.txt";

$buffer = fopen($fileName, 'r');

echo feof($buffer); // Verdadeiro

fclose($buffer);

// Como não há um ponteiro rodando o arquivo (não está sendo lido)
// ele sempre irá retornar verdadeiro, pois existem duas linhas.
// CASO o ponteiro seja mudado pra segunda linha, ele retornaria false
// pois o arquivo tem apenas duas linhas.
```

## 34.5 fread

A função **fread()** lê uma quantidade de bytes em uma linha do arquivo aberto pelo buffer (fopen).

A leitura é interrompida caso uma das condições abaixo seja atingida.

```txt
1. A quantidade de bytes informados como parâmetro são lidos;
2. Quando o final do arquivo  (EOF - end of file - final do arquivo) é alcançado;
3. um pacote tornou-se disponível (para network streams);
4. 8192 bytes (ou a quantidade de bytes necessárias pro que você irá ler) foram lidos (depois de abrir um stream).
```

Argumentos/Parâmetros:

- Buffer da função fopen() ou fsockopen();
- A quantidade de bytes a serem lidos (caso não tenha ideia, coloque por padrão 8192).

[Link para documentação](https://www.php.net/manual/pt_BR/function.fwrite)

Exemplos

Exemplo #1 Deixa o Prime

```php
// test.txt (2 linhas)
// He4rtDevs melhor grupo do mundo .........
// Entre no meu canal e

$buffer = fopen("test.txt","r");

while(!feof($buffer)){
	echo fread($buffer, 8192) . " deixa o prime";
}

fclose($buffer);

// Result:
// He4rtDevs melhor grupo do mundo ......... deixa o prime
// Entre no meu canal e deixa o prime
```
