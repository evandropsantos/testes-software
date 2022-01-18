# Pensando em testes
- **O que o código precisa fazer?**
- **Que dados ele recebe?**
- **Que dados ele precisa retornar?**
- **Que ações precisam acontecer para o código rodar?**

### Não coloque a carroça na frente dos bois

Sim, é isso mesmo que você leu. Não tente avançar o ciclo dos testes, só porque você já sabe como implementar do início ao fim. É importante que você se mantenha no ciclo (Red, Green, Refactor), isso vai fazer com que através da prática e disciplina, você se acostume e acabe ganhando agilidade e melhor visão do processo de desenvolvimento.

### Trate código de teste como código de produção

O código de teste precisa ser legível, separado em etapas bem definidas e possuir um bom report. Isso vai permitir termos nossa documentação, além de facilitar com que outros desenvolvedores entendam o sistema a partir dali. De nada adianta criar um conjunto de testes se eu não souber qual problema aconteceu se algum teste quebrar.

### Evite acoplamento

Quanto mais desacoplados seus testes, melhor. Isso evita a quebra em cascata, auxiliando na busca de erros. Isso também auxilia até mesmo o seu design de código, garantindo algo modularizado e de bem mais fácil manutenção.

### Um teste de cada vez

Esse é o padrão do TDD, mas não custa reafirmar, só escreva um próximo teste, se o primeiro passar. Isso garante que não ficarão coisas pela metade e nem o risco de acabar esquecendo algo no meio do caminho.

### Não teste o desnecessário

Por exemplo, se você estiver usando um framework, você não precisa testar se o método dele está funcionando, isso já foi amplamente testado no framework e o que você estará fazendo, nada mais é que repetindo testes.

### Responsabilidade Única

Isso serve para o seu código e para o seu teste também, se você precisa escrever muito para fazer um teste, significa que alguma coisa está errada. Sempre faça testes pequenos, em geral, um teste para um método ou mais testes para um mesmo método, nunca o contrário. Um teste 
jamais poderá testar mais de um método.