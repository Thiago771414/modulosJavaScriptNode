# CommonJS e ECMAScript Modules (ES Modules) em JavaScript com Node.js

## Módulos em JavaScript para Node.js
Comparação entre CommonJS e ECMAScript Modules (ES Modules)
O CommonJS é o sistema de módulos padrão para o Node.js antes da adoção dos ES Modules.
O require é utilizado para importar módulos no CommonJS.
Exemplo de módulo CommonJS:

````javascript
// Módulo com a função soma
function soma(a, b) {
    return a + b;
}
module.exports = { soma };
````
Uso do require no arquivo .js
Para usar um módulo CommonJS em um arquivo .js, utilizamos o require para importá-lo.
````javascript
const { soma } = require('./lib'); // Importa a função 'soma' do módulo './lib'
console.log(soma(2, 3)); // Imprime 5
````
## Adotando ECMAScript Modules

Os ECMAScript Modules (ES Modules ou ESM) são uma forma mais moderna de trabalhar com módulos em JavaScript.
Para habilitar os ESM no Node.js, podemos adotar duas estratégias:
Estratégia 1: Utilizando extensão .mjs
Basta renomear os arquivos com extensão .js para .mjs.

````json
node app.mjs
````
Estratégia 2: Atributo type no package.json
Adicionar o atributo type no package.json com o valor "module".

````javascript
// package.json
{
    "name": "my-app",
    "version": "1.0.0",
    "type": "module"
}
````
Exemplo de ECMAScript Module (.mjs)

````javascript
// Módulo com a função soma
function soma(a, b) {
    return a + b;
}

export { soma };
````
Uso do import em um arquivo .mjs
Para utilizar um módulo ECMAScript, utilizamos o import para importá-lo.

````javascript
import { soma } from './lib.mjs'; // Importa a função 'soma' do módulo './lib.mjs'
console.log(soma(2, 3)); // Imprime 5
````
Conclusão

CommonJS e ECMAScript Modules são sistemas de módulos utilizados em JavaScript com Node.js.
O CommonJS usa require para importar módulos, enquanto o ESM utiliza import.
Para habilitar os ECMAScript Modules no Node.js, podemos utilizar a extensão .mjs ou adicionar o atributo type: "module" ao package.json.
