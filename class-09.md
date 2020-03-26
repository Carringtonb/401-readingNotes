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