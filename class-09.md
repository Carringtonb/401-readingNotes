## LINQ

* With LINQ, a query is a first-class language construct, just like classes, methods, events. You write queries against strongly typed collections of objects by using language keywords and familiar operators. The LINQ family of technologies provides a consistent query experience for objects , relational databases , and XML . For a developer who writes queries, the most visible «language-integrated» part of LINQ is the query expression.

* By using query syntax, you can perform filtering, ordering, and grouping operations on data sources with a minimum of code. You use the same basic query expression patterns to query and transform data in SQL databases, ADO . You can write LINQ queries in C# for SQL Server databases, XML documents, ADO. The complete operation includes creating a data source, defining the query expression, and executing the query in a foreach statement.

* All LINQ query operations consist of three distinct actions
    * Query execution. The following illustration shows the complete query operation. In LINQ, the execution of the query is distinct from the query itself. In other words, you have not retrieved any data just by creating a query variable.


   *  In the previous example, because the data source is an array, it implicitly supports the generic IEnumerable interface. This fact means it can be queried with LINQ. A queryable type requires no modification or special treatment to serve as a LINQ data source. If the source data is not already in memory as a queryable type, the LINQ provider must represent it as such.

    * With LINQ to SQL, you first create an object-relational mapping at design time either manually or by using the LINQ to SQL Tools in Visual Studio in Visual Studio. You write your queries against the objects, and at run-time LINQ to SQL handles the communication with the database.

* Deferred Execution

    * As stated previously, the query variable itself only stores the query commands. The actual execution of the query is deferred until you iterate over the query variable in a foreach statement. Because the query variable itself never holds the query results, you can execute it as often as you like. In your application, you could create one query that retrieves the latest data, and you could execute it repeatedly at some interval to retrieve different results every time.

* Forcing Immediate Execution

    * These execute without an explicit foreach statement because the query itself must use foreach in order to return a result. Note also that these types of queries return a single value, not an IEnumerable collection.

    ## Collections

*  A collection is a class, so you must declare an instance of the class before you can add elements to that collection. If your collection contains elements of only one data type, you can use one of the classes in the System. Collections. Generic namespace.

* A generic collection enforces type safety so that no other data type can be added to it. When you retrieve an element from a generic collection, you do not have to determine its data type or convert it.

* Whenever possible, you should use the generic collections in the System. Collections namespace.

* The System. Specialized namespace provides specialized and strongly typed collection classes, such as string-only collections and linked-list and hybrid dictionaries.

* The Dictionary generic collection enables you to access to elements in a collection by using the key of each element. The following example creates a Dictionary collection and iterates through the dictionary by using a foreach statement.

* An iterator is used to perform a custom iteration over a collection. An iterator can be a method or a get accessor. An iterator uses a yield return statement to return each element of the collection one at a time.

* You call an iterator by using a foreach statement. Each iteration of the foreach loop calls the iterator. When a yield return statement is reached in the iterator, an expression is returned, and the current location in code is retained. Execution is restarted from that location the next time that the iterator is called.

## ENUMS 

* You can explicitly specify any other integral numeric type as an underlying type of an enumeration type.

* The default value of an enumeration type E is the value produced by expression 0, even if zero doesn't have the corresponding enum member.

*Enumeration types as bit flags*

* If you want an enumeration type to represent a combination of choices, define enum members for those choices such that an individual choice is a bit field. That is, the associated values of those enum members should be the powers of two.

`Days meetingDays = Days. Monday | Days. Wednesday | Days. Thursday | Days.`

* Enum API reference page. Enum type is the abstract base class of all enumeration types. It provides a number of methods to get information about an enumeration type and its values. Enum in a base class constraint to specify that a type parameter is an enumeration type.

* If you cast an enum value to its underlying type, the result is the associated integral value of an enum member.