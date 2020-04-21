# Razor Pages

* Razor pages can handle requests directly without going through a controller.

* By convention, the PageModel class file has the same name as the Razor Page file with .cs appended.

* The page has an OnPostAsync handler method, which runs on POST requests (when a user posts the form). You can add handler methods for any HTTP verb. The most common handlers are:
    * OnGet
    * OnPost

* Razor Pages, by default, bind properties only with non-GET verbs. Binding to properties can reduce the amount of code you have to write. Binding reduces code by using the same property to render form fields `(<input asp-for="Customer.Name">)` and accept the input.

* Pages work with all the capabilities of the Razor view engine. Layouts, partials, templates, Tag Helpers, _ViewStart.cshtml, _ViewImports.cshtml work in the same way they do for conventional Razor views.

* A layout file should go in the *Pages/Shared* folder because razor views are meant to rely on folder hierarchy. not path conventions.

* Razor pages are more lightweight than MVC and are typically considered easier for begginers of people transitioning from other languages.

* Razor pages is also good for smaller applications where building a full MVC is overkill.