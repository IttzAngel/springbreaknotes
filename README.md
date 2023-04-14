- CHAPTER 7-----
- if multiple classes can fit into the same category with an is-A relationship and have same methods you can create a parent class in which the other classes can inherit methods using the extends keyword
- subclass extends superclass
- inheritance can help to avoid duplicating code, use it for common methods
- override methods in individual subclasses for each subclass to have its own behavior (for example every animal has a makeNoise() method that exists in the parent class, but every animal makes a different noise)
- hierarchy is extremely important (for example dog and wolf is-A canine, canine is-A animal, therefore dog and wolf classes will extend canine class, and canine class will extend animal class)
- is-A relationship works in one direction, circle is-A shape, but shape is-A circle does not make any sense
- four access levels: private default protected public
- public members are inherited, private members are not inherited
- inheritance makes our life easier using common methods instead of having to constantly duplicate our code into every single class
- three steps of object declaration and assignment = 1. declare a reference variable 2. create an object 3. link the object and the reference. example: Dog myDog = new Dog();
- HOWEVER, with polymorphism, the reference and the object can be different. example: Animal myDog = new Dog();
- when overriding, arguments must be the same and return types must be compatible and the method cant be less accessible
- when overloading a method, the return types can be different, you cant change ONLY the return type, and you can vary the access levels in any direction

- CHAPTER 8-----
- if you mark a class as abstract, the compiler will stop any code anywhere from creating an instance of that type
- an abstract class means that nobody can ever make a new instance of the class
- if a class is not abstract, it is automatically concrete
- use abstract if there can be different types of this class/thing, and concrete if it should not change (example: cat is concrete, feline is abstract)
- abstract methods have no body
- you must implement all abstract methods
- you cannot have an abstract method in a non abstract class, but you can have both abstract and non abstract methods in an abstract class
- every class extends class Object
- polymorphism means "many forms"
- you can only call a method on an object if the class of the reference variable has the method
- avoid the deadly diamond of death, aka multiple inheritance (even though java does not allow this to happen)
- classes from different inheritacne tress can implement the same interface, for example, dog and cat are different trees, however they can both implement a pet interface
- make a class that doesnt extend anything if it does not pass the is-A test, make a subclass when you want to make a more specific version and need to override or add behaviors, make an abstract class when you want to define a template for a group of subclasses, and when you want to guarantee that nobody can make objects of that type, and an interface when you want to define a role that other classes can play, no matter which inheritance tree the class is in

- CHAPTER 9-----
- you can choose when and how to construct an object, and you can choose when to destroy it
- instance variables are declared inside a class but not inside a method, STAY OUT ALL METHODS INCLUDING MAIN
- local variables are declared inside a method, including method parameters
- the method on top of the stack is always the currently executing method, aka your code executes from top to bottom
- non primitive variable holds a reference to an object
- if the local variable is a reference to an object, only the variable goes on the stack
- it looks like a method at the end of the object creation, but we need to use the constructor
- before an object can be used, it needs to be constructed
- add a parameter to the constructor and an argument value and you can create the object with a property to it in one statement, and you can pass a value to the constructor (book example is duck and ducksize)
- if you want a no-arg constructor, you have to build it yourself, it is not automatic
- overloaded constructors mean you have more than one constructor in your class
- every contsuctor in an inheritance tree must run when you make a new object
- the only way to call a super constructor is by using super();
- the super class must be fully formed before the subclass can be constructed. a child cannot exist before the parents
- the call to super() must be the first statement in each constructor
- an objects life depends on the reference variables life
- a local variable only lives within the method that declared the variable
- an instance variable lives as long as the object does. if the object is still alive, so are the instance variables

- CHAPTER 10-----
- MATH methods are as close as youll get to any type of global method in java
- the keyword static lets a method run without any instance of the class
- static methods can not use non static (instance) variables
- static methods can not use non static methods
- a static variable means the value is the same for all instances of the class
- static variables are shared
- all instances of the same class share a single copy of the static variables
- static final variables are constants
- final can also be used for non static variables
- final simply means that the value can not be changed
- autoboxing does the conversion from primitive to wrapper object automatically
