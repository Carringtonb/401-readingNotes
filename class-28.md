# Claims and Application Roles

* A claim is a name value pair that represents what a subjet can is, not what a subject can do.
    * Ex - Drivers License
        * Claim name - DatOfBirth
        * Claim Value - 4/20/2020

## Adding Claims Checks

* Claims based on authorization check the value of a claim and allows access to a resource based upon that value.

* An identity can contain multiple values and can contain multiple claims of the same type.

* Claim based authorization checks are declarative - the developer embeds them within their code, against a controller or an action within a controller, specifying claims which the current user must possess, and optionally the value the claim must hold to access the requested resource. Claims requirements are policy based, the developer must build and register a policy expressing the claims requirements.

* Most claims come with a value, and a list of accepted values can be specified when creating the policy.

### Multiple Policy Evaluation

* You can apply multiple policies to a controller or action, but then all policies must pass before access is granted.

* The more policies a controller or action has the more secure and exclusive it becomes. 