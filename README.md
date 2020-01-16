# JS Quick Tips #1

[Version Code](code/jsquicktips1.js)

##### 1- A- Verifier si un tableau contient au moins un element qui realise une certaine condition (passée comme fonction)

```javascript
const monTableau = [1, 5, 8, 4, 3];
console.log(monTableau.some((element) => element % 2 === 0));
// resultat: true (8 et 4 sont divisibles par 2)
```

##### B - Meme truc mais cette fois-ci, on verifie que tous les elements du tableau réalisent notre condition

```javascript
console.log(monTableau.every((element) => element === 5));
// resultat: false
const autreTableau = [5, 5, 5, 5, 5, 5];
console.log(autreTableau.every((element) => element === 5));
// resultat: true
```

##### 2- A- Rapidement convertir une chaine de characteres vers un nombre

```javascript
const maChaine = '514.33';
console.log(+maChaine); // resultat: 514.33
```

##### B - Faire l'inverse

```javascript
const monNombre = 6868;
console.log(`${monNombre}`); // resultat: "6868"
```

##### 3- A- Initialiser plusieurs variables dans une seule ligne

```javascript
const [premier, deuxieme, troisieme] = [55, 'piano', true];
console.log(premier); //resultat: 55
console.log(deuxieme); // resultat: "piano"
console.log(troisieme); //resultat: true
```

##### B- Meme truc mais on veut sauter un element

```javascript
const mesElements = [1, 2, 3];
const [foo, , bar] = mesElements;
console.log(foo); //resultat: 1
console.log(bar); //resultat: 3
```

##### C- Extraire des elements à partir un objet par nom

```javascript
const monObjet = {
    hello: 'Hello',
    disney: 'Disney',
    world: 'World'
};
const { hello, world } = monObjet;
console.log(hello); //resultat: Hello
console.log(world); //resultat: World
```

##### 4- Rendre les grands nombres plus lisibles en utilisant le charactere '\_'

```javascript
const dixMillions = 10_000_000;
console.log(dixMillions); //resultat: 10000000

//on peut aussi appliquer ça sur les nombres decimaux
const PI = 3.14_15_92_65;
console.log(PI); //resultat: 3.14159265

//Attention: on n'a pas le droit d'utiliser ce charactere au debut, a la fin, ou adjacent au point decimal
// const monDec = 55_.08; //Erreur
// const monDec = 55._08; //Erreur
// const monDec = _55.08; //Erreur
// const monDec = 55.08_; //Erreur
```

### References:

-   [Array.prototype.some\(\)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
-   [Array.prototype.every\(\)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
-   [Unary + operator](https://www.ecma-international.org/ecma-262/5.1/#sec-11.4.6)
-   [Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
-   [Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
-   [Numeric separators](https://v8.dev/features/numeric-separators)
