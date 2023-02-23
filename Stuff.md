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

## 4. When we use const or not

Can not define a const contructor for a class with non final field
Example :
```dart
 final Color? color;
  final String text;
  double size;
  TextOverflow overflow;

  const BigText({Key? key, this.color, 
  required this.text, 
  this.size = 20,
  this.overflow = TextOverflow.ellipsis
  }) : super(key: key);
```
Because there is a non final field like ```double size```, so the you must remove the ```const```.


## 5. 

We cannot call as varieble, property or same as thing to the section above :

```dart
class BigText extends StatelessWidget {
  Color? color;
  final String text;
  double size;
  TextOverflow overflow;

  BigText({Key? key, this.color = , 
  required this.text, 
  this.size = 20,
  this.overflow = TextOverflow.ellipsis
  }) : super(key: key);

```
You must call same thing like const hexadecimal like ```const Color(0xFFfcab88);```


## 6. Dropdown Icon (Header Section ) 

```dart
Row(
     children: [
        SmallText(text: "Cirebon", color: Colors.black54,),
        Icon(Icons.arrow_drop_down_rounded )
          ],
)
```

## 7. 
```dart
class _FoodPageBodyState extends State<FoodPageBody> {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: PageView.builder(
        itemCount: 5, //5 items
        itemBuilder : (context, position){ //position 0-4
          return Container();
        } ),
    );
  }
}
```
* itemCount is the total item (if 5 mean there are 5 items but in position is mean 0-4)

## 8. Margin in Flutter

```dart
margin: EdgeInsets.only(left: 5, right:5 ),
```

## 9. Rounded our picture

```dart
decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(30) ),
    );
```
* Add this in your container 


## 10. Fit our picture in the cover

```dart
Widget _buildPageItem(int index){ // this section is like for food slides
    return Container(
      height:  220,
      margin: EdgeInsets.only(left: 5, right:5 ),
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(30) ,
        color: index.isEven?Color(0xFF69c5df) : Color(0xFF9294cc),
        image: DecorationImage(

          fit: BoxFit.cover, // fit the photo in our cover photo
          image: AssetImage(
            "assets/image/food1.jpg"
          )
        )
      )
    );
```    
* Focus to the ```fit: BoxFit.cover```

## 11.

```dart
 Widget _buildPageItem(int index){ // this section is like for food slides
    return Stack(
      children: [
        Container(
      height:  220,
      margin: EdgeInsets.only(left: 5, right:5 ),
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(30) ,
        color: index.isEven?Color(0xFF69c5df) : Color(0xFF9294cc),
        image: DecorationImage(

          fit: BoxFit.cover, // fit the photo in our cover photo
          image: AssetImage(
            "assets/image/food1.jpg"
          )
        )
      )
    )
      ],
    );
```

* Stack Widget is widget in flutter SDK which allows us to make a layer of widgets by putting them on top of each other. 

## 12. 

```dart
 Widget build(BuildContext context) {
    return Container(
      color: Colors.redAccent,
      height: 320,
      child: PageView.builder(
        itemCount: 5, //5 items
        itemBuilder : (context, position){ //position 0-4
          return _buildPageItem(position);
        } ),
    );
  }

  Widget _buildPageItem(int index){ // this section is like for food slides
    return Stack(
      children: [
        Container(
      height:  220,
      margin: EdgeInsets.only(left: 5, right:5 ),
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(30) ,
        color: index.isEven?Color(0xFF69c5df) : Color(0xFF9294cc),
        image: DecorationImage(

          fit: BoxFit.cover, // fit the photo in our cover photo
          image: AssetImage(
            "assets/image/food1.jpg"
          )
        )
      )
    )
      ],
    );
```
* If we make comment (//) the ```height:200``` section's height will join the ```height :320```    
