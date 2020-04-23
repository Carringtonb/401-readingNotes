# Policies

* An authorization policy consists of one or more requirements.

* The primary service that determines if authorization is successful is `IAuthorizationService`

* Policies are applied to controllers by using the `[Authorize]` attribute with the policy name.

* Policies are applied to Razor Pages by using the `[Authorize]` attribute with the policy name.

* An authorization requirement is a collection of data parameters that a policy can use to evaluate the current user principal.

* If an authorization policy contains multiple authorization requirements, all requirements must pass in order for the policy evaluation to succeed. 

### Authorization handlers

* An authorization handler is responsible for the evaluation of a requirement's properties. The authorization handler evaluates the requirements against a provided AuthorizationHandlerContext to determine if access is allowed.

* A requirement can have multiple handlers. A handler may inherit `AuthorizationHandler<RequirementToBeHandled>`.

* Authorization can't occur when the claim is missing, in which case a completed task is returned.

* Handlers are registered in the services collection during configuration.

* A handler indicates success by calling `context.Succeed(IAuthorizationRequirement requirement)`, passing the requirement that has been successfully validated.

* A handler doesn't need to handle failures generally, as other handlers for the same requirement may succeed.

* To guarantee failure, even if other requirement handlers succeed, call `context.Fail`.

* If a handler calls `context.Succeed` or `context.Fail`, all other handlers are still called. This allows requirements to produce side effects, such as logging, which takes place even if another handler has successfully validated or failed a requirement.

* In cases where you want evaluation to be on an OR basis, implement multiple handlers for a single requirement.

* There may be situations in which fulfilling a policy is simple to express in code. It's possible to supply a `Func<AuthorizationHandlerContext, bool>` when configuring your policy with the `RequireAssertion` policy builder.

* When using endpoint routing, authorization is typically handled by the Authorization Middleware.

