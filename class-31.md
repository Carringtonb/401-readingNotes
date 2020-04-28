# View Components

* View components are similar to partial views, but they're much more powerful.

* View components don't use model binding, and only depend on the data provided when calling into it. 

* View Components:
    * Render a chunk instead of a whole response
    * Include seperation of concerns
    * Can have parameters and business logic
    * Typically invoked from layout page

* View components are intended anywhere you have reusable rendering logic thats too complex for a partial view.

* A view component consists of the class(ViewComponent), and the result it returns(view).

* Like controllers, view components must be public, non-nested, and non-abstract classes. 

* A complex view component might need to specify a non-default view under some conditions.
