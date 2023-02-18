# Stuff


## 1
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
<br>
<br>

## 2. Flutter Package Project Name

- The name should be all lowercase, with underscores to separate words.
  Example:
```just_like_this.``` or ```test_program```
- Space and special characters are not allowed on the app name.
 Example : 
 ```	
!	"	#	$	%	&	'	(	)	*	+	,	‑	.	/
 ```
 - It doesn’t start with digits and isn’t a reserved word.

<br>
<br>

## 3. The First Page while run

The first page while run is in the 
```
return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        // This is the theme of your application.
        //
        // Try running your application with "flutter run". You'll see the
        // application has a blue toolbar. Then, without quitting the app, try
        // changing the primarySwatch below to Colors.green and then invoke
        // "hot reload" (press "r" in the console where you ran "flutter run",
        // or simply save your changes to "hot reload" in a Flutter IDE).
        // Notice that the counter didn't reset back to zero; the application
        // is not restarted.
        primarySwatch: Colors.blue,
      ),
      home: MainFoodPage(),//this the start class while you run it
    );,
    ```

## 3. When we use const or not


