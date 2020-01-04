### Typescript Compiler Online
<a href="https://www.typescriptlang.org/play" onclick="return ! window.open(this.href);">Playground</a>

### Install Typescript Compiler
```bash
npm install -g typescript 
npm install -g ts-node
```

### Test
_Typescript Compiler_
```
tsc --help
```

### Setting Up Visual Studio Code Path
* _View > Command Palette (CTRL + SHIFT + P)_
* _Install Path_

```
In windows: Go to the Enviroment Variables and edit the Path user variable. 
Inside of it, add a new variable with the current bin path of your Visual Studio Code installation. 
For example, "C:\Users\gokhankoc\AppData\Local\Programs\Microsoft VS Code\bin"
```

### Compiling Simple App
```ts
// index.ts
import axios from 'axios';

const url = 'https://jsonplaceholder.typicode.com/todos/1';

axios.get(url).then( response => {
    console.log(response.data);
});
```
```
tsc index.ts // Returns index.js
```

### Compile and Run
```
ts-node index.ts
```

### Defining an Interface
_Interfaces in TypeScript are used to define the structure of an object._
```ts
interface Todo {
    id: number;
    title: string;
    completed: boolean;
}

const todo = {id: 12, title: "Godfather", completed: true} as Todo;
```

### Specifying Types in Function Arguments
```ts
function logTodo (id: number, title: string, completed: boolean){
    console.log(`
        The todo with ID: ${id}
        Has a title of: ${title}
        Is it finished? ${completed}
    `); 
}
```

### Annotations
```ts
let myNumber: number = 5;
let myName: string = 'Gokhan';
let isActive: boolean = true;
let nothingMuch: null = null;
```

_Built-in Objects_
```ts
let now: Date = Date();
```

_Array of Strings_
```ts
let colors: string[] : ['red','green','blue'];
```

_Classes_
```ts
class Car{
//
}

let myCar: Car = newCar();
```

_Object Literal_
```ts
let point: { x: number; y: number } = {
    x: 10,
    y: 20
};
```


