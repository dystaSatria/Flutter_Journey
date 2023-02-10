# CONST & VAR 


## CONST
- [Block scoped variables](https://www.section.io/engineering-education/variables-in-javascript/#:~:text=Block%20scoped%20variables%3A%20A%20block,block%20is%20inside%20a%20function.) 
 - Value can’t be redeclared.

#### Example
```dart
void main(){
  const animal = 'shark';
  animal = 'killer whale';
  print(animal);
  }
```

#### Output
```
Error: Can't assign to the const variable 'animal'.
  animal = 'killer whale';
  ^^^^^^
Error: Compilation failed.

```

## Var
- Function-scoped variables and globally-scoped variables.
- Value can be redeclared.

```dart
void main(){
 
  var lesson = "Science";
   lesson = "Music & Art";
  print(lesson);
}
```
```
Music & Art

```





