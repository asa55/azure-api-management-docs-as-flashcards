##

API Management provides a rich, flexible set of features to support API authentication and authorization in addition to the standard control-plane authentication and role-based access control (RBAC) required when interacting with

%

Azure services

##

API Management also provides a fully customizable, standalone, managed developer portal, which can be used externally (or internally) to allow developer users to discover and interact with the APIs published through API Management. The developer portal has several options to facilitate secure user sign-up and

%

sign-in

##

Azure API Management "management plane", or

%

Azure control plane

##

API Management "data plane", or

%

API gateway

##

API Management "user plane", or

%

developer portal

##

Administrators, operators, developers, and DevOps service principals are examples of the different personas required to ``_____` an Azure API Management instance in a customer environment.

%

Administrators, operators, developers, and DevOps service principals are examples of the different personas required to **manage** an Azure API Management instance in a customer environment.

##

Azure API Management relies on Azure `_____` (Azure `_____`), which includes optional features such as multifactor authentication (MFA), and Azure RBAC to enable fine-grained access to the API Management service and its entities including APIs and policies.

%

Azure API Management relies on Azure **Active Directory** (Azure **AD**), which includes optional features such as multifactor authentication (MFA), and Azure RBAC to enable fine-grained access to the API Management service and its entities including APIs and policies.

##

The management plane can be accessed via:

- `_____`
- `_____`
- `_____`
- `_____`
- `_____`
- `_____`

%

- an Azure AD login (or token) through the Azure portal
- infrastructure-as-code templates (such as Azure Resource Manager or Bicep)
- the REST API
- client SDKs
- the Azure CLI
- or Azure PowerShell

##

API authentication and authorization in API Management involve the end-to-end communication of client apps to backend APIs through the API Management

%

gateway 

##

In many customer environments, `_____` is the preferred API authorization protocol. API Management supports `_____` across the data plane.

%

In many customer environments, **OAuth 2.0** is the preferred API authorization protocol. API Management supports **OAuth 2.0** across the data plane.

##

When a client app calls an API with a request that is secured using TLS and OAuth:

1. The client (the calling app, or `_____`) authenticates using credentials to an `_____`.
2. The client obtains a time-limited access token (a JSON web token, or JWT) from the identity provider's `_____`.
3. The identity provider (for example, Azure AD) is the issuer of the token, and the token includes an `_____` that authorizes access to a `_____` (for example, to a backend API, or to the API Management gateway itself).
4. The client calls the API and presents the access token - for example, in an Authorization header.
5. The `_____` validates the access token. Validation is a complex process that includes a check that the `_____` and `_____` claims contain expected values.
6. Based on token validation criteria, access to resources of the (backend) API is then granted.

%

1. The client (the calling app, or **bearer**) authenticates using credentials to an **identity provider**.
2. The client obtains a time-limited access token (a JSON web token, or JWT) from the identity provider's **authorization server**.
3. The identity provider (for example, Azure AD) is the issuer of the token, and the token includes an **audience claim** that authorizes access to a **resource server** (for example, to a backend API, or to the API Management gateway itself).
4. The client calls the API and presents the access token - for example, in an Authorization header.
5. The **resource server** validates the access token. Validation is a complex process that includes a check that the **issuer** and **audience** claims contain expected values.
6. Based on token validation criteria, access to resources of the (backend) API is then granted.

##

Depending on the type of client app and scenarios, different authentication flows are needed to request and manage tokens. For example, the authorization code flow and grant type are commonly used in apps that call

%

web APIs

##

The most common scenario is when the Azure API Management instance is a "transparent" proxy between the caller and backend API, and the calling application requests access to the API directly. The scope of the access token is between the calling application and backend API.

In this scenario, the access token sent along with the HTTP request is intended for the backend API, not API Management. However, API Management still allows for a defense in depth approach. For example, configure policies to validate the token, rejecting requests that arrive without a token, or a token that's not valid for the intended backend API. You can also configure API Management to check other claims of interest extracted from the token.

This describes the OAuth 2.0 scenario where audience is

%

the backend

##

In the OAuth 2.0 scenario where the audience is API Management, the API Management service acts on behalf of the API, and the calling application requests access to the API Management instance. The scope of the access token is between the calling application and API Management.

There are different reasons for wanting to do this. For example:

- `_____`
- `_____`

%

- The backend is a legacy API that can't be updated to support OAuth.
- The context required by the backend isn’t possible to establish from the caller.

##

API Management also supports acquisition and secure storage of OAuth 2.0 tokens for certain downstream services using the `_____` (preview) feature, including through use of custom policies and caching.

With `_____`, API Management manages the tokens for access to OAuth 2.0 backends, simplifying the development of client apps that access APIs.

%

API Management also supports acquisition and secure storage of OAuth 2.0 tokens for certain downstream services using the **authorizations** (preview) feature, including through use of custom policies and caching.

With **authorizations**, API Management manages the tokens for access to OAuth 2.0 backends, simplifying the development of client apps that access APIs.

##

Although authorization is preferred and OAuth 2.0 has become the dominant method of enabling strong authorization for APIs, API Management enables other authentication options that can be useful if the backend or calling applications are legacy or don't yet support OAuth. Options include:

- `_____` TLS (`_____`), also known as client certificate authentication, between the client (app) and API Management. This authentication can be end-to-end, with the call between API Management and the backend API secured in the same way.
- `_____` authentication, using the authentication-basic policy.
- `_____` key, also known as an API key. 

%

- **Mutual** TLS (**mTLS**), also known as client certificate authentication, between the client (app) and API Management. This authentication can be end-to-end, with the call between API Management and the backend API secured in the same way.
- **Basic** authentication, using the authentication-basic policy.
- **Subscription** key, also known as an API key. 

##

Microsoft recommends using a `_____` (API) key in addition to another method of authentication or authorization. On its own, a `_____` key isn't a strong form of authentication, but use of the `_____` key might be useful in certain scenarios, for example, tracking individual customers' API usage.

%

Microsoft recommends using a **subscription** (API) key in addition to another method of authentication or authorization. On its own, a **subscription** key isn't a strong form of authentication, but use of the **subscription** key might be useful in certain scenarios, for example, tracking individual customers' API usage.

##

The managed developer portal is an **optional** API Management feature that allows internal or external developers and other interested parties to discover and use APIs that are published through API Management.

%

The managed developer portal is an **optional** API Management feature that allows internal or external developers and other interested parties to discover and use APIs that are published through API Management.

##

If you elect to customize and publish the developer portal, API Management provides different options to secure it:

- `_____`
- `_____`
- `_____`

%

- External users
- Internal users
- Basic authentication

##

To secure developer portal: The preferred option when the developer portal is consumed externally is to enable business-to-consumer access control through Azure Active Directory `_____` (Azure AD `_____`).
  - Azure AD `_____` provides the option of using Azure AD `_____` native accounts: users sign up to Azure AD `_____` and use that identity to access the developer portal.
  - Azure AD `_____` is also useful if you want users to access the developer portal using existing social media or federated organizational accounts.
  - Azure AD `_____` provides many features to improve the end user sign-up and sign-in experience, including conditional access and MFA.

%

To secure developer portal: The preferred option when the developer portal is consumed externally is to enable business-to-consumer access control through Azure Active Directory **B2C** (Azure AD **B2C**).
  - Azure AD **B2C** provides the option of using Azure AD **B2C** native accounts: users sign up to Azure AD **B2C** and use that identity to access the developer portal.
  - Azure AD **B2C** is also useful if you want users to access the developer portal using existing social media or federated organizational accounts.
  - Azure AD **B2C** provides many features to improve the end user sign-up and sign-in experience, including conditional access and MFA.

##

To secure developer portal: The preferred option when the developer portal is consumed internally is to leverage your corporate Azure `_____`. Azure `_____` provides a seamless single sign-on (SSO) experience for corporate users who need to access and discover APIs through the developer portal.

%

To secure developer portal: The preferred option when the developer portal is consumed internally is to leverage your corporate Azure **AD**. Azure **AD** provides a seamless single sign-on (SSO) experience for corporate users who need to access and discover APIs through the developer portal.

##

To secure developer portal: A default option is to use the built-in developer portal `_____` and `_____` provider, which allows developer users to register directly in API Management and sign in using API Management user accounts. User sign up through this option is protected by a CAPTCHA service.

%

To secure developer portal: A default option is to use the built-in developer portal **username** and **password** provider, which allows developer users to register directly in API Management and sign in using API Management user accounts. User sign up through this option is protected by a CAPTCHA service.

##

In addition to providing configuration for developer users to sign up for access and sign in, the developer portal includes a test console where the developers can send test `_____`s through API Management to the backend APIs. This test facility also exists for contributing users of API Management who manage the service using the Azure portal.

%

In addition to providing configuration for developer users to sign up for access and sign in, the developer portal includes a test console where the developers can send test **request**s through API Management to the backend APIs. This test facility also exists for contributing users of API Management who manage the service using the Azure portal.

##

If the API exposed through Azure API Management is secured with OAuth 2.0 - that is, a calling application (_bearer_) needs to obtain and pass a valid access token - you can configure API Management to `_____` a valid token on behalf of an Azure portal or developer portal test console user.

%

If the API exposed through Azure API Management is secured with OAuth 2.0 - that is, a calling application (_bearer_) needs to obtain and pass a valid access token - you can configure API Management to **generate** a valid token on behalf of an Azure portal or developer portal test console user.

##

An API Management contributor and backend API developer wants to publish an API that is secured by OAuth 2.0. The API will be consumed by desktop applications whose users sign in using SSO through Azure AD. The desktop application developers also need to discover and test the APIs via the API Management developer portal.

Key configurations:

- Authorize developer users of the API Management developer portal using their corporate identities and Azure AD.	
- Set up the test console in the developer portal to obtain a valid OAuth 2.0 token for the desktop app developers to exercise the backend API.
  - The same configuration can be used for the test console in the Azure portal, which is accessible to the API Management contributors and backend developers.
  - The token could be used in combination with an API Management subscription key.
- Validate the OAuth 2.0 token and claims when an API is called through API Management with an access token.


Go a step further with this scenario by moving API Management into the network perimeter and controlling ingress through a 

%

reverse proxy

##

An API Management contributor and backend API developer wants to undertake a rapid proof-of-concept to expose a legacy API through Azure API Management. The API through API Management will be externally (internet) facing. The API uses client certificate authentication and will be consumed by a new public-facing single-page Application (SPA) being developed and delivered offshore by a partner. The SPA uses OAuth 2.0 with Open ID Connect (OIDC). Application developers will access the API in a test environment through the developer portal, using a test backend endpoint to accelerate frontend development.

Key configurations:

- Configure frontend developer access to the developer portal using the default username and password authentication.
  - Developers can also be invited to the developer portal.
- Validate the OAuth 2.0 token and claims when the SPA calls API Management with an access token. In this case, the audience is API Management.
- Set up API Management to use client certificate authentication to the backend.	

Go a step further with this scenario by using the developer portal with Azure AD authorization and Azure AD B2B collaboration to allow the delivery partners to collaborate more closely. Consider delegating access to API Management through RBAC in a development or test environment and enable SSO into the developer portal using their own corporate 

%

credentials

##

An API Management contributor and backend API developer is writing several new APIs that will be available to community developers. The APIs will be publicly available, with full functionality protected behind a paywall and secured using OAuth 2.0. After purchasing a license, the developer will be provided with their own client credentials and subscription key that is valid for production use. External community developers will discover the APIs using the developer portal. Developers will sign up and sign in to the developer portal using their social media accounts. Interested developer portal users with a test subscription key can explore the API functionality in a test context, without needing to purchase a license. The developer portal test console will represent the calling application and generate a default access token to the backend API.

Key configurations:

- Set up products in Azure API Management to represent the combinations of APIs that are exposed to community developers.
- Set up subscriptions to enable developers to consume the APIs.
- Configure community developer access to the developer portal using Azure AD B2C. Azure AD B2C can then be configured to work with one or more downstream social media identity providers.
- Set up the test console in the developer portal to obtain a valid OAuth 2.0 token to the backend API using the client credentials flow.

Go a step further by delegating user registration or product subscription and extend the process with your own

%

logic
