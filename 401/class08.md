# OO Design

## [SOLID principles intro](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)

- SOLID is an acronym for the first five object-oriented design (OOD) principles by Robert C. Martin (also known as Uncle Bob).
-  SOLID stands for:  
**S** - Single-responsiblity Principle(SRP)  
**O** - Open-closed Principle(OCP)  
**L** - Liskov Substitution Principle  
**I** - Interface Segregation Principle  
**D** - Dependency Inversion Principle  

```
Single-responsibility Principle (SRP) states:
A class should have one and only one reason to change, meaning that a class should have only one job.
```
```
Open-closed Principle (OCP) states:
Objects or entities should be open for extension but closed for modification.
```
OCB means the class should be extendable without modifying the class itself.

```
Interface segregation principle states:
A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.
```

```
Dependency inversion principle states:
Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.
```



## [OO SOLID principles in real life](https://dzone.com/articles/the-solid-principles-in-real-life)

### SOLID

- **S** Single-responsiblity Principle

By way of counter-example, classes are doing too much, in terms of the srp:
 1. consider a class that opens a connection to the database, pulls out some table data, and modify the data to a file. 

A good Example why to use SRP:
2. "duck" vehicles are street legal and water-capable, there are millions of families out there that own both cars and boats, but rare to find who own a duck vechile,why? maybe because no one wants to be unable to drive to work because their boat rudder is broken. 

- **O** Open-closed Principle

People should't change your class later. 

A good Example:

- Smartphones, App stores let you extend the base functionality of the phone.
And by that The core phone functionality closed for modification and open to an extension .

- **L** - Liskov Substitution Principle  

LSP says, `that any child type of a parent type should be able to stand in for that parent without things blowing up.`

As A cat and dog are child for animal class, cats should meow, dogs should bark, and not the vice versa.


- **I** - Interface Segregation Principle 

Real world Example:
- As in restaurant's menu. you'll see all of the normal menu mainstays, and then something that's just called "soup of the day."
 Clients that don't care about the soup needn't even be concerned, and clients that do use a different interface -- asking the server.

**D** - Dependency Inversion Principle 

- As going to store and pay for something with a credit card. the clerk doesn't examine your card. he just takes your card, whatever it is, and swipes it. 



