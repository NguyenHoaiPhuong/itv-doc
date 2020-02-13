---
title: "Interface"
linkTitle: "Interface"
weight: 7
description: >
  Dart - Interface.
---

## Introduction

* The interface defines the syntax that any class must follow. Interface mostly used to apply compulsion on class.
* When any class implements an Interface then it must override every method and instance variable of an interface.
* However, Dart does not have a syntax for declaring interfaces. The class declaration is themselves interface in a dart.
* Any class can act as an interface. Classes can use implements keyword to use any class as an interface.
* Once any class is used as interface then it is mandatory to override each and every method and instance variable of that class. In simple words, a class must redefine every method and instance variable of the interface.

## Syntax of declaring Interface

```
class class_name implements interface_name
```

## Sample Code

```
class Person {
  
  void walk() {
    print("Person can walk");
  }

  void talk() {
    print("Person can talk");
  }
}
class Jay implements Person {
  
  @override
  void walk() {
    print("Jay can walk");
  }

  @override
  void talk() {
    print("Jay can talk");
  }
}

main() {
  Person person = new Person();
  Jay jay = new Jay();

  person.walk();
  person.talk();

  jay.walk();
  jay.talk();
}

Output
Person can walk
Person can talk
Jay can walk
Jay can talk
```

## Implementing Multiple Interface

Dart does not support multiple inheritance but dart can implement multiple interfaces. To provide similar power and functionality.

### The syntax for declaring multiple interfaces

```
class class_name implements interface1, interface2, interface3
```

### Sample Code

```
class Person {
  String name;

  void ShowName() {
    print("My name is $name");
  }

  void walk() {
    print("Person can walk");
  }

  void talk() {
    print("Person can talk");
  }
}

class Viveki {
  String profession;

  void ShowProfession() {
    print("from class Viveki my profession is $profession");
  }
}

class Jay implements Person, Viveki {
  @override
  String profession;

  @override
  void ShowProfession() {
    print("from class Jay my Profession is $profession");
  }
@override 
  String name; 
 
  @override 
  void ShowName() { 
    print("From class Jay my name is $name"); 
  } 
 
  @override 
  void walk() { 
    print("Jay can walk"); 
  } 
 
  @override 
  void talk() { 
    print("Jay can talk"); 
  } 
} 
 
main() { 
  Person person = new Person(); 
  Jay jay = new Jay(); 
  Viveki viveki = new Viveki(); 
 
  person.walk(); 
  person.talk(); 
  person.name = "Person"; 
  person.ShowName(); 
 
  print(""); 
 
  jay.walk(); 
  jay.talk(); 
  jay.name = "JAY"; 
  jay.profession = "Software Development"; 
  jay.ShowProfession(); 
  jay.ShowName(); 
 
  print(""); 
 
  viveki.profession = "Chemical Engineer"; 
  viveki.ShowProfession(); 
}
Output
Person can walk
Person can talk
My name is Person

Jay can walk
Jay can talk
from class Jay my Profession is Software Development
From class Jay my name is JAY

from class Viveki my profession is Chemical Engineer
```