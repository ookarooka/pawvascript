# PawvaScript

<img alt='PawvaScript Logo' src='assets/pawvascript.png' width='300px'/>

## Introduction

Ever wish that JavaScript had less symbols and more dogs? We did, so we made PawvaScript!

PawvaScript is an object-oriented scripting language designed to make JavaScript more programmer-friendly (so friendly that your dog could learn it, probably). PawvaScript draws on many fundamentals from JavaScript but replaces confusing symbols with clear and readable terms, adds types to help with debugging, and throws in some dog related keywords just for fun.

## Features

- Language for scripting
- Object-Oriented
- Static typing
- 5 types
  - string
  - boolean
  - number
  - function
  - breed (what we call objects)
- 5 kinds of loops
- Conditional Statements
- Lists
- Maps
- Single and multi-line comments

## Example Programs

### The Basics

Let's start with the classing Hello, World:

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

woof "Hello, World!";                                               console.log("Hello, World!");
bark "my ball!";                                                    console.log("my ball".toUpperCase());
howl "uh-oh"                                                        console.error("uh-oh");
```

### Variable Declaration and Assignment

<br>Declare variables by barking.

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

leash dogName is "Cece";                                            let dogName = "Cece";

number dogAge is 12;                                                let dogAge = 12;

goodDog isCute is true;                                             let isCute = true;

list dogNames[leash] is ["Cece", "Fluffy"];                         let dogNames = ["Cece", "Fluffy"];

map dogAges[leash:number] is ["Cece": 1, "Fluffy": 2];              let dogAges = {"Cece": 1, "Fluffy": 2};

!!! this has a default initialization of 0 !!!
number cuteness;                                                    let cuteness;

cuteness is 100;                                                    cuteness = 100;
```

### Strings

String interpolation and concetation:

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

leash dogName is "Ce" with "Ce";                                    let dogName = "Ce" + "Ce";

leash sentence is "![dogName] is the best dog";                     let sentence = `${dogName} is the best dog`;
```

### Lists

Lists are the PawvaScript equivalent of arrays in JavaScript:

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

list goodDogs[leash] is ["CeCe", "Buster", "Muffin"];               let goodDogs = ["CeCe", "Buster", "Muffin"];

!!! The without keyword can remove elements from a list. !!!
list bestDogs[leash] is goodDogs without "Muffin";                  let bestDogs = goodDogs;
                                                                    const indexOfMuffin = goodDogs.indexOf("Muffin");
                                                                    if (indexOfMuffin > -1) {
                                                                         bestDogs.splice(indexOfMuffin, 1);
                                                                    }

list ages[number] is [1, 1, 2];                                     let ages = [1, 1, 2];
```

### Maps

Maps are data structures like Python dictionaries.

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

map goodDogs[leash:leash] is [                                      let goodDogs = {
    "CeCe": "German Shepherd",                                          CeCe: "German Shepherd",
	"Buster": "Golden Doodle",                                          Buster: "Golden Doodle",
	"Mo": "Potato"                                                      Mo: "Potato"
];                                                                  };
map ages[leash:number] is ["CeCe": 1, "Buster": 1, "Mo": 5];        let ages = {CeCe: 1, Buster: 1, Mo: 5};
```

### Relational Operators

Wanna compare stuff?

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

boolean a is x equals y;                                            let a = x === y;

a is x notEquals y;                                                 a = x !== y;

a is x isGreaterThan y;                                             a = x > y;

a is x isLessThan y;                                                a = x < y;

a is x isAtLeast y;                                                 a = x >= y;

a is x isAtMost y;                                                  a = x <= y;
```

### Arithmetic Operators

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

number a is x + y;                                                  a = x + y;

a is x - y;                                                         a = x - y;

a is x * y;                                                         a = x * y;

a is x / y;                                                         a = x / y;

a is x mod y;                                                       a = x % y;

a is x!;                                                            a = x!;

