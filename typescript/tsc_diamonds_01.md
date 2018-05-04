# Diamonds 01

## Typescript

interface testI { 
    name?: string,
    isTest: boolean,
    repeatedTimes: number | string
}

// 1) using Interface
//
const test: testI = {
    isTest: false,
    repeatedTimes: "2"
};
// 2.1) Function type
//
let myAdd: ((x: number, y: number) => number) =
    function (x: number, y: number): number { return x + y; };

// 2.2) Function type using Interface
//      
interface Ifn {
    (x: number, y:number):number
}

let myAdd2: Ifn = function (a:number , b:number) { 
    return a + b;
}


// 3) Object type
//
const myObj: ({ firstName: string }) = { firstName: 'Duo' };

// 4) Classes 
//
class Pokemon { 
    // must declare public, protected and private 
    // in the constructor;
    constructor(public name: string, public _type: string) {}
}

const pokemon = new Pokemon('Pikachu', 'electric');
console.log(pokemon);


## Plain JavaScript

// 1) using Interface
//
var test = {
    isTest: false,
    repeatedTimes: "2"
};
// 2.1) Function type
//
var myAdd = function (x, y) { return x + y; };
var myAdd2 = function (a, b) {
    return a + b;
};
// 3) Object type
//
var myObj = { firstName: 'Duo' };
// 4) Classes 
//
var Pokemon = /** @class */ (function () {
    // must declare public, protected and private 
    // in the constructor;
    function Pokemon(name, _type) {
        this.name = name;
        this._type = _type;
    }
    return Pokemon;
}());
var pokemon = new Pokemon('Pikachu', 'electric');
console.log(pokemon);
