# PawvaScript

<img alt='PawvaScript Logo' src='assets/pawvascript.png' width='300px'/>

## Introduction
Ever wish that JavaScript had less symbols and more dogs? We did, so we made PawvaScript!

PawvaScript is an object-oriented scripting language designed to make JavaScript more programmer-friendly (so friendly that your dog could learn it, probably). PawvaScript draws on many fundamentals from JavaScript but replaces confusing symbols with clear and readable terms, adds types to help with debugging, and throws in some dog related keywords just for fun.

## Features
* Language for scripting
* Object-Oriented 
* Static typing
* 5 types
    * string
    * boolean
    * number
    * function
    * breed (what we call objects)
* 5 kinds of loops
* Conditional Statements
* Lists
* Maps
* Single and multi-line comments

## Example Programs

### The Basics

```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

say "Hello, World!";                                                console.log("Hello, World!")
```

<br>Initialize variables by barking.
```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

bark string dogName is "Cece";                                      let dogName = "Cece";

bark number dogAge is 12;                                           let dogAge = 12;

bark boolean isCute is true;                                        let isCute = true;

bark list dogNames[string] is ["Cece", "Fluffy"];                   let dogNames = ["Cece", "Fluffy"]

bark map dogAges[string:number] is ["Cece": 1, "Fluffy": 2];        let dogAges = {"Cece": 1, "Fluffy": 2} 

!!! this has a default initialization of 0 !!! 
bark number cuteness;                                               let cuteness; 

cuteness is 100;                                                    cuteness = 100;
```

<br>String interpolation and concetation
```JavaScript
PAWVASCRIPT                                                       JAVASCRIPT

bark string dogName is "Ce" with "Ce"                             let dogName = "Ce" + "Ce";

bark string sentence is "![dogName] is the best dog"              let sentence = `${dogName} is the best dog`;
```

<br>Wanna compare stuff?
```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

x equals y                                                          x === y

x not equals y                                                      x !== y

x is greater than y                                                 x > y

x is less than y                                                    x < y

x is at least y                                                     x >= y

x is at most y                                                      x <= y  
```

<br>Conditional Statements
```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

if x is at least y then:                                            if (x <= y) {
    bark string dogName is "CeCe";                                      let dogName = "CeCe";
else:                                                               else {
    bark string dogName is "Buster";                                    let dogName = "Buster";
end                                                                 }  

if x not equals y then:                                             if (x !== y) {
    say "CeCe is kinda cute";                                           console.log("CeCe is kinda cute");
else if x is greater than y then:                                   else if (x > y) {
    say "CeCe is pretty cute";                                          console.log("CeCe is pretty cute");
else if x is less than y then:                                      else if (x < y) {
    say "Okay, CeCe is really cute";                                    console.log("Okay, CeCe is really cute");
else:                                                               else {
    say "CeCe is the cutest of the cutest";                             console.log("CeCe is the cutest of the cutest");
end                                                                 }
```

<br>Let's write some comments
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

loop:                                                               while (true) {
    say "I run forever!";                                      	        console.log("I run forever!")
end                                                                 }
```

<br>Fixed Loop
```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

loop 5 times:                                                       for (let i = 0; i < 4; i++) {
    say "Stay.";                                              	        console.log("Stay.")
end                                                                 }
```

<br>While Loop
```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

loop while x is at most 5:                                          while (x <= 5) {                                
    say x;                                                     	        console.log(x);
end                                                                 }
```

<br>For Loop
```JavaScript
PAWVASCRIPT                                                         JAVASCRIPT

loop number i is 0 by i*2 while i is less than 10:                  for (let i = 0; i *= 2; i <10;) {
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