a is -x;                                                            a = -x;
```

### Conditional Statements

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

if x isAtLeast y then:                                              if (x <= y) {
    leash dogName is "CeCe";                                            let dogName = "CeCe";
else:                                                               else {
    leash dogName is "Buster";                                          let dogName = "Buster";
tail                                                                }

if x notEquals y then:                                              if (x !== y) {
    woof "CeCe is kinda cute";                                          console.log("CeCe is kinda cute");
else if x isGreaterThan y then:                                     else if (x > y) {
    woof "CeCe is pretty cute";                                         console.log("CeCe is pretty cute");
else if x isLessThan y then:                                        else if (x < y) {
    woof "Okay, CeCe is really cute";                                   console.log("Okay, CeCe is really cute");
else:                                                               else {
    woof "CeCe is the cutest of the cutest";                            console.log("CeCe is the cutest of the cutest");
tail                                                                 }
```

### Comments

Let's write some comments!

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

!!! I'm a one line comment !!!                                      // I'm a comment

!!! I'm a                                                           /* I'm a
multiline                                                           multiline
comment !!!                                                         comment */
```

### Loops

Forever Loop

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

chase:                                                              while (true) {
    woof "I run forever!";                                      	    console.log("I run forever!");
tail                                                                }
```

<br>Fixed Loop

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

chase 5 times:                                                      for (let i = 0; i < 5; i++) {
    woof "Stay.";                                              	        console.log("Stay.");
tail                                                                }
```

<br>While Loop

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

chase while x isAtMost 5:                                           while (x <= 5) {
    woof x;                                                     	    console.log(x);
tail                                                                }
```

<br>For Loop

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

loop number i is 0 by i*2 while i is less than 10:                  for (let i = 0; i < 10; i *= 2) {
    say i;                                                     	        console.log(i);
end                                                                 }
```

<br>For Each Loop

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

loop element through myList:                                        for (let element of myArray) {
    say element;                                               	        console.log(element);
end                                                                 }
```

### Functions

Let's find the greatest common divisor between two numbers!

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

bark func gcd chases[number:num1, number:num2] fetches number:	    function gcd(num1, num2) {
    bark number remainder;                                              let remainder;

    loop while (a mod b) is greater than 0:                             while ((num1 % num2) > 0) {
        remainder is (a mod b);                              	            remainder = a % b;
        a is b;                                                             a = b;
        b is remainder;                                                     b = remainder;
	end                                                                 }
	give a;                                                             return a;
end                                                                 }

bark number a is 8;                                                 let a = 8;
bark number b is 12;                                                let b = 12;
bark number c is gcd(a, b);                                         let c = gcd(a, b);
```

The classic Fibonacci function to get the nth term of the Fibonacci sequence:

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

bark func fib chases[number:n] fetches number:                      function fib(n) {
	if n is at most 1 then:                                             if (n <=1) {
		give n;                                                             return n;
	else:                                                               } else {
		give fib(n-1) + fib(n-2);                                           return fib(n-1) + fib(n-2);
	end                                                                 }
end                                                                 }

bark huzzah is fib(100);                                            let huzzah = fib(100);
```

### Objects

Let's make an owner object!

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

bark breed Owner is:                                                class Owner {
    bark string dogName;                                                constructor(dogName) {
                                                                            this.dogName = dogName;
    bark func Owner chases[string:dogName] fetches Owner;               }

    bark func introduceDog:                                             introduceDog() {
        say "My dog's name is " with Owner's dogName;                       console.log(`My dog's name is ${this.dogName}`);
    end                                                                 }

    bark func command fetches string:                                   command() {
        give Owner's dogName with ", stay!";                                return `${this.dogName}, stay!`;
    end                                                                 }
end                                                                 }

bark Owner lucille is Owner("Cece")                                 let lucille = new Owner("Cece");
lucille's introduceDog() !!! output: "My dog's name is Cece" !!!    lucille.introduceDog();
say lucille's command()  !!! output: "Cece, stay." !!!              console.log(lucille.command());
```
