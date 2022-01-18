# Test Driven Development (TDD)
TDD é o desenvolvimento de software orientado a testes. Porém mais que simplesmente testar seu código o TDD é uma filosofia, uma cultura. E foi fortemente adotado e influenciado pelo movimento ágil.

TDD é o desenvolvimento de software orientado a testes, Test Driven Development em inglês. Porém mais do que simplesmente testar seu código, **TDD é uma filosofia, uma cultura**. E foi fortemente adotado e influenciado pelo movimento ágil.

De acordo com Kent Beck, um método ágil é comparável ao ato de dirigir um carro: você deve observar a estrada e fazer **correções contínuas** para se manter no caminho. Neste contexto onde a agilidade é fundamental, o testador seria aquele que ajuda o motorista a chegar com segurança ao seu destino, impedindo que sejam feitas conversões incorretas durante o percurso, evitando que o motorista se perca e fazendo com que ele pare epeça instruções quando necessário.

Neste ambiente, destaca-se o TDD, como sendo uma abordagem evolutiva na qual o **desenvolvedor escreve o teste antes de escrever o código funcional** necessário para satisfazer aquele teste.

## Ciclo de desenvolvimento com TDD

![TDD Flow](./images/tdd_flow.gif)

Todos que já viram pelo menos um pouco sobre TDD devem ter visto essa imagem. Ela é basicamente a estrutura do funcionamento da cultura do TDD. Possuindo 3 grandes passos:

- `Red` - etapa inicial do TDD, onde você escreve um teste que falha, para alguma funcionalidade que você ainda vai escrever.
- `Green` - já com o teste criado, é o momento que você precisa fazer o teste passar, lembrando sempre de ir para solução mais simples primeiro.
- `Refactor` - etapa para eliminar códigos redundantes, remover acoplamentos e deixar o design de código mais legível.

## Por que poucos fazem TDD?

Existem alguns pontos principais que os desenvolvedores falam, quando tentam justificar porque não fazem TDD:

- `Perda de tempo` - os desenvolvedores acham que por ter de escrever além do código, os testes, vai fazer com que demorem mais para desenvolver. Para quê perder tempo aprendendo uma coisa que eu não vejo como útil/importante não é mesmo?
- `Curva de aprendizado` - o estilo de programar muda, é uma nova cultura e para isso, você precisa se adaptar. E é nesse ponto que a maioria desiste, pois não conseguem ver o valor do esforço inicial.

## O que ganho com TDD?

### Reduz o tempo gasto em depuração e correção de bugs

Quando iniciamos o processo de correção de um bug, a primeira coisa que geralmente fazemos é tentar reproduzir o erro, para em seguida depurar o fluxo onde ocorre o bug para enfim analisar o estado dos objetos em busca da raíz do problema. Quando você não possui testes, você precisa mais uma vez realizar os passos de um teste funcional para depurar. Se você escrever um teste unitário que “estimule” o sistema a passar pelo código defeituoso, você estará “reproduzindo” o erro sem necessidade de executar a aplicação como um todo.

### Não é desenvolvido código desnecessário

Essa pode parecer uma frase um pouco controversa, mas não é. Como o flow de desenvolvimento é "Criar testes antes, fazer solução depois", você acaba não criando código desnecessário, visto que você sempre faz o suficiente para os testes passarem.

### Auxilia testes de regressão

É comum, ao corrigir um bug, introduzir um novo bug. Em outras palavras, a correção de um bug pode ter como efeito colateral que uma parte do software que antes funcionava deixe de funcionar. Quando isto ocorre, dizemos que o software regrediu. Chamam-se “teste de regressão” os testes que visam verificar a integridade geral do sistema quando um bug é corrigido, ou até mesmo quando uma nova funcionalidade é implementada no sistema. O uso do TDD vai reduzir a introdução de efeito colaterais junto com alterações no código. É claro que apenas na parte 
do código que seja coberta pelo testes unitários. Além disso, quando um teste passa a falhar após sua alteração, você acabou de identificar o bug num momento muito próximo de sua introdução.

### Melhora a qualidade do código

O TDD encoraja que você pense antes de desenvolver a solução e que você sempre crie as soluções mais simples. Existe uma frase muito importante no TDD que é:

> "Se são necessárias muitas linhas de código criando objetos para uma simples
asserção, então há algo de errado."
> 

Isso faz com que você já saiba se está indo na direção certa para construção da solução ou se ela está fortemente acoplada e precisa ser modularizada/simplificada.

### Documentação pelos testes

Os testes nos ajudam a documentar o sistema se nomearmos ele bem. Como pensamos antes de codificar e fazemos testes pequenos para cada pedaço de funcionalidade, praticamente somos obrigados a escrever um teste legível. Se pararmos para ver todos os testes de uma funcionalidade temos ali praticamente uma documentação de caso de uso.

### Refatoração constante

Como o próprio ciclo do TDD já sugere, a última etapa é a refatoração. Então, para cada teste que escrevemos, olhamos novamente nosso código e se nos sentirmos incomodados devemos refatorá-lo. O grande diferencial de trabalharmos com testes automatizados é que temos a segurança de fazer alterações, pois nossos testes devem garantir que nosso código continuará funcionando. Outro aspecto interessante é que refatorando a cada “verde”, evitamos que nosso código fique ilegível e com repetições desnecessárias.