# 🍋 Lemonj Programming Language
## What is Lemonj ?
Lemonj is currently a concept of a programming language. Features and syntax are not yet implemented.

## What inspires Lemonj?
Lemonj is inspired by many programming languages such as <a href="https://www.typescriptlang.org/" target="_blank">TypeScript</a>, 
<a href="https://www.python.org/" target="_blank">Python</a> and <a href="https://learn.microsoft.com/en-us/dotnet/csharp/" target="_blank">C#</a>.

# The Syntax
## A simple Lemonj program
```js
main lemonjProg{

@start
  lemonjProg.print("Hello from Lemonj");
  @comment="This is a commment 2";
@end

}
```
1. A Lemonj program must have a main method.
2. the <code>lemonjProg</code> refers to the name of the program.
3. <code>@start</code> indicates the entry point of the program.
4. <code>@end</code> indicates the exit point of the program.
5. All statements ends with a semicolon ";".
7. <code>@comment</code> to write comment inside of the <code>@start</code> and <code>@end</code> block.
7. <code>// </code> to write comment inside of the <code>@start</code> and <code>@end</code> block.

## Variable declaration with static typing
```js
@enum rarityOptions={"normal","rare", "super-rare"};

var name:string = "Falcon";

var age:int = 22;

var canFly:boolean = True;

var isFriendly:boolean = False;

var price:double = 300.65;

var rarity:rarityOptions = @rarityOptions;
```

## Null safety
```js
// allows username tto be null or not null
var username:string = null; 

// prevents username2 to be null
// Using @notnull{ } and wrapping the variable that couldn't be null
var @notnull{username2:string} = null; // an error occurs due to null
```

## Object Oriented Programming
```js
@enum rarityOptions={"normal","rare", "super-rare"};

// creating an animal class
@class Animal{

// Defining object property
  var name:string;

  var age:int;

  var canFly:boolean;

  var isFriendly:boolean;

  var price:double;

  var rarity:rarityOptions;
}

// Creating a new object
var newAnimal:object = @Animal.create();

// Short alias for newAnimal
newAnimal as @na;

// Assigning property value
na.name = "Po";

na.type = "Mamals"; // an error occurs due to undefined property
```

## Web development (Server side)
```js
// If current user is the original author of the post
// display post delete button

@if(currentUser.uid == post.author.uid){

  <button action=@deletePost(post.id)>
    Delete post
  </button>

}

```
