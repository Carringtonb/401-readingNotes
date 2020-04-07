# Views and Azure Deployment

* Common HTML structures such as scripts and stylesheets are also frequently used by many pages within an app. All of these shared elements may be defined in a layout file, which can then be referenced by any view used within the app. Layouts reduce duplicate code in views.

* The layout defines a top level template for views in the app. Apps don't require a layout. Apps can define more than one layout, with different views specifying different layouts.

* The layout specified can use a full path (for example, /Pages/Shared/_Layout.cshtml or /Views/Shared/_Layout.cshtml) or a partial name (example: _Layout). When a partial name is provided, the Razor view engine searches for the layout file using its standard discovery process. The folder where the handler method (or controller) exists is searched first, followed by the Shared folder.

* A layout can optionally reference one or more sections, by calling `RenderSection`.

* The body and every section in a Razor page must be either rendered or ignored.
    * To ignore the body or sections you can call the `IgnoreBody` and `IgnoreSection` methods.

* Code that needs to run before each view or page should be placed in the _ViewStart.cshtml file.

# Tag Helpers

* Front-end designers conversant with HTML/CSS/JavaScript can edit Razor without learning C# Razor syntax. A rich IntelliSense environment for creating HTML and Razor markup This is in sharp contrast to HTML Helpers, the previous approach to server-side creation of markup in Razor views. Tag Helpers compared to HTML Helpers explains the differences in more detail. IntelliSense support for Tag Helpers explains the IntelliSense environment.

* Even developers experienced with Razor C# syntax are more productive using Tag Helpers than writing C# Razor markup. A way to make you more productive and able to produce more robust, reliable, and maintainable code using information only available on the server For example, historically the mantra on updating images was to change the name of the image when you change the image. The ImageTagHelper can append a version number to the image name, so whenever the image changes, the server automatically generates a new unique version for the image. Most built-in Tag Helpers target standard HTML elements and provide server-side attributes for the element.