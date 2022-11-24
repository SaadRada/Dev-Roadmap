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

- **String**
  ```
  String name = "Saad";
  ```
- **int**
  ```
  int age = 21;
  ```
- **double**
  ```
  double rate = 4.5;
  ```
- **num**
- **List** (Array)

  ```
  List countries = [];
  countries.add("Morocco");
  countries.add("Egypt");
  countries.add("Tunisia");

  print(countries);
  print(countries[0]);
  ```

- **Map** (Object)

  ```
  Map data = Map();
  data['id'] = 1;
  data['name'] = "saad";
  data['age'] = 21;

  print(data);
  print(data['id']);
  ```

- **bool**

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
- **get DataType**

  ```
  String name = 'saad';
  int age = 23;

  print(name.runtimeType); // String
  print(age.runtimeType); // int
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

- **sublist**
  sublist is used to get specefic part from other list
  **don't modify the origin list**

  ```
  // varNAme.sublist(start, end);
  List data = [1, 2, 3, 4, 5, 6];

  print(data.sublist(0, 2)); // [1, 2, 3]
  print(data.sublist(2)); // [3, 4, 5, 6]
  ```

- **shuffle**
  shuffle is used to sort randomly a list
  **modify the origin list**

  ```
  List data = [1, 2, 3, 4];

  print(data.shuffle()); // [2, 4, 1, 3]
  print(data.shuffle()); // [4, 2, 1, 3]
  print(data.shuffle()); // [1, 4, 2, 3]
  ```

- **whereType**
  create a new list with type verefication

  ```
  List data = ['saad', 1, 3, 'mehdi', 5, 'abdo'];

  var newList = data.whereType<int>().toList(); // get only integer
  ```

- **every and any**
  every and any method s return a boolean value based on a condition

  ```
  List data = ['saad', 'abdelmounim', 'mehdi'];

  var check = data.every((e) => e.length > 2); // true all names length grater than w
  var check2 = data.any((e) => e.length > 7); // return true becaus abdelmounim length grater than 7
  ```

- **take**
  Returns a lazy iterable of the [count] first elements of this iterable.
  ```
  final numbers = <int>[1, 2, 3, 5, 6, 7];
  final result = numbers.take(4); // (1, 2, 3, 5)
  final result = numbers.take(4).toList(); // [1, 2, 3, 5]
  final takeAll = numbers.take(100); // (1, 2, 3, 5, 6, 7)
  final takeAll = numbers.take(100).toSet(); // {1, 2, 3, 5, 6, 7}
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
- **asMap**
  convert List to Map with keys as indexes

  ```
  List data = ['saad', 'mehdi', 'abdo'];
  Map lisAsMAp = data.asMap();

  print(listAsMap); // {0: saad, 1: mehdi, 2: abdo}
  ```

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

## Iterable

An Iterable is a collection of elements that can be accessed sequentially and can apply map forEach ... to it

## OOP - Oriented Object Programming

- ### class

  ```
  void main() {
    Post php = new Post();
    php.title = 'php 8 Tutorial';
    php.date = '24-11-2022';
    ...
  }

  class Post {
    // properties
    String title;
    String date;
    int rating;
    List categories;
  }
  ```

- ### Methods

  method is a function inside a class

  ```
  void main() {
    Post php = new Post();
    php.title = 'php 8 Tutorial';
    php.date = '24-11-2022';
    ...
  }

  class Post {
    // properties
    ...

    void like() {
      likes ++;
    }
  }
  ```

- ### Constructor

  A class constructor is a special member function of a class that is executed whenever we create new objects of that class. A constructor will have exact same name as the class and it does not have any return type at all, not even void.

  ```
  class Post {
    // properties
    ...
    // contructor
    Post() {
      print("Hello from post");
    }

  }
  ```

- ### Reset Variables

  - **Dot Notation**

    ```
    void main() {
      Persone saad = new Persone();

      Person.name = 'saad';
    }
    class Person {
      Late String name;
      late String city;
      late int age;
    }
    ```

  - **Cascade Operator**
    ```
    void main() {
      Persone saad = new Persone()..name = 'saad'..city = 'casablanca';
    }
    class Person {
      Late String name;
      late String city;
      late int age;
    }
    ```
  - **With Constructor**

    ```
    void main() {
      Persone saad = new Persone();

      Person.name = 'saad';
    }
    class Person {
      Late String name;
      late String city;
      late int age;

      Person(name, city, age){
        this.name = name;
        this.city = city;
        this.age = age;
      } // old
      Person(this.name, this.city, this.age); // new
    }
    ```

- ### Getter and Setter

  Getter and setter methods are the class methods used to manipulate the data of the class fields. Getter is used to read or get the data of the class field whereas setter is used to set the data of the class field to some variable.

  ```
  void main() {
    Person saad = new Person();
    saad.setName = "Saad";
    print(saad.getName);
  }

  class Person {
    late String name;
    late String lastName;

    String get getName {
      return this.name;
    }

    set setName(String name) {
      this.name = name;
    }
  }
  ```

- ### Static properties and methods

  - Static properties and methods are used to access them in a global scope
  - Declaring class properties and methods as static makes them accessible without needding an anstantiation of the class
  - The pseudo-variable **this** is not available in static methods
  - A property declared as static cannot be accessed with an instantiated **without getter** class object (Though a static method can)

    ```
    void main() {
      print(Persone.name); // undifined
      print(Persone.age); // 21

      print(Personne.sayHello); // undifined
      print(Personne.sayBye); // Bye

      Person personOne = new Person();

      print(personOne.age); // can't be accessed through an instance
      personOne.sayBye; // Bye
    }

    class Person {
      static int age = 21;
      late String name;

      void sayHello() {
        print("Hello");
      }

      static void sayBye() {
        print("Bye");
      }
    }
    ```

