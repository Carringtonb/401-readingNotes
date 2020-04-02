# Entity Framkework Pt.2

* Data seeding is the process of populating a database with an initial set of data, there are several ways this can be accomplished.
    * Model Seed Data
        * New if EF Core 2.1
        * The primary key value needs to be specified even if it's usually generated by the database. It will be used to detect data changes between migrations.Previously seeded data will be removed if the primary key is changed in any way.
    * Manual Migration Customization
        * Manually adding calls for `InsertData()`, `UpdateData()`, and `DeleteData()`
    * Custom initialization logic
        * Running the initialization app locally
        *Deploying the initialization app with the main app, invoking the initialization routine and disabling or removing the initialization app.

## Tag Helpers

* Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files.
* For the most part, tag helpers look like standard *HTML*
* Most built-in Tag Helpers target standard HTML elements and provide server-side attributes for the element.