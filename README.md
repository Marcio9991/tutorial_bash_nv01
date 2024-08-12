# Tutorial Bash - nível iniciante  

![*Tux, the Linux penguin*](imagens/tux.png)  

## Introdução  

Este tutorial é um jogo caça-letras para ajudar usuários iniciantes em Linux a se familiarizarem com a _Command Line Interface_ (CLI), ou **[shell](https://pt.wikipedia.org/wiki/Shell_(computa%C3%A7%C3%A3o))**, mais especificamente com o **[bash](https://pt.wikipedia.org/wiki/Bash)**, um interpretador de comandos shell.  

Este tutorial é uma adaptação do tutorial **[bash_tutorial](https://github.com/krother/bash_tutorial)** de Kristian Rother.  

### Para quem é este tutorial?  

Para todos que tem pouca ou nenhuma experiência com o **bash**  

### O que você alcançará ao completar este tutorial?  

Conhecimento sobre comandos para:  

* Navegar entre diretórios  
* Criar e manipular arquivos de texto  
* Baixar arquivos da internet  
* Compactar e descompactar arquivos  
* Executar scripts  
* Argumentos e parâmetros dos comandos  

### Pré-requesitos  

Este tutorial foi elaborado e implementado em uma Distribuição Linux baseado em Debian. Desta forma, espera-se que qualquer [distribuição baseada em Debian](https://distrowatch.com/search.php?ostype=Linux&basedon=Debian) seja o suficiente para completá-lo.

## Objetivo  

Você deverá encontrar os 23 caracteres escondidos neste repositório utilizando vários comandos **shell**. Estes caracteres formam uma frase com duas palavras e um espaço em branco entre elas.  

![*disposição dos 23 caracteres*](imagens/caca_letras.png)


## Preparação inicial

Em uma máquina com uma distribuição Linux, abra o terminal. Muito provavelmente você estará no diretório de trabalho chamado de _home do usuário_, indicado pela linha:  
``` {.sourceCode .bash}
<usuário>@<máquina>:~$
```

O termo **<usuário\>** é o nome do usuário logado no momento. Em computadores de escolas, normalmente os técnicos de informática escolhem **aluno**, **usuário** ou qualquer outro **nome genérico**, mas se você estiver em um computador seu ou da sua família, este nome deve ser um nome reconhecido por você.  

Na sequência, o termo **<máquina\>** é o nome do computador que você está usando, podendo ser nomes bem variados e criativos.

Para a coerência deste jogo, toda vez que for necessário apresentar a linha de comando completa, será usado estes dois termos genéricos **<usuário\>** e **<máquina\>**.

para garantir que você está no diretório _home do usuário_ entre com o seu primeiro comando:  
Observação 1: para executar um comando, digite-o e pressione **ENTER**
``` {.sourceCode .bash}
usuário@máquina:~$ pwd # pressione ENTER
```  
Deverá ser apresentado a seguinte resposta:
``` {.sourceCode .bash}
/home/usuário
```

Observação 2: em alguns momento será necessário adicionar um ou outro comentário, desta forma, o caractere **#** será utilizado, portanto, tudo o que estiver à direita do **#** é um comentário e não deve ser entrado no terminal

Após verificado estas condições inicias, vamos começar nossa caçada às letras.

## 1. Baixar arquivo da internet e Descompactá-lo  

### 1.1 Baixar o arquivo tutorial_bash_nv01.zip

Vamos baixar a estrutura de diretórios e arquivos deste repositório utilizando o comando **wget**.  
Este comando é um _downloader_ que aceita como argumento uma [URI](https://pt.wikipedia.org/wiki/URL). Neste caso, como desejamos baixar a estrutura de diretórios do nosso repositório, usaremos a URI do arquivo compactado como este argumento. Desta forma, no terminal, entre com o seguinte comando:
``` {.sourceCode .bash}
wget https://github.com/bellorini/tutorial_bash_nv01/archive/refs/heads/tutorial_bash_nv01.zip
```

TODO, apresentar texto de completado após completar a construção deste tutorial  

O arquivo baixado chama-se **tutorial_bash_nv01.zip**. Para verificar se este arquivo foi baixado, use o comando **ls**.  
Este comando lista o conteúdo de um diretório.
``` {.sourceCode .bash}
usuário@máquina:~$ ls
```  

É possível que apareçam muitos outros arquivos, porém, o arquivo **tutorial_bash_nv01.zip** deve estar presente.

### 1.2 Descompactar o arquivo tutorial_bash_nv01.zip  

O arquivo baixado está no formato [zip](https://pt.wikipedia.org/wiki/ZIP). Estes arquivos agrupam (empacotam) e compactam outros arquivos.  

O comando **unzip** é utilizado para, entre outras coisas, listar o conteúdo de um arquivo compactado e descompactar este pacote.  
Inicialmente, vamos listar o conteúdo do pacote **tutorial_bash_nv01.zip** com a seguinte linha de comando:
``` {.sourceCode .bash}
usuário@máquina:~$ unzip -l tutorial_bash_nv01.zip
```  

Será apresentado uma tabela com uma estrutura de diretórios e arquivos, contendo tamanho, data e nome.

A partir deste momento, o dispositivo mouse não deve ser mais necessário, desta forma, __mãos ao teclado__!  
![teclado sim, mouse não](imagens/keymouse.png)  

Observe que o comando **unzip** recebeu um parâmetro **-l** e um argumento **tutorial_bash_nv01.zip**. Mas o que são argumentos e parâmetros?  

* **argumento(s)** são modificadores do comando que alteram a funcionalidade deste. No nosso exemplo, o comando **unzip** apenas lista o conteúdo do pacote sem qualquer outro resultado, como descompactar ou alterá-lo. 
* **parâmetro(s)** são modificadores do comando que indicam os objetos de entrada e/ou saída da funcionalidade executada. Neste caso, o pacote **tutorial_bash_nv01.zip** é o nosso objeto que será listado.  

Agora, para descompactar o pacote **tutorial_bash_nv01.zip** basta entrar com o comando:
``` {.sourceCode .bash}
usuário@máquina:~$ unzip tutorial_bash_nv01.zip
```  

Deverá ser criado um novo diretório chamado **tutorial_bash_nv01** dentro do seu diretório __home__. Para verificar, vamos usar o comando **ls** já conhecido, porém adicionando o argumento **tutorial_** e pressione a tecla **TAB** para autocompletar (o terminal é esperto o suficiente para autocompletar)
``` {.sourceCode .bash}
usuário@máquina:~$ ls tutorial_ #TAB (autocompleta com "bash_nv01")
# resultado após pressionar TAB: 
usuário@máquina:~$ ls tutorial_bash_nv01
```  

## 2. Navegação entre diretórios

Rumo ao primeiro caractere!

### 2.1 Alterar o diretório atual de trabalho












