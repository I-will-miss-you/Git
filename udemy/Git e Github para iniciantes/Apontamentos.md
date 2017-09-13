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
>[git-push](https://git-scm.com/docs/git-push) - Update remote refs along with associated objects
```sh 
git commit -am "mensagem" 
# depois
git push origin master 
```


### Clone de repositório
>[git-clone](https://git-scm.com/docs/git-clone) - Clone a repository into a new directory
```sh
git clone host@host nome_arquivo
# exemplo:

```