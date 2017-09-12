# Como clonar e explorar o Repo

## Como clonar um repositório
Para clonar um repositório, execute ``` git clone ``` seguido por um espaço e a URL do repositório.

## URL do Asteroids
Use a seguinte url para clonar o repositório do Asteroids: https://github.com/udacity/asteroids.git

## Saída de ``` git log ```
Para interromper a visualização da saída do ``` git log ```, pressione ``` q ``` (que significa quit).

- exemplos para usar no ``` diff ```
    - commit b83411e908dfd9858090a46486a4d096ac0e7004
    - commit aa902007d3c4f509b6d6229a15a55a35752da4d2

## Como obter uma saída colorida
Para obter uma saída de diff colorida, execute ```git config --global color.ui auto```.

Cópia e colagem da linha de comando.

Para realizar este teste, você vai querer copiar e colar algumas IDs do commit.

### Windows
Para copiar e colar dentro do Git Bash, siga as instruções nesta página.

### Mac
Para copiar e colar dentro do terminal no Mac, use Cmd+C e Cmd+V

### Ubuntu
Para copiar e colar dentro do terminal no Ubuntu, use Ctrl+Shift+C e Ctrl+Shift+V.

## Uso de **git log** e **git diff**
Como um lembrete, a execução de ``` git log ``` mostrará uma lista dos commits recentes com informações sobre eles, incluindo IDs do commit. A execução de git diff seguida por dois IDs do commit comparará as duas versões do código nesses commits. Se precisar relembrar, talvez você queira assistir novamente a este vídeo.

## Inserção de IDs do commit
Se for mais fácil, você poderá inserir os primeiros quatro ou mais caracteres do ID do commit, em vez de colar todo o ID.

## QUIZ resolução:
- Revert Control - commit b0678b161fcf74467ed3a63110557e3d6229cfa6
- Commit Anterior - commit f19cb1b80fe27e938e4d72770ca0a42f25e99ecc
- ``` git diff b0678b161fcf74467ed3a63110557e3d6229cfa6 f19cb1b80fe27e938e4d72770ca0a42f25e99ecc ```
- add --» 4
- delete --» 4

