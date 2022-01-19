# Instalação

```jsx
yarn add -D mocha chai
```

```json
{
  "name": "js-tdd-course",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT",
  "scripts": {
    "test": "mocha tests/**/*.spec.js",
    "test:tdd": "mocha tests/**/*.spec.js --watch"
  },
  "devDependencies": {
    "chai": "^4.3.4",
    "mocha": "^9.0.2"
  }
}
```