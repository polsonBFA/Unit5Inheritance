[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=23658678)
# Instructions

Design and implement a hierarchy of classes, such that the code fragment in another class
```java
  ArrayList<Money> piggyBank = new ArrayList<Money>();
  piggyBank.add(new Quarter());
  piggyBank.add(new Bill(1));
  piggyBank.add(new Nickel());
  piggyBank.add(new Nickel());
  piggyBank.add(new Dime());
  piggyBank.add(new Coin("half-dollar", 0.50));
  piggyBank.add(new Bill(5));
  System.out.println(piggyBank);
  double amount = 0;
  for (Money item : piggyBank)
    {
      amount += item.getValue();
    }
  System.out.println("The piggy bank holds $" + amount + ".");
  
```

displays
```java
[quarter, $1, nickel, nickel, dime, half-dollar, $5]
The piggy bank holds $6.95.
```
# Design Requirements
__All Money objects have the following attributes.__
* A double variable indicating the value of a particular type of money.
* The Money class contains a getValue method that returns the value of a Money object.

__The Coin class is a subclass of Money.__
* The Coin class contains an additional attribute not found in Money: A String variable indicating the name of a coin.
* The constructor for the Coin class accepts two parameters for the name of the coin and the value of the coin.* The value is passed to the Money class.

__The Quarter, Nickel, and Dime classes are all subclasses of Coin__  
* These classes do not contain any attributes or methods other than those found in the Coin or Money classes. 
* The constructor for these classes accepts no parameters, yet passes a literal string with coin name and the appropriate value to the Coin class to construct the object.

__The Coin and Bill classes should each have an appropriate toString method__


__Write your classes to avoid duplication of code by using inheritance
properly.__


US coin names and values are as indicated.
* Quarter = $0.25
* Dime = $0.10
* Nickel = $0.05

  
