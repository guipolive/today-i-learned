# typescript

## o que é?

- basicamente, typescript é um superset do es6/javascript

- ele nos permite, além de outras coisas, adicionar tipagem ao javascript
    - com o uso de tipagem, podemos ter alguns benefícios no código como o auxílio do IntelliSense do editor de texto, que antes seria mais difícil, pois uma função javascript poderia receber um objeto qualquer, e esta mesma, utilizando typescript, poderia receber um objeto definido

## importando uma bibliteca

- quando importamos uma biblioteca usando typescript, precisamos importar também as definições de tipos. É possível que essas definições venham junto com a própria lib importada, mas existem casos em que essa lista deve ser instalada separadamente
    - normalmente, é possível instalar essa lista utilizando o comando `npm install @types/express` , onde express é a nossa 'lib' de exemplo.