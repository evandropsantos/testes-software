# Comandos base
- **describe:** Descreve os testes de um certo bloco;
- **context:** Separa os casos de testes;
- **it:** Corpo dos testes;
- **skip:** Ignora um teste;
- **only:** roda apenas um teste especifico.

```jsx
const { expect } = require('chai')

describe('Main', () => {

  describe('Metodo A', () => {

    context('Case 1', () => {
      it('should bla bla bla', () => {
        expect(2 + 2).to.equal(4)
      })
    })

    context.skip('Case 2', () => {
      it('should not bla bla bla', () => {
        throw new Error('Deu ruim')
      })
    })
  })

  describe('Metodo B', () => {

    it('should bla', () => {
      expect(5 - 3).equal(2)
    })
  })
})
```