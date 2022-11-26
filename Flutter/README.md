# Flutter

![Flutter](http://engineering.letsnurture.com/wp-content/uploads/2018/07/flutter.png)

## Introduction

Flutter is a free open source tool (Framework) that allows you to build native-cross-platform app with one programming language and codebase.

Flutter based on Dart, Dart is a programming language created by Google Focused on FrontEnd (Mobile apps, web) user interface UI developement

## Flutter architecture

Apps UI is a widget tree
![flutter architecture](https://docs.flutter.dev/assets/images/docs/arch-overview/platform-channels.png)

## Material Dessign

- Material is a design system created and used by Google
- It's not Google style for evryone! it's indeed highly customiable (and work on IOS devices too)
- Material Dessign is built into flutter but you also find Apple-styled (Cupertino) widgets

## Create Project

ther is a lot of ways to create flutter project (with command line, in vscode in android studio)

```
flutter create project_name
```

## main.dart

```
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Welcome to Flutter'),
        ),
        body: const Center(
          child: Text('Hello World'),
        ),
      ),
    );
  }
}
```

- **main** : the main accesible function that the program see
- **runapp** : takes the given Widget and makes it the root of the widget tree
- **@override** : as we know in dart tutorial the @override keyword tell us that this method is overrided from the origin class
- **super** : super is used to call the constructor of the base class
- **key** : Key is a type used in Flutter to identify widgets and allows Flutter to know when a widget that's moved in the tree is the same as a widget that was previously in a different location
- **stateLessWidget** : The app extends StatelessWidget, which makes the app itself a widget. In Flutter, almost everything is a widget, including alignment, padding, and layout.
- **build** : A widget's main job is to provide a build method that describes how to display the widget in terms of other, lower-level widgets.

### Stateful and stateless widgets

A widget is either stateful or stateless. If a widget can change—when a user interacts with it, for example—it's stateful. A stateless widget never changes. Icon , IconButton , and Text are examples of stateless widgets.
