# Intro to Identity

* ASP.NET Core Identity is a membership system that adds login functionality to ASP.NET Core apps. Users can create an account with the login information stored in Identity or they can use an external login provider.

* When a user clicks the Register link, the `RegisterModel.OnPostAsync` action is invoked.

* If the user was created successfully, the user is logged in by the call to `_signInManager.SignInAsync.`

* The Log out link invokes the `LogoutModel.OnPost` action.

* The default web project templates allow anonymous access to the home pages. To test Identity, add `[Authorize]` to the Privacy page.