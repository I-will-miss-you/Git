# Git e Github para iniciantes

## Configuração inicial do Git

### Configurações inicias
```sh
git config --global user.name "Code36u4r60"
git config --global user.mail "code36u4r60@hotmail.com"
git config --global core.editor code
```

### Para saber as configurações:
> Para saber o user name
```sh
git config user.name
```
> Para saber o mail
```sh
git config user.mail
```
> Para ter acesso a lista com todas as configurações
```sh
git config --list
```

## Criar um repositorio
1. Criar um Diretório
```sh
mkdir nome_do_diretorio
```
2. Entrar no Arquivo
```sh
cd nome_do_diretorio
```
3. Iniciar o Repositóriop Git
```sh
git init
```

## O ciclo de vida dos status dos Arquivos

### [File Status Lifecycle](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository)
![File Status Lifecycle](lifecycle.png "File Status Lifecycle")

> Saber o [__status__](https://git-scm.com/docs/git-status) do repositório Git
```sh
git status
```

> Criar um arquivo  
> _Exemplo usando o VSCode no win10:_
```sh
code Readme.md
```

> Se voltar a verificar o [__status__](https://git-scm.com/docs/git-status) vai verificar que houve alterações
```sh
git status
```
> [__git-add__](https://git-scm.com/docs/git-add) - Adicionar o conteúdo do arquivo para o índice
```sh
git add Readme.md
```

> [__git-commit__](https://git-scm.com/docs/git-commit) - Gravar alterações no repositório
```sh
git commit -m "Add Readme.md"
```

> [__commit -am] Add + Commit (se o ficheiro já existir no repositório)
```sh
git commit -am "new Commit"
```

## Visualização de logs
### git-log
> [__git-log__](https://git-scm.com/docs/git-log) - Show commit logs
```sh
git log
```

> __--decorate[=short|full|auto|no]__ - permite obter mais informações. O default é _short_
```sh
git log --decorate
```

> __--author=<pattern>__ - pesquisa por autor
```sh
git log --author="nome_autor"
```
> __--graph__ - mostra o registo log de forma gráfica
```sh
git log --graph
``` 

### git-shortlog
> [__git-shortlog__](https://git-scm.com/docs/git-shortlog) - Summarize git log output, mostra todas os contribuintes do repositório.   
> Para cada elemento informa, quantos commits foram feitos e quais.
```sh
git shortlog
```

> __sn__ (--summary  and --numbered) - retorna todos os colaboradores e quantos commits fizeram.
```sh
git shortlog -sn
```

### git-show
> [__git-show__](https://git-scm.com/docs/git-show) - Show various types of objects.
```sh
git show commitKey
# exemplo:
git show 1ac64b4354480387f00a1f1b5c464f94582508d1
```

## Git Diff
>[__git-diff__](https://git-scm.com/docs/git-diff) - Mostrar mudanças entre os commits, commit e working tree, etc  
> Ver a modificações efetuadas nos arquivos.
```sh
git diff
```

> Saber quais arquivos sofreram alterações
```sh
git diff --name-only
```

## "Resetar" erros, voltar a um ponto anterior no trabalho.
>[git-checkout](https://git-scm.com/docs/git-checkout) - Alternar ramos ou restaurar arquivos da estrutura de trabalho.

> Retornar a estado anterior da edição / alteração do arquivo
```sh
git checkout nome_do_arquivo
```

>[__git-reset__](https://git-scm.com/docs/git-reset) - Reset current HEAD to the specified state

> Retornar ao ponto anterior depois do _git add_
```sh
git reset HEAD nome_do_arquivo
```

> Retornar ao estado anterior após o _commit_. O __id__ deve ser o __id__ de "destino"
> ver a diferenças entres __--soft__ , __--mixed__ e __--hard__     
>
> __--soft__ - serve para mudar a mensagem do commit.       
> __--mixed__ - serve para alterar alguma coisa no documento. Pois ele volta ao estado logo antes do "__add__"      
> __--hard__ - serve para descartar todas alterações feitas e voltar ao estado do _commit_ anterior.        
```sh
git reset [soft | mixed | hard] id_commit
# exemplo: 
git reset hard 1e9403fecd9d41ea60b361e3d0479e5e5f21b385
```
 
 ## GitHub
 ### Enviar mudanças para repositório remoto
>[__git-push__](https://git-scm.com/docs/git-push) - Update remote refs along with associated objects
```sh 
git commit -am "mensagem" 
# depois
git push origin master 
```


### Clone de repositório
>[__git-clone__](https://git-scm.com/docs/git-clone) - Clone a repository into a new directory
```sh
git clone https://host.git nome_arquivo
# exemplo:
git clone https://github.com/code36u4r60/Git.git Cursos_Git
```

### Fork do repositório
> é so clicar no botão :)

## BRANCH
>[__git-branch__](https://git-scm.com/docs/git-branch) - List, create, or delete branches

### Criar
> Criar um "_branch_"
```sh
git checkout -b nome_new_brache
```
> Saber quais são os _branchs_ existentes. O _breach_ selecionado fica referenciado com um __*__
```sh
git branch
```

### Mudar e apagar _branchs_

> Mudar de _branch_
```sh
git checkout nome_branch_destino
```
> Apagar um _branch_
```sh
git branch -D nome_branch_para_apagar
```

## Merge
> [__git-merge__](https://git-scm.com/docs/git-merge) - Join two or more development histories together


## Rebase
> [__git-rebase__](https://git-scm.com/docs/git-rebase) - Reapply commits on top of another base tip

## Stash
> [__git-stash__](https://git-scm.com/docs/git-stash) - Stash the changes in a dirty working directory away     
> permite deixar um tarefa em working-progress e criar um _branch_.      
> para isso basta usar: 
```sh
git stash
# para voltar 
git stash apply
# para ver a lista de _git-stash's_ 
git stash list
# para apagar todos os _git-stash's_
git stash clear
```

## Git Aliases - atalhos
[__Git Aliases__](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
```sh
# exemplos
git config --global alias.s status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
```

## Versionando com Tags
[__git-tag__](https://git-scm.com/docs/git-tag) - Create, list, delete or verify a tag object signed with GPG
```sh
git commit -am "messagem"

git push origin master

# Criar uma tag para esta alteração
git tag -a 1.0.0 -m "mensagem"

# Saber as tag's criadas
git tag

# Subir a nova tag
git push origin master --tags
```
## Revert
[__git-revert__](https://git-scm.com/docs/git-revert) - Revert some existing commits
```sh
git revert id_commit_que_deu_problema
```

## Apagando tags e branches remotos
```sh

# apagar no local
git tag -d nome_tag

# apagar as do repositório
git push origin :nome_tag
```