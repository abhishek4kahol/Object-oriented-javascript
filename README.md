# Object-oriented-javascript
JavaScript is not a class-based but an object-based enironment.In an object-based environment, there are no classes.

Working in object-based environment has its upsides, but there are limits to what you do without class-based concepts like properties and inheritance, for that ECMAScript has sought to integrate object oriented into JavaScript without scarificing its unique style.
JavaScript uses **Prototypical inheritance** rather than classical inheritance like many other C-style languages.

## OBJECT

An object is a container of values combined to form a single data structure that has aparticular identity such as a person, an      order, through an aggregation of data and functionalities.

Simplest way to create an object in JavaScript is: 
```ruby
var emptyObject = {};
var person = {"name": "John", "surname": "Smith"};
```

> The data is called properties and are represented by pairs of names and values. 

Example:
```ruby
Nested object:

var person = {name: "John",
              surname: "Smith",
              address: {
                        street: "13 Duncannon Street",
                        city: "London",
                        country: "United Kingdom"
                        }
             };
```

To access the values stored in an object property, we have two approaches:

1.The firstapproach is the so-called dot-notation,by which we indicate an object and the property.

```ruby
var name = person.name;
```

2.the second approach, we specify the properties of an object by indicating its name as a string in square brackets:  

```ruby
var name = person["name"];
```

> The functionalities are usually called methods and are represented by functions.

## METHODS
While object properties represent data, methods represent actions that an object can peform.
Example:

```ruby
function showFullName() {
return "John Smith";
}
```

```ruby
var person = {name: "John",
surname: "Smith",
showFullName: function() {
      return "John Smith";
  }
};
```

ECMAScript 2015 allows us to define methods in literal notation in a more direct form, as in
the following example:

```ruby
var person = {name: "John",
surname: "Smith",
showFullName() {
    return "John Smith";
    }
};
```
## CLASSES

ES6 specifications introduce the class construct in JavaScript too. However, this construct has nothing to do with the classes of the traditional Object-Oriented Programming paradigm.
In JavaScript the class construct is just a syntactic simplification of the approaches to create objects we have already seen. The JavaScript class construct provides a much simpler and clearer syntax for managing constructors, prototypes, and inheritance.

Let's take a look at what a class looks like:
```ruby
class Person {
    constructor(name, surname) {
        this.name = name;
        this.surname = surname;
      }
}
```
classes are just syntactic sugar for the constructor's definition.
a class is a collection of methods included in braces and identified by a name.One of these methods is the constructor() method, whose task is to define and initialize the properties.
The constructor of a class is a method with the reserved name constructor . You cannot have more than one constructor() method in a class.

## OOP Principles

The principles of Object oriented languages are:

### ENCAPSULATION
Encapsulation is the principle of information hiding.The ability to concentrate in one entity both data(properties) and functions (methods), hiding the internal details.
In other words, the encapsulation principle allows an object to expose just what is needed touse it, hiding the complexity of its implementation.
Example: we drive cars. We need just to know how to speed up,brake, and change direction. We do not need to know how the car works in detail, how itsmotor burns fuel or transmits movement to the wheels.
Another	aspect	of	information	hiding	is	the	visibility	of	methods	and	properties.	In	some languages,	objects	can	have	 public ,	 private ,	and	 protected 	methods	and	properties.	This categorization	defines	the	level	of	access	the	users	of	the	object	have.	For	example,	only	the methods	of	the	same	object	have	access	to	the	 private 	methods,	while	anyone	has	access	to	the public 	ones.	In	JavaScript,	all	methods	and	properties	are	 public ,	but	we'll	see	that	there	are ways	to	protect	the	data inside	an	object	and	achieve	privacy.

Approaches to implement the visibility and accessibility of members of a JavaScript object:
1. **Public and  Private Properties**.
Many object-oriented languages, such as Java and C#, provide specific keywords such as public and private (access modifiers) to allow developers to easily implement the Information Hiding principle. JavaScript does not include such keywords. All members in
an object are public by default.However, some common patterns can be used to obtain different levels of information hiding as happens in most classical OOP languages.
JavaScript objects do not care about privacy. All the properties and methods are publicly
accessible if no caution is taken. So, if we want to avoid access to some properties or
methods concerning internal implementation details, we have to set up a strategy.

2. **Scope and Closure**.

### INHERITANCE

Inheritance	is	an elegant	way	to	reuse	existing	code.It enables new objects to acquire the properties of existing objects.
In	classical	OOP, classes	inherit	from	other	classes,	but	in	JavaScript,	as	there	are	no	classes, objects	inherit	from	other	objects.

### POLYMORPHISM

The ability to call the same	method	on different	objects, and	have each	of	them	respond	in	their	own	way,	is	called polymorphism.
In most languages, overloading is what happens when you have two methods with the same name but different signatures.
