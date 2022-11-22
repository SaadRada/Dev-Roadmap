# Dart Progrramming Language

![dart](https://soject.com/wp-content/uploads/2021/07/Dart-Tutorial.png)

Dart is a programming language designed for client development, such as for the web and mobile apps. It is developed by Google and can also be used to build server and desktop applications. It is an object-oriented, class-based, garbage-collected language with C-style syntax

## Hello World

Every app has a main() function. To display text on the console, you can use the top-level print() function:

```
void main() {
  print("Hello World");
}
```

## Variables

- **Declaration**
  ```
  var name = value;
  DataType name = value;
  ```
- **Concatination**

  ```
  var name = "Saad";
  var lastName = "Rada";

  print("The Full Name is $name $lastName");
  ```

## Data Type

- String
  ```
  String name = "Saad";
  ```
- int
  ```
  int age = 21;
  ```
- double
  ```
  double rate = 4.5;
  ```
- num
- List (Array)

  ```
  List countries = [];
  countries.add("Morocco");
  countries.add("Egypt");
  countries.add("Tunisia");

  print(countries);
  print(countries[0]);
  ```

- Map (Object)

  ```
  Map data = Map();
  data['id'] = 1;
  data['name'] = "saad";
  data['age'] = 21;

  print(data);
  print(data['id']);
  ```

- bool

  ```
  bool isClicked = false
  ```

- **Null safety**

  ```
  String name;
  string? lastName; // ? could be null

  print(name); // error
  print(lastName); // null
  ```

- **Late**
  ```
  late String name; // this variable will get a value later
  ```

## Arithmetic, Logical operators

it's the same for javascipt

## Check data type

we can check data type in dart by **is** keyword and the result is a boolean value

```
String name = "saad";

print(name is String); // true
print(name is int); // false
```
