---
title: "Architecture Application"
linkTitle: "Architecture Application"
weight: 4
description: >
  Flutter - Architecture Application.
---

In this chapter, let us discuss the architecture of the Flutter framework.

## Widgets

The core concept of the Flutter framework is **In Flutter, Everything is a widget**. Widgets are basically user interface components used to create the user interface of the application.

In Flutter, the application is itself a widget. The application is the top - level widget and its UI is build using one or more children (widgets), which again build using its children widgets. This composability feature helps us to create a user interface of any complexity.

For example, the widget hierarchy of the hello world application (created in previous chapter) is as specified in the following diagram:

<img class="center-small" src="hello_world_application.jpg">

Here the following points are worth notable:

* `MyApp` is the user created widget and it is built using the Flutter native widget, `MaterialApp`.
* `MaterialApp` has a home property to specify the user interface of the home page, which is again a user created widget, `MyHomePage`.
* `MyHomePage` is built using another flutter native widget, `Scaffold`.
* `Scaffold` has two properties – body and appBar
* `body` is used to specify its main user interface and appBar is used to specify its header user interface
* `Header UI` is built using flutter native widget, `AppBar` and `Body UI` is built using `Center` widget.
* The `Center` widget has a property, `Child`, which refers the actual content and it is built using `Text` widget

## Gestures

Flutter widgets support interaction through a special widget, `GestureDetector`. `GestureDetector` is an invisible widget having the ability to capture user interactions such as tapping, dragging, etc., of its child widget. Many native widgets of Flutter support interaction through the use of GestureDetector. We can also incorporate interactive feature into the existing widget by composing it with the GestureDetector widget. We will learn the gestures separately in the upcoming chapters.