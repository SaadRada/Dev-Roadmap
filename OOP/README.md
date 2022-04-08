# OOP - Object-Oriented Programming

The basic entities in object-oriented programming are classes and objects.

- All objects has a <strong>state</strong> and <strong>behavior</strong>
- state : variables like Boolean OnOff
- behavior : methods like turnOn() turnOff()

##  Classe
<strong>Classes</strong> are the building blocks of programs built using the object-oriented methodology. Such programs consist of independent self-managing modules and their interactions.

- class architecture :
  - fields : color
  - methods : drive()

![class architecture](https://bparanj.gitbooks.io/ruby-basics/content/part1/multiple-objects-share-single-method2.png)

- ### classe declaration
  ````
  class className {
    // fields
    String name;
    int age;

    // methods
    void  drink(){
      ...
    }
    void eat(){
      ...
    }
  }
  ````

- ### Access modifiers
  There are three types of access modifiers. Let’s take a look at them one by one.
  - ### Private
    A private member cannot be accessed directly from outside the class
    ````
    class personne {
      private String cardId;
    }
  - ### Public
    A public member can be directly accessed by anything which is in the same scope as the class object.
    ````
    class personne {
      public String name;
    }
    ````
    Public members of a class can be accessed by a class object using the . operator.
    ````
    personne ahmed = new personne();
    ahmedd.name = "ahmed";
    ````

