---
title: "Syntax"
linkTitle: "Syntax"
weight: 3
description: >
  Dart Programming - Syntax.
---

Syntax defines a set of rules for writing programs. Every language specification defines its own syntax. A Dart program is composed of :

- Variables and Operators
- Classes
- Functions
- Expressions and Programming Constructs
- Decision Making and Looping Constructs
- Comments
- Libraries and Packages
- Typedefs
- Data structures represented as Collections / Generics

## First Dart code

```
main() {
  print("Hello World!")
}
```

The main() function is a predefined method in Dart. This method acts as the **entry point** to the application. A Dart script needs the main() method for execution. print() is a predefined function that prints the specified string or value to the standard output i.e. the terminal.

The output of the above code will be:

```
Hello World!
```

## Execute a Dart Program

You can execute a dart program in 2 ways:

- Via the terminal
- Via the WebStorm IDE

### Via the terminal

- Navigate to the path of the current project
- Type the following command in the Terminal window

```
dart file_name.dart
```

### Via the WebStorm IDE

TO UPDATE

## Dart Command-Line Options

<table class="table-2">
  <colgroup>
    <col class="thirty" />
    <col class="seventy" />
  </colgroup>

  <tr>
    <th>Sr.No</th>
    <th>Command-Line Option & Description</th>
  </tr>

  <tr>
    <td>1</td>
    <td>
      <p><b>--enable-asserts</b></p>
      <p>Enables assertions.</p>
    </td>
  </tr>

  <tr>
    <td>2</td>
    <td>
      <p><b>--version</b></p>
      <p>Displays VM version information.</p>
    </td>
  </tr>

  <tr>
    <td>3</td>
    <td>
      <p><b>--package&ltpath&gt</b></p>
      <p>Specifies the path to the package resolution configuration file.</p>
    </td>
  </tr>

  <tr>
    <td>4</td>
    <td>
      <p><b>-p&ltpath&gt</b></p>
      <p>Specifies where to find imported libraries. This option cannot be used with --packages.</p>
    </td>
  </tr>

  <tr>
    <td>5</td>
    <td>
      <p><b>-h or --help<path></b></p>
      <p>Displays help.</p>
    </td>
  </tr>
</table>

## Identifiers in Dart

Identifiers are names given to elements in a program like variables, functions etc. The rules for identifiers are: Identifiers can include both, characters and digits. However, the identifier cannot begin with a digit.

- Identifiers cannot include special symbols except for underscore (_) or a dollar sign ($).
- Identifiers cannot be keywords.
- They must be unique.
- Identifiers are case-sensitive.
- Identifiers cannot contain spaces.

The following table lists a few examples of valid and invalid identifiers:

<table class="table-2">
  <colgroup>
    <col class="thirty" />
    <col class="seventy" />
  </colgroup>

  <tr>
    <th>Valid identifiers</th>
    <th>Invalid identifiers</th>
  </tr>

  <tr>
    <td>firstName</td>
    <td>Var</td>
  </tr>

  <tr>
    <td>first_name</td>
    <td>first name</td>
  </tr>

  <tr>
    <td>num1</td>
    <td>first-name</td>
  </tr>

  <tr>
    <td>$result</td>
    <td>1number</td>
  </tr>
</table>

## Keywords in Dart

The following table lists some keywords in dart:

<table class="table-2" border="1">
  <tr>
    <td>abstract</td>
    <td>continue</td>
    <td>false</td>
    <td>new</td>
    <td>this</td>
    <td>as</td>
    <td>default</td>
    <td>final</td>
    <td>null</td>
    <td>throw</td>
    <td>assert</td>
    <td>deferred</td>
  </tr>

  <tr>
    <td>finally</td>
    <td>operator</td>
    <td>true</td>
    <td>async</td>
    <td>do</td>
    <td>for</td>
    <td>part</td>
    <td>try</td>
    <td>async*</td>
    <td>dynamic</td>
    <td>get</td>
    <td>rethrow</td>
  </tr>

  <tr>
    <td>typedef</td>
    <td>await</td>
    <td>else</td>
    <td>if</td>
    <td>return</td>
    <td>var</td>
    <td>break</td>
    <td>enum</td>
    <td>implements*</td>
    <td>set</td>
    <td>void</td>
    <td>case</td>
  </tr>

  <tr>
    <td>export</td>
    <td>import</td>
    <td>static</td>
    <td>while</td>
    <td>catch</td>
    <td>external</td>
    <td>in</td>
    <td>super</td>
    <td>with</td>
    <td>class</td>
    <td>extends</td>
    <td>is</td>
  </tr>

  <tr>
    <td>switch</td>
    <td>yield</td>
    <td>const</td>
    <td>factory</td>
    <td>library</td>
    <td>sync*</td>
    <td>yield*</td>
  </tr>
</table>

## Whitespace and Line Breaks

Dart ignores spaces, tabs and new lines that appear in programs. 

## Dart is Case-sensitive

This means that Dart differentiates between uppercase and lowercase characters.

## Statements end with a Semicolon

Each line of instruction is called a statement. Each dart statement must end with a semicolon (;). A single line can contain multiple statements. However, these statements must be separated by a semicolon.

## Comments in Dart

Dart supports the following types of comments:

* **Single-line comments** ( // ) − Any text between a "//" and the end of a line is treated as a comment
* **Multi-line comments** (/* */) − These comments may span multiple lines.

Example:

```
// this is single line comment  
  
/* This is a   
   Multi-line comment  
*/ 
```

## Object-Oriented Programming in Dart

Dart is an Object-Oriented language. Object Orientation is a software development paradigm that follows real-world modelling. Object Orientation considers a program as a collection of objects that communicate with each other via mechanism called methods.

* **Object** − An object is a real-time representation of any entity. As per Grady Brooch, every object must have three features:
  * **State** − described by the attributes of an object.
  * **Behavior** − describes how the object will act.
  * **Identity** − a unique value that distinguishes an object from a set of similar such objects.

* **Class** − A class in terms of OOP is a blueprint for creating objects. A class encapsulates data for the object.

* **Method** − Methods facilitate communication between objects.

Example:

```
class TestClass {   
   void disp() {     
      print("Hello World"); 
   } 
}  
void main() {   
   TestClass c = new TestClass();   
   c.disp();  
}
``

The above example defines a class **TestClass**. The class has a method `disp()`. The method prints the string “Hello World” on the terminal. The `new` keyword creates an object of the class. The object invokes the method `disp()`.

The code should produce the following output:

```
Hello World
```