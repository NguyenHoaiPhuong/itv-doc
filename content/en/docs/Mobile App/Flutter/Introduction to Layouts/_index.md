---
title: "Introduction to Layouts"
linkTitle: "Introduction to Layouts"
weight: 6
description: >
  Flutter - Introduction to Layouts.
---

Since the core concept of Flutter is **Everything is widget**, Flutter incorporates a user interface layout functionality into the widgets itself. Flutter provides quite a lot of specially designed widgets like `Container`, `Center`, `Align`, etc., only for the purpose of laying out the user interface. Widgets build by composing other widgets normally use layout widgets.

Let use learn the Flutter layout concept in this chapter.

## Type of Layout Widgets

Layout widgets can be grouped into two distinct category based on its child:

* Widget supporting a single child
* Widget supporting multiple child

Let us learn both type of widgets and its functionality in the upcoming sections.

## Single Child Widgets

In this category, widgets will have **only one** widget as its **child** and every widget will have a special layout functionality.

For example:
* `Center` widget just centers it child widget with respect to its parent widget
* `Container` widget provides complete flexibility to place it child at any given place inside it using different option like padding, decoration, etc.

Single child widgets are great options to create high quality widget having **single functionality** such as button, label, etc.

The code to create a simple button using Container widget is as follows:

```
class MyButton extends StatelessWidget {
  MyButton({Key key}) : super(key: key); 

  @override 
  Widget build(BuildContext context) {
    return Container(
        decoration: const BoxDecoration(
          border: Border(
              top: BorderSide(width: 1.0, color: Color(0xFFFFFFFFFF)),
              left: BorderSide(width: 1.0, color: Color(0xFFFFFFFFFF)),
              right: BorderSide(width: 1.0, color: Color(0xFFFF000000)),
              bottom: BorderSide(width: 1.0, color: Color(0xFFFF000000)),
          ),
        ),
        child: Container(
          padding: const
          EdgeInsets.symmetric(horizontal: 20.0, vertical: 2.0),
          decoration: const BoxDecoration(
              border: Border(
                top: BorderSide(width: 1.0, color: Color(0xFFFFDFDFDF)),
                left: BorderSide(width: 1.0, color: Color(0xFFFFDFDFDF)),
                right: BorderSide(width: 1.0, color: Color(0xFFFF7F7F7F)),
                bottom: BorderSide(width: 1.0, color: Color(0xFFFF7F7F7F)),
              ),
              color: Colors.grey,
          ),
          child: const Text(
              'OK',textAlign: TextAlign.center, style: TextStyle(color: Colors.black)
          ), 
        ), 
    ); 
  }
}
```

Here, we have used two widgets – a Container widget and a Text widget. The result of the widget is as a custom button as shown below:

