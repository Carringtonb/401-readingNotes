# Interfaces

* The class whose members are inherited is called the base class, and the class that inherits those members is called the derived class. If ClassC is derived from ClassB, and ClassB is derived from ClassA, ClassC inherits the members declared in ClassB and ClassA.

* Interface declarations may define a default implementation for its members. When you define a class to derive from another class, the derived class implicitly gains all the members of the base class, except for its constructors and finalizers. The following illustration shows a class WorkItem that represents an item of work in some business process. These members include a constructor, because constructors aren't inherited.

* Class ChangeRequest inherits from WorkItem and represents a particular kind of work item. ChangeRequest adds two more members to the members that it inherits from WorkItem and from Object. It must add its own constructor, and it also adds originalItemID. Property originalItemID enables the ChangeRequest instance to be associated with the original WorkItem to which the change request applies.

* If a derived class does not invoke a base- // class constructor explicitly, the default constructor is called // implicitly. «.

### Abstract and virtual methods

If a derived class is itself abstract, it inherits abstract members without implementing them. Abstract and virtual members are the basis for polymorphism, which is the second primary characteristic of object-oriented programming.

### Abstract base classes

An abstract class can contain one or more method signatures that themselves are declared as abstract. These signatures specify the parameters and return value but have no implementation . Derived classes that aren't abstract themselves must provide the implementation for any abstract methods from an abstract base class. For more information, see Abstract and Sealed Classes and Class Members.

### Interfaces

An interface is a reference type that defines a set of members. All classes and structs that implement that interface must implement that set of members. An interface may define a default implementation for any or all of these members.

### Derived class hiding of base class members

A derived class can hide base class members by declaring members with the same name and signature. The new modifier can be used to explicitly indicate that the member isn't intended to be an override of the base member.