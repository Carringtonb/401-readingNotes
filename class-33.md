# OAUTH

* OAUTH allows user to sign into a web app using existing credentials from another app. Such as:
    * Google
    * Microsoft
    * Twitter
    * Facebook

* This is convenient for users and shifts many of the complexities of managing the sign-in process onto a third party.

* Social login providers assign Application Id and Application Secret tokens during the registration process. The exact token names vary by provider.

* These tokens represent the credentials your app uses to access their API. The tokens constitute the "secrets" that can be linked to your app configuration with the help of Secret Manager.

* When the app requires multiple providers, chain the provider extension methods behind `AddAuthentication`
