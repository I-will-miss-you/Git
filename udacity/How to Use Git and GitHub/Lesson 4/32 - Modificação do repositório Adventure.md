## Bifurcar o repositório e clonar sua bifurcação

Agora que você já aprendeu a bifurcar um repositório, efetue push das alterações para a bifurcação e efetue uma requisição pull. Você estará pronto para contribuir com a história create-your-own-adventure que você viu no início da lição. Para isso, primeiro bifurque este repositório. Em seguida, clone sua bifurcação e faça um branch para efetuar suas alterações.

### Observação: 

Você pode fazer suas alterações diretamente no branch master na sua bifurcação, mas ao contribuir com um repositório público, é uma prática padrão fazer as alterações em um branch que não seja master dentro da bifurcação. Dessa forma, você pode facilmente manter seu branch master atualizado com o master do repositório original e mesclar as alterações do master em seu branch quando estiver pronto.

### Observação para usuários do Windows: 

A história cresceu tanto que excede o limite de tamanho do caminho do Windows. Se você encontrar um erro ao clonar, poderá solucionar isso modificando uma configuração definida. Execute este comando no git bash: git config --system core.longpaths true.

## Fazer uma alteração na história

Faça uma alteração real na história. Para obter instruções sobre como fazê-lo, leia o README no repositório create-your-own-adventure.

## Efetuar uma requisição pull

Você deve efetuar uma requisição pull contendo suas alterações no repositório original. Para fazer isso, clique no botão \"pull request\" do seu branch como você já fez antes, mas nesse momento, deixe o repositório original como base.

## Solicitar a mesclagem da requisição pull

Você não tem permissão para modificar esse repositório; então, precisa de alguém na Udacity para mesclar sua requisição pull. Nossa prestativa Casey talvez consiga mesclar sua requisição pull automaticamente. Para que sua requisição pull seja mesclada automaticamente, você precisará seguir as diretrizes no README do repositório e, além disso, você não poderá excluir nem modificar as linhas. Essa restrição sobre exclusões é porque Casey não quer mesclar uma solicitação que exclua acidentalmente parte da história e que ela não consiga diferenciar entre uma exclusão acidental e uma modificação intencional. Para solicitar uma mesclagem automática, deixe um comentário na requisição pull contendo \"@casey-collab\". Por exemplo \"Revise isto, @casey-collab\". Deixe o comentário na guia \"Conversation\" da requisição pull, não na guia \"Files changed\".

Há algumas requisições pull válidas que Casey não poderá mesclar. Por exemplo, ela não aceitará uma requisição pull que corrija um erro ortográfico, uma vez que isso modifica uma linha. Se quiser fazer uma requisição pull que Casey não consiga mesclar, fique à vontade para fazer isso, e alguém da Udacity mesclará a requisição pull se tivermos tempo. No entanto, não conseguimos garantir uma resposta a essas requisições pull.
Caso necessário, atualize sua requisição pull

Se alguém mesclar sua requisição pull ou deixar um comentário, o GitHub enviará um email e o informará. Se for solicitado que você faça algumas alterações, efetue push dessas alterações para sua bifurcação para atualizar a requisição pull. Deixe claro para o revisor que ele deve verificar novamente!