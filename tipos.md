# Tipos de testes
O TDD se baseia principalmente nos testes unitários, que de fato são a base para o desenvolvimento orientado por testes. Mas existem outros testes tão importantes quanto. Martin Fowler, que é basicamente um dos maiores apoiadores do TDD, disse o seguinte: a maioria do desenvolvimento sempre foi pensada na interface e, com isso, os testes mais criados também eram os de interface. Mas o problema é que esses testes são muito lentos e nós não queremos isso. Nós queremos respostas eficientes e rápidas, por isso, os testes unitários precisam ser o de maior de número e os mesmos precisam ser bem rápidos. Seguindo esse pensamento, ele desenvolveu a seguinte pirâmide:

![Pirâmide de testes - Criada pelo Martin Fowler](./images/pyramid.png)

Criada pelo Martin Fowler

Nessa pirâmide, podemos ver que os testes unitários formam a base, seguidos pelos testes de serviço, que podem ser entendidos como testes de integração e testes de sanidade. Por final, temos os testes de interface, também conhecidos como testes de aceitação. Esse tipo de lógica faz com que os testes sejam mais eficazes e rápidos.

E eles seguem o seguinte fluxo, se os testes unitários passarem, realizamos a integração entre os componentes e vemos se os mesmos continuam funcionando. Tudo estando ok, fazemos os testes de aceitação, que já trabalham com a interface e também com usuários diretamente. Se algum teste quebra, todo o resto é abortado, evitando assim de rodarmos testes mais lentos sem necessidade.

Existem outros vários tipos de testes, mas irei abordar os principais, que serão os utilizados no nosso dia-a-dia.

### Teste Unitário (Unit Test)

O teste unitário tem por objetivo testar a menor parte testável do sistema (unidade), em geral, um método. Idealmente, o teste unitário é independente de outros testes, validando assim cada parte ou funcionalidade individualmente.

Para seguir um padrão legal do seu teste unitário, ele deve ser capaz de responder as seguintes perguntas:

- O que eu estou testando?
- O que o método deveria fazer?
- Qual o seu atual retorno?
- O que eu espero que retorne?

Se você conseguir olhar para o teste e responder tudo isso, seu teste é bastante válido e irá te ajudar bastante caso algo dê errado.

### Teste de Integração (Integration Test)

Teste de integração é a fase do teste de software em que módulos são combinados e testados em grupo. Ela vem depois dos testes unitários, em que os módulos são testados individualmente, e vem antes dos testes de aceitação, em que o sistema completo é testado num ambiente que simula o ambiente de produção.

O teste de integração é alimentado pelos módulos previamente testados individualmente pelos testes unitários, agrupando-os assim em componentes, como estipulado no plano de teste, e resulta num sistema integrado e preparado para o teste de sistema.

### Teste de Aceitação (Acceptance Test)

O teste de aceitação verifica se todo o projeto funciona de acordo com sua especificação, ele já é um teste final, que visa juntar todos os módulos e testá-los em conjunto já a uma interface gráfica. Esses testes visam aferir se algo na interface faça o sistema não funcionar ou que dificulte o acesso ao usuário, um exemplo seria se um input não estivesse aparecendo para que dados fossem inseridos.