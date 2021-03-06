
<img src="https://www.luby.com.br/wp-content/uploads/2020/05/Logo-01-160x52.png" style="" />



*Implemente os métodos abaixo:*


*1)* Implemente um método que crie um novo array baseado nos valores passados.<br>
Entradas do método (3,a), Resultado do método: ['a', 'a', 'a']

```javascript
function repeatString(num, str) {
  if (typeof num !== 'number') {
    console.log('O primeiro argumento deve ser um número', typeof num);
  }
  const arr = new Array(num);
  for (let i = 0; i < arr.length; i++) {
    arr[i] = str;
  }
  return arr;
}

console.log(repeatString(7, 'oi'));
```

*2)* Implemente um método que inverta um array, não utilize métodos nativos do array.<br>
Entrada do método ([1,2,3,4]), Resultado do método: [4,3,2,1]

```javascript
function invertArray(arr) {
  const newArr = [];
  for (let i = 0; i < arr.length; i++) {
    newArr[arr.length - 1 - i] = arr[i];
  }

  return newArr;
}

console.log(invertArray([1, 2, 3, 'a', 4]));
```

*3)* Implemente um método que limpe os itens desnecessários de um array (false, undefined, strings vazias, zero, null).<br>
Entrada do método ([1,2,'', undefined]), Resultado do método: [1,2]

```javascript
function cleanArray(arr) {
  const clearArr = [];
  for (let i = 0; i < arr.length; i++) {
    if (arr[i]) {
      clearArr.push(arr[i]);
    }
  }

  return clearArr;
}

console.log(cleanArray([undefined, 0, 1, 'c', false, true, '', null]));
```

*4)* Implemente um método que a partir de um array de arrays, converta em um objeto com chave e valor.<br>
Entrada do método ([["c",2],["d",4]]), Resultado do métdodo: {c:2, d:4}

```javascript
function arrayToObj(arr) {
  const newObj = {};
  for (let i = 0; i < arr.length; i++) {
    if (arr[i]) {
      newObj[arr[i][0]] = arr[i][1];
      {
      }
    }
  }

  return newObj;
}

console.log(
  arrayToObj([
    ['c', 2],
    ['d', 4],
  ]),
);
```

*5)* Implemente um método que retorne um array, sem os itens passados por parâmetro depois do array de entrada.
Entrada do método ([5,4,3,2,5], 5,3), Resultado do método: [4,2]

```javascript
function removeElements(arr, ...n) {
  const newArr = arr.filter(a => !n.includes(a));

  return newArr;
}

console.log(removeElements([1, 2, 3, 6], 6));
```

*6)* Implemente um método que retorne um array, sem valores duplicados.<br>
Entrada do método ([1,2,3,3,2,4,5,4,7,3]), Resultado do método: [1,2,3,4,5,7]

```javascript
function distinctElements(arr) {
  const newArr = [...new Set(arr)]
}

console.log(distinctElements([1, 2, 3, 6, 6]));
```

*7)* Implemente um método que compare a igualdade de dois arrays e retorne um valor booleano.<br>
Entrada do método ([1,2,3,4],[1,2,3,4]), Resultado do método: true

```javascript
function arrayCompare(arr) {
  return (arrA.toString() == ArrB.toString());
}

console.log(arrayCompare([1, 2, [3], [4, 5]]));
```

*8)* Implemente um método que remova os aninhamentos de um array de arrays para um array unico.<br>
Entrada do método ([1, 2, [3], [4, 5]]), Resultado do método: [1, 2, 3, 4, 5]

```javascript
function arrayDry(arr) {
  return arr.flat()
}

console.log(arrayCompare([1, 2, [3], [4, 5]]));
```

*9)* Implemente um método divida um array por uma quantidade passada por parâmetro.<br>
Entrada do método ([1, 2, 3, 4, 5], 2), Resultado do método: [[1, 2], [3, 4], [5]]

```js
function arraySplit(arr, div) {
  let newArr = [];
  let size = Math.ceil(arr.length/div);
  for(let i = 0; i < size; i++){
    newArr.push(arr.splice(0,div))
    console.log(1)
  }
  return newArr;
}

console.log(arraySplit([1, 2, 3, 4, 5], 4));
```

*10)* Implemente um método que encontre os valores comuns entre dois arrays.<br>
Entrada do método ([6, 8], [8, 9]), Resultado do método: [8]

```js
function intersection(arrA, arrB){
    let newArr = [];
    arrA.map(a => {
        if(b.includes(a)) {
            newArr.push(a);
        }
});
    return newArr;
}

console.log(intersection(a,b))
```

ps: Esses exercícios são de senso comum da comunidade desenvolvimento, utilize o melhor padrão para implementação, criando uma semântica factível.


