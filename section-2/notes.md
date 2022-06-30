# Execution contexts and Lexical Env

# Conceptual Asides

## CA - Syntax Parser (Big Word Alert)

Definition: A program that reads your code and determines what it does and if its grammar is valid. It is a program written by someone else to read your code and translate it into something that computer undertands.

## Execution Context - Big Word Alert

    A wrapper to help manage the code tha is running. There are a multiple lexical enviroments in a progarm. Which is currently running is managed via execution contexts. It can contain things beyond what you've written in your code.

## Lexical Enviorment - Big Word Alert

    Where something sits physically in the code you write.

    Lexical means having to do with words or grammar. Lexicalc env exists in programming langauge in which where you write something is important.

## CA - Name/Value Pairs aka Objects

    Objects are important part of javascript.

    ## Name/Value Pair

    A name which maps to a unique value. The name may be defined mor ethan once, but can have only one value in any given context. That value may be more name/value pairs.

    i.e Address = '100 Main St.'

All code that runs in js runs in an execution context. A wrapper, the js engine a program that other people wrote to parse your code.

It wraps the currently executing code in execution context.

The base execution context has couple of other things that comes along for a ride that you did not write. They are already there.

When you run your js code in browser or any other env like node. The Global execution context creates two things for you.

1. A global object
2. A special variable called "this" that points to the global object.

This global object is collection of name/value pairs and methods that can do things for you.

In your javascript file, if you create variables or functions that are not inside other function, they get attached to the global object.

For variables there is one caveat. They will only get attached to the global object if you create them using the var keyword.

For example:

```JS

var a = 'hello world';
function b(){
    return 'yay';
}

```

Both of them will now be part of a global object.

So in execution context, at the base level lives:

- Global object
- 'this' variable
- link to outer env
