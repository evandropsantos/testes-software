# Chai
Chai é uma biblioteca de asserção BDD / TDD compatível com **Node** e **Browser**, que pode ser perfeitamente emparelhado com qualquer estrutura de teste de **Javascript**.

## **Site Oficial**

[https://www.chaijs.com](https://www.chaijs.com/)

## Documentação

[https://www.chaijs.com/api/bdd](https://www.chaijs.com/api/bdd/)

```jsx
const { expect } = require('chai')

describe('Chai', () => {
  let arr

  beforeEach(() => {
    arr = [1, 2, 3]
  })

  // testar tipos ou se existe (smoke test)
  it('verifica se e um array', () => {
    expect(arr).to.be.a('array')
  })

  it('O tamanho tem que ser 4 apos inserir um dado', () => {
    arr.push(4)
    expect(arr).to.have.lengthOf(4)
  })

  it('Removendo o ultimo valor, nao deve ter o 3', () => {
    arr.pop()
    expect(arr).to.not.include(3)
  })

  it('Verificando o booleano', () => {
    expect(arr.pop() === 3).to.be.true
  })

  it('Removendo um valor o tamanho sera 2', () => {
    arr.pop()
    expect(arr).to.have.lengthOf(2)
  })
})
```