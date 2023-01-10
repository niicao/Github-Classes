# Introdução

Este guia tem como alvo usuários de Linux, mais especificamente Ubuntu, uma vez que este é o SO que estou utilizando e este guia está sendo feito para reforçar meu aprendizado.


Primeiramente, cheque se você possui Git instalado na sua máquina por meio do comando:

    git --version
Se não estiver instalado, basta executar os comandos:
    
    sudo apt update
    sudo apt install git

## Comandos
### `git clone`
Cria uma pasta na sua máquina com os conteúdos presentes em um repositório do Github.

    Exemplo:
    git clone git@github.com:niicao/Github-Classes.git

Irá clonar este repositório para a sua máquina :)

### `git add`
Este comando serve para registrar no Git todas as mudanças que foram feitas no repositório, tais como arquivos alterados e arquivos novos.

Normalmente se usa:
    
    git add .
Isso fará com que o comando registre todas as alterações que não foram registradas ainda.

### `git status`

Retorna no terminal o estado do diretório (pasta) em que você está trabalhando. Te permite visualizar todos os arquivos que estão registrados no Git e quais arquivos foram alterados.

    git status

### `git commit` 
Salva as alterações no seu repositório __local__. Esse comando não salva automaticamente todas as mudanças feitas, para selecionar as mudanças que você deseja que sejam salvas você deve usar o comando `git add`.

#### Flags
* -m `<message>`

Define a mensagem de commit. Essa mensagem serve para que a pessoa que deu commit no repositório dê uma descrição detalhada do que foi alterado por meio desse commit. É recomendando sempre enviar uma mensagem de commit.
* -a

Inclui todos os arquivos alterados no commit. Arquivos que não foram registrados (não passaram por um `git add`) não serão incluidos
* --amend

Substitui o ultimo commit feito com as mudanças e/ou uma nova mensagem de commit. Esse comando só deve ser utilizado em commits que ainda não foram pushados (`git push`).