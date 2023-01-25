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

## Branching
Branch é o nome dado a cada versão diferente de um repositório que está sendo desenvolvido. A branch chamada `master` é a versão principal do seu programa. Quando se trabalha em outra branch, não é possível ver as alterações feitas fora da branch em que você está trabalhando.

### Qual a utilidade de branches?
Quando se está trabalhando em um projeto, especialmente com várias pessoas, é necessário separar o que cada uma está fazendo, para evitar o acúmulo de problemas.

Exemplo: um time está desenvolvendo um aplicativo com múltiplas features, é de extrema importância que cada feature esteja sendo desenvolvida em uma branch para não só organizar o trabalho sendo feito como facilitar a detecção de erros ao longo do projeto.

Também é comum que sejam criadas branches de *hotfix* (correções de emergência) entre um `commit` e outro na master branch.

<!-- ![alt-text](https://github.com/niicao/Github-Classes/blob/main/Imagens/git_diagram.png) -->

## Comandos

### `git branch`
O comando `git branch` vai retornar as branches existentes em um repositório e irá marcar com um asterisco a branch em que você se encontra

    * main
      feature-1
### `git checkout`
Este comando é usado para trocar de branch.
    
    git checkout feature-1
    git branch

Irá retornar

    * feature-1
      main

### Criar uma nova branch
Para criar uma nova branch no repositório nós adicionaremos a flag `-b` no comando `git checkout`

    git checkout -b <nome-da-branch>

