# Day 2 

## 1. In the big_text.dart

```dart
 @override
  Widget build(BuildContext context) {
    return Text(
         text,
         maxLines: 1,
         overflow: overflow, //we use this overflow so we use maxLines = 1; If there property or 
         style: TextStyle(
          color: color,
          fontSize: size,
          fontFamily: 'Roboto',
          fontWeight: FontWeight.w400
         ),
    );
  }
```
