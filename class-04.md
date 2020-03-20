## Classes

* When the object is created, enough memory is allocated on the managed heap for that specific object, and the variable holds only a reference to the location of said object.

### Declaring Classes

* The class keyword is preceded by the access level. Because public is used in this case, anyone can create instances of this class. The name of the class follows the class keyword.

### Creating objects

* An object is a concrete entity based on a class, and is sometimes referred to as an instance of a class.

* When an instance of a class is created, a reference to the object is passed back to the programmer. In the previous example, object1 is a reference to an object that is based on Customer. This reference refers to the new object but does not contain the object data itself.

* Because objects that are based on classes are referred to by reference, classes are known as reference types.

### Class inheritance

* When you create a class, you can inherit from any other interface or class that is not defined as sealed, and other classes can inherit from your class and override class virtual methods. Inheritance is accomplished by using a derivation, which means a class is declared by using a base class from which it inherits data and behavior. An abstract class contains abstract methods that have a signature definition but no implementation. They can only be used through derived classes that implement the abstract methods.

* By contrast, a sealed class does not allow other classes to derive from it. For more information, see Abstract and Sealed Classes and Class Members.