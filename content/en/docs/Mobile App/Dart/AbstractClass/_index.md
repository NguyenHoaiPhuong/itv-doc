---
title: "Abstract Classes and Abstract Methods"
linkTitle: "Abstract Classes and Abstract Methods"
weight: 6
description: >
  Dart - Abstract Classes and Abstract Methods.
---

## Introduction

* An **abstract class** is a type of class that cannot be instantiated directly which means an object cannot be created from it.
* An abstract class cannot be instantiated but they can be sub-classed.
* To define an abstract class we use abstract keyword.

## The syntax for defining Abstract Class

```
abstract class class_name {
  // Body of abstract class
}
```

## Abstract Methods

* Abstract methods can only exist within an abstract class.
* To make a method abstract, use a semicolon (;) instead of the method body.

```
void talk (); // Abstract method
void walk (); // Abstract method
```

* Normal classes can extend the abstract class, but they have to override every abstract method.
* You can also create normal methods in the abstract class. And to override normal method is not mandatory.
* The abstract class will only complain when you don’t override the abstract method.

## Sample Code

```
abstract class Person{
  void walk();  //Abstract Method
  void talk();  //Abstract Method
}
class Jay extends Person{
  @override
  void walk() {
    print("Jay can walk");
  }
  @override
  void talk() {
    print("Jay can talk");
  }
}
main(){
  Jay jay = new Jay();
  jay.talk();
  jay.walk();
}

Output
Jay can talk
Jay can walk
```

## Difference between Abstract class and Interface

<table class="table-2">
  <colgroup>
    <col class="fifty" />
    <col class="fifty" />
  </colgroup>

  <tr>
    <th>Abstract class</th>
    <th>Interface</th>
  </tr>

  <tr>
    <td>Abstract class cannot be instantiated.</td>
    <td>Interface, as a normal class, can be instantiated.</td>
  </tr>
  <tr>
    <td>Abstract methods can be created here.</td>
    <td>Abstract methods cannot be created here.</td>
  </tr>
  <tr>
    <td>When abstract class is extended by other classes, only abstract methods need to override.</td>
    <td>When interface is implemented in other classes, all methods and instance variables needs to override.</td>
  </tr>
  <tr>
    <td>We can only extend one abstract class.</td>
    <td>We can implement multiple interfaces.</td>
  </tr>
</table>