- ### Cascade Operator

  The cascade notation (. .) in Dart allows you to make a sequence of operations on the same object (including function calls and field access). This notation helps keep Dart code compact and removes the need to create temporary variables to store data

  ```
  void main() {
    Persone mob = new Person();
    print(mob.mehodOme()); // method one
    print(mob.mehodTwo()); // method two

    new Person.methodOne(); // method one
    new Person.methodTwo(); // method two

    new Person..methodOne()..methodTwo(); // method one method two
  }

  class Person {

    void methodOne() {
      print('Method one');
    }
    void methodTwo() {
      print('Method two');
    }
  }
  ```

- ### Inheritance

  Inheritance in dart is defined as the process in which one class derive the properties and characteristics of another class. It is helpful as it provides an ability with which we can create a new class from an existing class

  ```
  class Mobile {
    String screen;
    String cpu;
    double price;
  }

  class Samsung extends Mobile {
    // has all Mobile Properties and can have others
    String brand = "Samsung";
  }
  ```

  **with constructor**
  The child class can inherit all properties (methods, variables) and behavior of parent expect parent class constructor. & The superclass constructor can be invoke in sub class by using the super() constructor. We can access both non-parameterized and parameterized constructor of superclass.

  ```
  void main() {
    Samsung s21 = new Samsung('samsung', 'cam', 'Dragon', '8');

    print(s21.brand);
    print(s21.camera);
    print(s21.cpu);
    print(s21.ram);
  }

  class Mobile {
    late String camera;
    late String cpu;
    late String ram;

    Mobile(this.camera, this.cpu, this.ram);
  }

  class Samsung extends Mobile {
    late String brand;

    Samsung(this.brand, camera, cpu, ram) : super(camera, cpu, ram);
  }

  ```

- ### Overide

  Method overriding occurs in dart when a child class tries to override the parent class's method. When a child class extends a parent class, it gets full access to the methods of the parent class and thus it overrides the methods of the parent class.

  ```
  class Mobile{
    String screen;

    printScreen(this.screen) {
      print(this.screen);
    }
  }

  class Samsung extends Mobile {
    String anotherScreen;

    @overide // this mean that this method will be overide the class parent method
    printScreen(this.anotherScreen) {
      print(this.anotherScreen);
    }
  }
  ```

- ### Abstract

  an abstract class can't be intansed, can only inherited

  ```
  void main() {
    Mobile samsung = new Mobile(); // error abstract class can'e be instansed
    Samsung s21 = new Samsung();
    print(s21.screen); // 6.5
  }
  abstract class Mobile {
    double screen = 6.2;
  }

  class Samsung extends Mobile {

  }
  ```

- ### Implement
  Dart considers class definitions to be interfaces. To use an interface, classes need to use the implements keyword. It forces us to override all methods of the class it implements. Note: In Dart, we can implement as many classes as needed
  ```
  void main() {
    Companies curent = Companies.AINSI;
  }
  enum Companies {
    AINSI,
    EDF,
    FGT,
  }
  ```
- ### Regular Expressions

  ```
  void main() {
    RegExp name = new RegExp(pattern);
    RegExp phone = new RegExp('^(?:[+0]9)?[0-9]{10}$');

    print(phone.hasMatch('0700342660')); // true
    print(phone.hasMatch('06543241')); // false
  ```

- ### Private

  Private Properties are those properties that are accessible only inside the file they are defined or the class they are declared. Dart provided privacy at the library level rather than class level due to which keywords like public, private, and protected are not used, unlike most languages. Identifiers starting with an underscore “\_” are visible inside the dart library. Thus, all the private properties inside dart are declared with an underscore at the start of their name.

  ```
  class Mobile {
    String? name;
    double? _price; // private

    Mobile(this.name, this.price); // public
    Mobile._(this.name, this.price); // private

    _printPrice() { // private
      print(this.price);
    }
    printName() {
      print(this.name);
    }
  }
  ```

- ### Mixin

  A mixin is a class with methods and properties utilized by other classes in Dart.

  It is a way to reuse code and write code clean.

  To declare a mixin, we use the mixin keyword:

  ```
  mixin Mixin_name{
  }
  ```

  Mixins, in other words, are regular classes from which we can grab methods (or variables) without having to extend them. To accomplish this, we use the with keyword.

  ```
  // Creating a Bark mixin
  mixin Bark {
    void bark() => print('Barking');
  }

  mixin Fly {
    void fly() => print('Flying');
  }

  mixin Crawl {
    void crawl() => print('Crawling');
  }
  // Creating an Animal class
  class Animal{
    void breathe(){
      print("Breathing");
    }
  }
  // Createing a Dog class, which extends the Animal class
  // Bark is the mixin with the method that Dog can implement
  class Dog extends Animal with Bark {}

  // Creating a Bat class Bat, which extends the Animal class
  // Fly is the mixin with the method that Bat can implement
  class Bat extends Animal with Fly {}

  class Snake extends Animal with Crawl{
    // Invoking the methods within the display
    void display(){
      print(".....Snake.....");
      breathe();
      crawl();
    }
  }

  main() {
    var dog = Dog();
    dog.breathe();
    dog.bark();

    var snake = Snake();
    snake.display();

  }
  ```
