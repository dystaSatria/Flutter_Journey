# Introduction to Dart

## Hello World

Every app requires the top-level `main()` function, where execution starts. To display text on the console, use the `print()` function:

```dart
void main() {
  print('Hello, World!');
}
```

## Variables
In Dart, you can declare most variables without explicitly specifying their type using var:

```dart
var name = 'Voyager I';
var year = 1977;
var antennaDiameter = 3.7;
var flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune'];
var image = {
  'tags': ['saturn'],
  'url': '//path/to/saturn.jpg'
};
```

## Control Flow Statements
Dart supports the usual control flow statements like if, for, and while:

```dart
Copy code
if (year >= 2001) {
  print('21st century');
} else if (year >= 1901) {
  print('20th century');
}

for (final object in flybyObjects) {
  print(object);
}

for (int month = 1; month <= 12; month++) {
  print(month);
}

while (year < 2016) {
  year += 1;
}
```

# Functions
It's recommended to specify the types of function arguments and return values:

```dart

int fibonacci(int n) {
  if (n == 0 || n == 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

var result = fibonacci(20);
```

## Comments
Comments in Dart usually start with // for single-line comments and /* */ for multi-line comments:

dart
Copy code
// This is a normal, one-line comment.

/// This is a documentation comment, used to document libraries, classes, and their members.

/* Comments like these are also supported. */
Read more about comments in Dart

Imports
To access APIs defined in other libraries, use the import statement:

dart
Copy code
import 'dart:math'; // Importing core libraries

import 'package:test/test.dart'; // Importing libraries from external packages

import 'path/to/my_other_file.dart'; // Importing files
Read more about libraries and visibility in Dart

Classes
Here's an example of a class Spacecraft:

dart
Copy code
class Spacecraft {
  String name;
  DateTime? launchDate;

  // Constructor, with syntactic sugar for assignment to members.
  Spacecraft(this.name, this.launchDate) {
    // Initialization code goes here.
  }

  // Method.
  void describe() {
    print('Spacecraft: $name');
    // Rest of the method...
  }
}
Read more about classes in Dart

Enums
Enums are used to enumerate a predefined set of values:

dart
Copy code
enum PlanetType { terrestrial, gas, ice }

enum Planet {
  mercury,
  venus,
  // Rest of the planets...
}
Read more about enums in Dart

Inheritance
Dart supports single inheritance:

dart
Copy code
class Orbiter extends Spacecraft {
  double altitude;

  Orbiter(String name, DateTime launchDate, this.altitude) : super(name, launchDate);
}
Read more about inheritance in Dart

Mixins
Mixins are a way of reusing code in multiple class hierarchies:

dart
Copy code
mixin Piloted {
  int astronauts = 1;

  void describeCrew() {
    print('Number of astronauts: $astronauts');
  }
}
Read more about mixins in Dart

Interfaces and Abstract Classes
All classes implicitly define an interface. You can create an abstract class to be extended (or implemented) by a concrete class:

dart
Copy code
abstract class Describable {
  void describe();
}
Read more about interfaces and abstract classes in Dart

Async/Await
Dart supports asynchronous programming with async and await:

dart
Copy code
Future<void> printWithDelay(String message) async {
  await Future.delayed(Duration(seconds: 1));
  print(message);
}
Read more about asynchrony support in Dart

Exceptions
To raise an exception, use throw. To catch an exception, use a try statement:

dart
Copy code
if (astronauts == 0) {
  throw StateError('No astronauts.');
}

try {
  // Code that might throw an exception.
} on Exception catch (e) {
  // Handling the exception.
} finally {
  // Code that always runs, regardless of an exception.
}
Read more about exceptions in Dart

Important Concepts
Everything in Dart is an object.
Dart supports strong typing but allows type inference.
Null safety was introduced in Dart 2.12.
Dart supports generic types, top-level functions, variables, etc.
Dart doesn't have public, protected, private keywords; it uses underscore _ for privacy.
Dart supports expressions and statements, and provides warnings and errors.
