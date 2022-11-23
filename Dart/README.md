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
  var is a dynamic data type
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

- toString()
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

## String Methods

- isEmpty
- length
- toLowerCase()
- toUpperCase()
- trim()
  ... same for javascript

## List Methods

- **Declaration**
  ```
  List name = [];
  ```
- **Indexing**

  ```
  List numbers = [1, 2, 3, 4, 5];

  print(umbers[0]); // 1
  ```

- **add**

  ```
  List numbers = [1, 2, 3];

  numbers.add(4);

  print(numbers); // [1, 2, 3, 4]
  ```

- **length**

  ```
  List numbers = [1, 2, 3, 4];

  print(numbers.length); // 4
  ```

- **first and lasr **

  ```
  List numbers = [1, 2, 3, 4];

  print(numbers.first); // 1
  print(numbers.last); // 4
  ```

- **isEmpty**
- **isNotEmpty**
- **reversed**

  ```
  List numbers = [1, 2, 3, 4];

  print(numbers.reversed.toList()); // [4, 3, 2, 1]
  ```

- **addAll**
  add list to list

  ```
  List numbers = [1, 2, 3];

  print(numbers.add([4, 5, 6])); // [1, 2, 3, [4, 5, 6]]
  print(numbers.addAll([4, 5, 6])); // [1, 2, 3, 4, 5, 6]
  ```

- **insert**

  ```
  List x = [1, 2, 3];

  x.insert(0, 4); // add in the first
  ```

- **insertAll** : insert list in spesefic position
- **remove**

  ```
  List x = [1, 2, 3];
  x.remove(2);

  print(x); // [1, 3]
  ```

- **removeAt**

  ```
  List x = [1, 2, 3];
  x.removeAt(0);

  print(x); [2, 3]
  ```

- **removeRange**

  ```
  List x = [1, 2, 3, 4, 5];

  x.removeRange(0,2);

  print(x); // [3, 4, 5]
  ```

## Map Methods

```
Map data = {
  'id': 1,
  'name' : 'saad',
  'age' : 21
};
```

- **addAll** : add in the last or update if key already exist
- **isEmpty** : check is empty : bool
- **isNotEmpty** : check is not empty : bool
- **keys** : get only keys
- **values** : get only values
- **length** : get length
- **remove** : remove with key
- **clear** : clear the map

## Functions

- **Decalaration**

  ```
  funcName() {
    // code
  }

  funcName(); // call
  ```

- **with parametrs**

  ```
  calculate(int a, int b) {
    return a + b;
  }

  print(calculate(3, 2)); // 5
  ```

- **Arrow Function**

  ```
  calculat(int a, int b) => a + b;

  print(calculate(3, 2)); // 5
  ```

## Assert

The assert statement is a useful tool to debug the code and it uses boolean condition for testing. If the boolean expression in assert statement is true then the code continues to execute, but if it returns false then the code ends with Assertion Error.

```
let a;
assert(a == null, "message"); // get error before printing a
print(a);
```

**note** : this is before the null safety, but now we can use only null safety withot assert

```
let a; // give error a can't be null withot null safety
print(a);
```

## Math functions

- Max()
- Min()
- sqrt()
- sin()
- cos()
- tan()
- ...
