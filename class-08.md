# Interfaces pt 2

* An interface may define static methods, which must have an implementation. Beginning with C# 8.0, an interface may define a default implementation for members. By using interfaces, you can, for example, include behavior from multiple sources in a class.

* Interfaces can contain instance methods, properties, events, indexers, or any combination of those four member types. Interfaces may contain static constructors, fields, constants, or operators. An interface can't contain instance fields, instance constructors, or finalizers. Interface members are public by default.

* To implement an interface member, the corresponding member of the implementing class must be public, non-static, and have the same name and signature as the interface member. When a class or struct implements an interface, the class or struct must provide an implementation for all of the members that the interface declares but doesn't provide a default implementation for. However, if a base class implements an interface, any class that's derived from the base class inherits that implementation. The following example shows an implementation of the IEquatable interface.

* The derived interface inherits the members from its base interfaces. A class that implements a derived interface must implement all members in the derived interface, including all members of the derived interface's base interfaces. If the interface is inherited because you inherited a base class that implements the interface, the base class provides the implementation of the members of the interface. However, the derived class can reimplement any virtual interface members instead of using the inherited implementation.

* When interfaces declare a default implementation of a method, any class implementing that interface inherits that implementation. Implementations defined in interfaces are virtual and the implementing class may override that implementation. A base class can also implement interface members by using virtual members. In that case, a derived class can change the interface behavior by overriding the virtual members.

