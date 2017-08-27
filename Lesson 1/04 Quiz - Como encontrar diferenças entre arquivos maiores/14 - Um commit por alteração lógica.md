# Um commit por alteração lógica

## Com que frequência confirmar?

Como você pode escolher quando fazer um commit, talvez esteja se perguntando com que frequência confirmar suas alterações. Em geral, é uma boa ideia limitar a quantidade de commits. Conforme o diff entre duas versões aumenta de tamanho, ele fica mais difícil de entender e menos útil. No entanto, você não quer limitar tanto seus commits. Se você sempre salvar um commit a cada vez que alterar uma linha de código, seu histórico será mais difícil de ler, pois terá um grande número de commits durante um período curto.

Uma boa regra prática é fazer um commit por alteração lógica. Por exemplo, se você corrigiu um erro de digitação, depois corrigiu um bug em uma parte separada do arquivo, deve usar um commit para cada alteração, pois eles estão logicamente separados. Se você fizer isso, cada commit terá um propósito que poderá ser facilmente entendido. O Git permite a você escrever uma mensagem curta explicando o que mudou em cada commit, e essa mensagem será mais útil se cada commit tiver uma única alteração lógica.


## Teste sobre o tamanho do commit
Para praticar um pouco a avaliação da frequência de execução de commits, na próxima tela, marque se você acha que os tamanhos a seguir seriam bons tamanhos de commit. Caso contrário, indique se você acha que esse commit é muito pequeno e gostaria de esperar e fazer o commit depois, ou se você acha que é muito grande deveria ter feito o commit antes. Isso é subjetivo, portanto, não há respostas certas ou erradas definitivas, apenas escolha a resposta que você acha melhor em cada caso.
- Faça o commit de todas as alterações necessárias para adicionar um novo recurso, em que você está trabalhando há uma semana. Você não executou commits desde que começou a trabalhar nele.
- Você encontra três erros de digitação no seu README. Você corrige e faz o commit do primeiro.
- Você faz o commit de todas as alterações necessárias para adicionar um novo recurso, em que está trabalhando há uma hora.
- Você corrige dois pequenos bugs em funções diferentes e faz o commit delas ao mesmo tempo.

## Solução de um commit por alteração lógica
### Faça o commit de todas as alterações necessárias para adicionar um novo recurso, em que você está trabalhando há uma semana. Você não executou commits desde que começou a trabalhar nele.
Esse commit parece muito grande. Será mais fácil entender o que cada commit faz se cada um fizer apenas uma coisa e for razoavelmente pequeno. Passar uma semana sem nenhum commit não é a melhor ideia.

### Você encontrou três erros de digitação no seu README. Você corrige e faz o commit do primeiro.
Esse commit parece muito pequeno. Seria melhor corrigir todos os três erros de digitação e depois executar o commit. Dessa forma, seu histórico não ficará muito poluído com erros de digitação. Além disso, você não precisa se preocupar em introduzir bugs em um README, por isso, reunir as alterações em um pacote provavelmente é uma boa ideia.

### Você faz o commit de todas as alterações necessárias para adicionar um novo recurso, em que está trabalhando há uma hora.
Provavelmente, esse é um bom tamanho para um commit. Todo o trabalho é realizado em um único recurso, portanto, o commit terá um objetivo lógico claro. Depois de uma hora, o diff provavelmente terá uma quantidade razoável de conteúdo, mas não muito para entender.
Por outro lado, às vezes, depois de trabalhar por uma hora, você passou por mais de um ponto natural de commit. Nesse caso, vai querer dividir o recurso em commits menores. Por causa disso, \"muito grande\" também pode ser uma resposta razoável aqui.

### Você corrige dois pequenos bugs em funções diferentes e faz o commit delas ao mesmo tempo.
Esse commit provavelmente é muito grande. Teria sido melhor executar o commit depois da correção do primeiro bug, pois as duas correções de bugs não estão relacionadas.

# Quiz: Um commit por alteração lógica
## O que é um README?
Muitos projetos contêm um arquivo chamado \"README\" que fornece uma descrição geral do que o projeto faz e como usá-lo. Com frequência, é uma boa ideia ler esse arquivo antes de fazer qualquer coisa com o projeto, pois o arquivo recebe esse nome para aumentar a probabilidade de os usuários o lerem.