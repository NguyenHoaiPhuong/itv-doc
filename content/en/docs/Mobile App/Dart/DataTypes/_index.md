---
title: "Data Types"
linkTitle: "Data Types"
weight: 4
description: >
  Dart Programming - Data Types.
---

The Dart language supports the following types:

- Numbers
- Strings
- Booleans
- Lists
- Maps

## Numbers

The Number Dart come in two flavours:

- Integer: `int` keyword.

- Double: `double` keyword.

## Strings

Strings represent a sequence of characters. A Dart string is a sequence of `UTF-16` code units. `Runes` are used to represent a sequence of `UTF-32` code units. 

String values are embedded in either single or double quotes.

## Boolean

Boolean values true and false. Dart uses the `bool` keyword to represent a Boolean value.

## List and Map

The data types list and map are used to represent a collection of objects.

- A List is an ordered group of objects. The List data type in Dart is synonymous to the concept of an array in other programming languages.
- A Map data type represents a set of values as key-value pairs.

## The Dynamic Type

Dart is an optionally typed language. If the type of a variable is not explicitly specified, the variable’s type is dynamic. The `dynamic` keyword can also be used as a type annotation explicitly.

## Final and Const

The `final` and `const` keyword are used to declare constants. Dart prevents modifying the values of a variable declared using the final or const keyword. These keywords can be used in conjunction with the variable’s data type or instead of the `var` keyword.

### Const

Syntax: `const` keyword

```
const variable_name
const data_type variable_name
```

The `const` keyword is used to represent a compile-time constant. Variables declared using the const keyword are implicitly final.

If the value you have is computed at runtime (new DateTime.now(), for example), you cannot use a `const` for it. However, if the value is known at compile time (const a = 1;), then you should use `const` over `final`. There are 2 other large differences between `const` and `final`. Firstly, if you're using `const`, you have to declare it as static const rather than just `const`. Secondly, if you have a `const` collection, everything inside of that is in `const`. If you have a `final` collection, everything inside of that is not `final`.

Example:

```
void main() { 
   const pi = 3.14; 
   const area = pi*12*12;
   print("The output is ${area}");
}
```

### Final

Syntax: `final` Keyword

```
final variable_name
final data_type variable_name
```

`final` means single-assignment: a `final` variable or field must have an initializer. Once assigned a value, a `final` variable's value cannot be changed. final modifies variables.

`final` should be used over `const` if you don't know the value at compile time, and it will be calculated/grabbed at runtime. If you want an HTTP response that can't be changed, if you want to get something from a database, or if you want to read from a local file, use final. Anything that isn't known at compile time should be `final` over `const`.

Example:

```
void main() { 
   final val1 = 12; 
   print(val1); 
}
```