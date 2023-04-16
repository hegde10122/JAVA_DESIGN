
### What is UML ?

The Unified Modeling Language (UML) is one of the most useful tools in the
world of system development. It is a visual modeling language that allows
system builders to create blueprints that capture their visions in a standard, easy-to-understand manner, 
and provides a mechanism to effectively share and communicate these  visions with others.

The UML consists of a number of graphical elements that combine to form diagrams. Because
the UML is a language, it has rules for combining these elements. 

### Class Diagram

We have many things around us in our daily surroundings. These things have properties (attributes) and behave in certain 
ways. These behaviours are a set of operations. These things fall into a set of categories like buildings, shops, 
vehicles,gadgets etc. A class is a category or group of things that have the same attributes and the same behaviours. 

Anything in the class of microwave ovens has attributes such as brand name, model, serial number, and
capacity. Behaviours for things in this class include the operations "accept food,"turn on", and "turn off".

UML class icon
---------------
An example of the UML notation that captures these attributes and behaviours of a microwave oven. 
A rectangle is the icon that represents the class. It's divided into three areas. 
The uppermost area contains the name, the middle area holds the attributes, and the lowest area holds the operations.

Similarly,  we consider class of Washing machines. Both the class diagrams are depicted in the figure below.

Observe the spacing in the names of the class, the attributes, and the operations. In UML, a
multi-word classname has initial capital letters for all the words and eliminates whitespace
between each word (for example, WashingMachine or MicrowaveOven). Attribute-names and operation-names
follow the same convention, but the first letter of the first word isn't capitalized (for example,
acceptFood()).

<h3><img align="center" height="300" width="300" src="https://github.com/hegde10122/JAVA_KOTLIN_DESIGN/blob/master/uml/01_UML_Class.svg">  UML class diagram</h3>

A class diagram consists of a number of these rectangle icons connected by lines that show how the classes relate to one another.

Object Diagram
---------------

An object is an instance of a class - a definite thing with certain values of the class' attributes. For example, the microwave might have the brand name 
Samsung, the model name Countertop, serial number G134250, capacity of 23L.

See the figure below for an idea about object diagram.

<h3><img align="center" height="300" width="300" src="https://github.com/hegde10122/JAVA_KOTLIN_DESIGN/blob/master/uml/objects.png">  UML object diagram</h3>

Use Case Diagram
----------------

A use case is a description of a system's behaviour from a user's standpoint. It is an old way of collecting system requirements from a user's point of view. 

Use case diagram example can be found in the below diagram. 

<h3><img align="center" height="300" width="300" src="https://github.com/hegde10122/JAVA_KOTLIN_DESIGN/blob/master/uml/uml_usecase.png">UML use-case diagram</h3>

The small stick figure that corresponds to the microwave oven user is called an actor. The ellipse represents the use case. 
Note that the actor — the entity that initiates the use  case — can be a person or another system. Note also that the use case is inside a rectangle
that represents the system, and the actor is outside the rectangle.


State Diagram
-------------

At any given time, an object is in a particular state. A person can be a  child or an adult. A car is either moving or stationary. A washing machine
can be either in the soaking, washing, rinsing, spinning, or off state.

An example of state diagram can be found below.

<h3><img align="center" height="300" width="300" src="https://github.com/hegde10122/JAVA_KOTLIN_DESIGN/blob/master/uml/uml_statediagram.png">UML state diagram</h3>

The symbol at the top of the  above figure represents the start state and the symbol at the bottom
represents the end state.

Sequence Diagram
-----------------

Class diagrams and object diagrams represent static information. 
In a functioning system, however, objects interact with one another, and these interactions occur over time. 
The UML sequence diagram shows the time-based dynamics of the interaction.
Using the washing machine example, the components of the  washing machine include a timer, a water pipe (for fresh water input), 
and a drum (the part that holds the clothes,soap and the water). These, of course, are also objects.

If the user invokes the "Wash clothes" use case, assuming the user has completed the
"add clothes," "add detergent," and "turn on" operations, the sequence of steps goes something like this:

1. At the beginning of "soaking," water enters the drum via the water pipe.
2. The drum remains stationary for 7 minutes.
3. At the end of "Soaking," water stops entering the drum.
4. At the beginning of "Washing," the drum rotates back and forth and continues doing this
   for 15 minutes.
5. At the end of "Washing," the drum pumps out the soapy water.
6. The drum stops rotating.
7. At the beginning of "Rinsing," water entry restarts.
8. The drum rotates back and forth.
9. After 15 minutes water entry stops.
10. At the end of "Rinsing," the drum pumps out the rinse water.
11. The drum stops rotating.
12. At the beginning of "Spinning," the drum rotates clockwise and continues for 5 minutes.
13. At the end of "Spinning," the drum rotation stops.
14. The wash is done.

Imagine that the timer, the water pipe, and the drum are objects. Assume that each object
has one or more operations. The objects work together by sending messages to each other.

Each message is a request from the sender-object to the receiver-object. The request asks
the receiver to complete one of its (the receiver's) operations.
Let's get specific about the operations. 

The timer can
a) Time the soaking
b) Time the washing
c) Time the rinsing
d) Time the spinning

The water pipe can
a) Start a flow
b) Stop a flow

The drum can
a) Store water
b) Rotate back and forth
c) Rotate clockwise
d) Stop rotating
e) Pump water


<h3><img align="center" height="300" width="300" src="https://github.com/hegde10122/JAVA_KOTLIN_DESIGN/blob/master/uml/sequence_diagram.png">UML sequence diagram</h3>

The above figure  shows how to use these operations to create a sequence diagram that captures the
messages among the timer, water pipe, drum, and drain represented as anonymous objects
at the top of the diagram. 
Each arrow represents a message that goes from one object to another. Time, in this diagram, proceeds from top to bottom.
So the first message is timeSoak(), which the timer sends to itself. The second message is sendWater(), which the
timer sends to the water pipe. The final message, stopRotating(), goes from the timer to the drum.

UML Activity Diagram
---------------------

The activity diagram for steps 4 to 6 for the washing machine ia as below

<h3><img align="center" height="300" width="300" src="https://github.com/hegde10122/JAVA_KOTLIN_DESIGN/blob/master/uml/activity_diagram.png">UML activity diagram</h3>
