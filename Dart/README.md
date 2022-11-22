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
print(name is! String); // false
is! == is not
```

## Assignement opertor

```
int age = 21;
int price;

age ??= 33; // if age null assign the value
price ??= 300;
print(age); // 21
print(price); // 300
```

## Control Flow (if else, loops)

the same for javascipt

## Number Methods

- isFinite
- isInfinite
- isNegative
- sign

  ```
  var x = 10;
  var y = -30;

  print(x.sign); // 1
  print(y.sign); // -1

  return 1 if positive
  return -1 is negative
  return 0 is number equal to 0
  ```

- isEven

  ```
  var x = 2;
  var y = 3;

  print(x.isEven); // true 2 % 2 = 0
  print(y.isEven); // 3 % 2 != 0
  ```

- isOdd : Reverse of isEven
- abs() : return positive number
- ceil()

  ```
  double x = 1.2;

  print(x.ceil()); // 2
  ```

- round()

- compatTo() : compare two numbers

  ```
  int x = 10;

  print(x.comparTo(10)); // 0
  print(x.comparTo(21)); // -1
  print(x.comparTo(1)); // 1
  ```

- floor() : convert double to int
- toInt() : double to integer
- num.parse("10") : convert string to number
