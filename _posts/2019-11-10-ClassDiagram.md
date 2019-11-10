---
layout: post
title:  "How to Read Class Diagram"
date:   2019-11-10
excerpt: ""
tag:
- iOS
- DesignPattern
comments: true
---

# Design Pattern OverView
* [What are Design Patterns?](https://changsic.github.io/DesignPattern/)
  * [A real-world example](#ex)
  * [Example explanation](#ex_detail)
  * [Types of design patterns](#type)
  * [Criticisms of design patterns](#criticisms)
  * [Benefits of design patterns](#benefits)
  * [Key Points](#key)
* How to Read a Class Diagram.

Class diagrams are like engineering blueprints; they provide information about a system through the medium of pictures, symbols and annotations.

Class diagrams은 공학의 청사진과 같은 것. 시스템 정보를 사진, 기호, 주석같은 도구를 통해 제공한다.


* Class is a box
![](/assets/dog_class.png)

* Inheritance is open arrowhead
![](/assets/arrow_inheritance.png)
  * ex : To show that SheepDog inherits from Dog, You would read this, from bottom to top, as  "SheepDig is a Dog"
  ![](/assets/inheritance_ex.png)

* Property is a plain arrowhead!
[](/assets/arrow_property.png)
  * ex : You should read a property arrow as “has a.” For example, if a Farmer has a Dog
  ![](/assets/property_ex.png)
  * You can indicate one-to-many relationships by specifying a range next to the arrowhead. For example, you can denote a Farmer has one or more Dogs like this
  ![](/assets/property_ex2.png)

* Protocol
![](/assets/petOwning_protocol.png)

* A class implements a protocol is an open arrowhead with a dashed line
![](/assets/arrow_protocol.png)
  * ex : You may either read this as “implements” or “conforms to.” For example, you’d indicate Farmer conforms to PetOwning
  ![](/assets/protocol_ex.png)

* A plain arrowhead with a dashed line is "uses", which is called a “dependency” in UML terms
![](/assets/arrow_use.png)
  * whenever you use a dependency arrow, you usually should annotate its purpose. For example, you can use a dependency arrow to indicate the following things:
    * A weak property or delegate.
    * An object that’s passed into a method as a parameter, but not held as a property.
    * A loose coupling or callback, such as an IBAction from a view to a controller.
    ![](/assets/use_ex.png)

* You can also denote properties and methods in a class diagram
![](/assets/protocol_ex2.png)


## Key points
Here are the key points you learned:
* Class diagrams give a visual representation of class and protocol types, showing their properties and methods.
* Class diagrams also show the relationship between the object types.
* Class diagrams can be drawn in any other orientation; the direction of the arrows define the meaning.
* Boxes denote classes, and lines denote relationships: “implements,” “has a,” “uses“ and “conforms to” are the most common relations.
* Boxes can also denote protocols, which is indicated by <<protocol>> before the name.
