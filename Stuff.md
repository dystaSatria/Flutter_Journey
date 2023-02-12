# Stuff


#### 1
```dart
import 'package:flutter/material.dart';

String getFullName(String firstName, String lastname) => '$firstName $lastname'; //this section

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});
  
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    print(getFullName('Reza', 'Satria'));  //this section
    return MaterialApp(
        debugShowCheckedModeBanner: false,
       home: Scaffold(
        appBar: AppBar( 
          title: const Text('App Title'),
        ),
        body: const Text("Body \nAku suka makan mie goreng"),
      ),
       
    );
  }
}
```

# 2

- The name should be all lowercase, with underscores to separate words.
  Example:
  ```just_like_this.```
  or ```test_program```
