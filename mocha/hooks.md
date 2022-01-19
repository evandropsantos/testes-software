# Hooks
- **before:** Roda uma vez, antes do bloco;
- **after:** Roda uma vez, depois do bloco;
- **beforeEach:** Roda todas as vezes, antes do bloco;
- **afterEach:** Roda todas as vezes, depois do bloco.

```jsx
describe('Hooks', () => {

  before(() => console.log('before'))

  beforeEach(() => console.log('beforeEach'))

  after(() => console.log('after'))

  afterEach(() => console.log('afterEach'))

  it('test 1', () => console.log('test 1'))

  it('test 2', () => console.log('test 2'))
})

// before
// beforeEach
// test 1
// afterEach
// beforeEach
// test 2
// afterEach
// after
```

### Na prática

```jsx
describe('Hooks Pratica', () => {
  let arr

  before(() => {
    // inicia uma conexão no banco
    // criar um conjunto de dados
  })

  // roda uma vez, depois do bloco
  after(() => {
    // fecha conexão do banco
    // apagar esse conjunto de dados
  })

  beforeEach(() => {
    arr = [1, 2, 3]
  })

  it('O tamanho tem que ser 4 apos inserir um dado', () => {
    arr.push(4);
    console.log(arr.length); // 4
  })

  it('Removendo o ultimo valor, nao deve ter o 3', () => {
    console.log(arr.pop() === 3); // true
  })

  it('Removendo um valor o tamanho sera 2', () => {
    arr.pop();
    console.log(arr.length); // 2
  })
})
```