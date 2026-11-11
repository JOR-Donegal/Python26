# 8. Getting started

These notes are provided to demonstrate how to get started with _Object Oriented_ (OO) coding in Python. So far, we have concentrated on functional programming. The fundamental units of coding are functions, and we create a main program to call these functions in the correct sequence. In scripting, this is a perfect paradigm for most of the code we are going to write.

But there is an entirely different paradigm which organizes our code around self-contained objects, which encapsulate data, properties (attributes), and functions (methods). Where we create large projects, which are complex, and will be maintained by many people, this is a more scalable way to organize.

On a large project, I can have groups working separately on different objects, giving me better scalability and code reuse. In this approach, a class is a template used to create objects. We instantiate the class to create instances of an individual object. Everything related to this class is contained inside an object, and only selected attributes and methods are exposed to the outside.

Some of my projects look at _digital twins_, a very poorly defined term. However, in every case, I use OO techniques for these projects.

In electronics terms, an object is a _black box_. It provides an abstraction to the complexity which it contains.

Imagine I am writing an instrument system for an airplane, and I create an instrument class. Instruments have certain characteristics or properties (Name, Type, etc) that all instruments have. If I want to verify communications, I could have a method to check a _cyclical redundancy check_ (CRC). By making the barometer class a sub-class of the instrument class, the barometer class can inherit all the properties and methods of the instrument class.

My airspeed class could also inherit the properties and methods of all instruments and have additional properties and methods specific to the pitot sensor. Methods can be extended and overridden; this is _polymorphism_.

Objects can share behaviors and functions can have different meanings and usages depending on the context.

In our coding so far, you have extensively used this functionality! Every time you use the format object.method you are using this.

For example

```python
my_string = "jor" 
my_proper_string = my_string.capitalize() 
print(my_proper_string)
```

Appending, sorting are all examples of methods which change the contents of an object.

For this group of exercises, create a folder called _/Python/Exercises08_

Keep your scripts in _/Python/Exercises08/Code_ with an appropriate name.

Keep a screenshot of any tests you do in _/Python/Exercises08/Tests_ with an appropriate name.
