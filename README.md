# Introdução

    Este guia tem como alvo usuários de Linux, mais especificamente Ubuntu, uma vez que este é o SO que estou utilizando e este guia está sendo feito para reforçar meu aprendizado.

Primeiramente, cheque se você possui Git instalado na sua máquina por meio do comando:

    git --version
Se não estiver instalado, basta executar os comandos:
    
    sudo apt update
    sudo apt install git

## Comandos
### git clone
Cria uma pasta na sua máquina com os conteúdos presentes em um repositório do Github.

    Exemplo:
    git clone git@github.com:niicao/Github-Classes.git

Irá clonar este repositório para a sua máquina :)

### git add
Este comando serve para registrar no Git todas as mudanças que foram feitas no repositório, tais como arquivos alterados e arquivos novos.

Normalmente se usa:
    
    git add .
Isso fará com que o comando registre todas as alterações que não foram registradas ainda.

