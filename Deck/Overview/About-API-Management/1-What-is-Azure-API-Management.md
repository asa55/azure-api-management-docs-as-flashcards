##

Azure API Management is a hybrid, multicloud management platform for APIs across all 

%

environments

##

As a `_____`-as-a-service, API Management supports the complete API lifecycle.

%

As a **platform**-as-a-service, API Management supports the complete API lifecycle.

##

APIs enable digital experiences, simplify application integration, underpin new digital products, and make data and services reusable and universally

%

accessible

##

With the proliferation and increasing dependency on APIs, organizations need to manage them as first-class assets throughout their

%

lifecycle

##

Azure API Management helps customers meet these challenges:

- `_____` backend architecture diversity and complexity from API consumers
- Securely `_____` services hosted on and outside of Azure as APIs
- `_____`, accelerate, and observe APIs
- Enable API `_____` and consumption by internal and external users

%

- **Abstract** backend architecture diversity and complexity from API consumers
- Securely **expose** services hosted on and outside of Azure as APIs
- **Protect**, accelerate, and observe APIs
- Enable API **discovery** and consumption by internal and external users

##


Common API Management scenarios include:

- Unlocking `_____` assets
- `_____`-centric app integration
- Multi-`_____` user experiences
- B2B `_____`

%

- Unlocking **legacy** assets
- **API**-centric app integration
- Multi-**channel** user experiences
- B2B **integration**

##

APIs are used to abstract and modernize legacy backends and make them accessible from new cloud services and modern applications. APIs allow innovation without the risk, cost, and delays of

%

migration

##

`_____` are easily consumable, standards-based, and self-describing mechanisms for exposing and accessing data, applications, and processes. They simplify and reduce the cost of app integration.

%

**APIs** are easily consumable, standards-based, and self-describing mechanisms for exposing and accessing data, applications, and processes. They simplify and reduce the cost of app integration.

##

APIs are frequently used to enable user experiences such as web, mobile, wearable, or Internet of Things applications. Reuse APIs to accelerate development and

%

Return on Investment (ROI)

##

APIs exposed to partners and customers lower the barrier to integrate business processes and exchange `_____` between business entities.

%

APIs exposed to partners and customers lower the barrier to integrate business processes and exchange **data** between business entities.

##

APIs eliminate the overhead inherent in `_____` integration. Especially with self-service discovery and onboarding enabled, APIs are the primary tools for scaling B2B integration.

%

APIs eliminate the overhead inherent in **point-to-point** integration. Especially with self-service discovery and onboarding enabled, APIs are the primary tools for scaling B2B integration.

##

API Management is available in various `_____` differing in capacity and features

%

API Management is available in various **tiers** differing in capacity and features

##

Azure API Management is made up of the following components. These are Azure-hosted and fully managed by default

- `_____`
- `_____`
- `_____`

%

- an API gateway
- a management plane
- and a developer portal

##

All requests from client applications first reach the API

%

gateway

##

The API gateway forwards requests from client applications to respective `_____` services.

%

The API gateway forwards requests from client applications to respective **backend** services.

##

The API gateway acts as a facade to the `_____` services, allowing API providers to abstract API implementations and evolve `_____` architecture without impacting API consumers.

%

The API gateway acts as a facade to the **backend** services, allowing API providers to abstract API implementations and evolve **backend** architecture without impacting API consumers.

##

The API `_____` enables consistent configuration of routing, security, throttling, caching, and observability.

%

The API **gateway** enables consistent configuration of routing, security, throttling, caching, and observability.

##

The API gateway:

- Acts as a `_____` to backend services by accepting API calls and routing them to appropriate backends
- `_____` API keys and other credentials such as JWT tokens and certificates presented with requests
- `_____` usage quotas and rate limits
- Optionally `_____` requests and responses as specified in policy statements
- If configured, `_____` responses to improve response latency and minimize the load on backend services
- `_____` logs, metrics, and traces for monitoring, reporting, and troubleshooting

%

- Acts as a **facade** to backend services by accepting API calls and routing them to appropriate backends
- **Verifies** API keys and other credentials such as JWT tokens and certificates presented with requests
- **Enforces** usage quotas and rate limits
- Optionally **transforms** requests and responses as specified in policy statements
- If configured, **caches** responses to improve response latency and minimize the load on backend services
- **Emits** logs, metrics, and traces for monitoring, reporting, and troubleshooting

##

With the `_____` gateway, customers can deploy the API gateway to the same environments where they host their APIs, to optimize API traffic and ensure compliance with local regulations and guidelines. The `_____` gateway enables customers with hybrid IT infrastructure to manage APIs hosted on-premises and across clouds from a single API Management service in Azure.

The `_____` gateway is packaged as a Linux-based Docker container and is commonly deployed to Kubernetes, including to Azure Kubernetes Service and Azure Arc-enabled Kubernetes.

%

With the **self-hosted** gateway, customers can deploy the API gateway to the same environments where they host their APIs, to optimize API traffic and ensure compliance with local regulations and guidelines. The **self-hosted** gateway enables customers with hybrid IT infrastructure to manage APIs hosted on-premises and across clouds from a single API Management service in Azure.

The **self-hosted** gateway is packaged as a Linux-based Docker container and is commonly deployed to Kubernetes, including to Azure Kubernetes Service and Azure Arc-enabled Kubernetes.

##

API providers interact with the service through the `_____` plane, which provides full access to the API Management service capabilities.

%

API providers interact with the service through the **management** plane, which provides full access to the API Management service capabilities.

##

Customers interact with the `_____` plane through Azure tools including the Azure portal, Azure PowerShell, Azure CLI, a Visual Studio Code extension, or client SDKs in several popular programming languages.

%

Customers interact with the **management** plane through Azure tools including the Azure portal, Azure PowerShell, Azure CLI, a Visual Studio Code extension, or client SDKs in several popular programming languages.

##

Use the management plane to:

- Provision and configure API Management service `_____`
- Define or import API `_____` from a wide range of sources, including OpenAPI specifications, Azure compute services, or WebSocket or GraphQL backends
- `_____` APIs into products
- Set up `_____` like quotas or transformations on the APIs
- Get `_____` from analytics
- `_____` users

%

- Provision and configure API Management service **settings**
- Define or import API **schemas** from a wide range of sources, including OpenAPI specifications, Azure compute services, or WebSocket or GraphQL backends
- **Package** APIs into products
- Set up **policies** like quotas or transformations on the APIs
- Get **insights** from analytics
- **Manage** users

##

The open-source `_____` portal is an automatically generated, fully customizable website with the documentation of your APIs.

%

The open-source **developer** portal is an automatically generated, fully customizable website with the documentation of your APIs.

##

API providers can customize the look and feel of the developer portal by adding custom content, customizing styles, and adding their branding. Extend the developer portal further by

%

self-hosting

##

App developers use the open-source `_____` portal to discover the APIs, onboard to use them, and learn how to consume them in applications. (APIs can also be exported to the Power Platform for discovery and use by citizen developers.)

%

App developers use the open-source **developer** portal to discover the APIs, onboard to use them, and learn how to consume them in applications. (APIs can also be exported to the Power Platform for discovery and use by citizen developers.)

##

Using the developer portal, developers can:

- Read API `_____`
- Call an API via the `_____` console
- Create an `_____` and subscribe to get API keys
- Access `_____` on their own usage
- Download API `_____`
- Manage API `_____`

%

- Read API **documentation**
- Call an API via the **interactive** console
- Create an **account** and subscribe to get API keys
- Access **analytics** on their own usage
- Download API **definitions**
- Manage API **keys**

##

API Management integrates with many complementary Azure services to create enterprise solutions, including:

- Azure `_____` for secure safekeeping and management of client certificates and secrets
- Azure `_____` for logging, reporting, and alerting on management operations, systems events, and API requests
- `_____` for live metrics, end-to-end tracing, and troubleshooting
- `_____`, private endpoints, and Application Gateway for network-level protection
- Azure `_____` for developer authentication and request authorization
- `_____` for streaming events
- Several Azure `_____` offerings commonly used to build and host APIs on Azure, including Functions, Logic Apps, Web Apps, Service Fabric, and others.

%

- Azure **Key Vault** for secure safekeeping and management of client certificates and secrets
- Azure **Monitor** for logging, reporting, and alerting on management operations, systems events, and API requests
- **Application Insights** for live metrics, end-to-end tracing, and troubleshooting
- **Virtual networks**, private endpoints, and Application Gateway for network-level protection
- Azure **Active Directory** for developer authentication and request authorization
- **Event Hubs** for streaming events
- Several Azure **compute** offerings commonly used to build and host APIs on Azure, including Functions, Logic Apps, Web Apps, Service Fabric, and others.

##

`_____` are the foundation of an API Management service instance. Each `_____` represents a set of operations available to app developers. Each `_____` contains a reference to the backend service that implements the `_____`, and its operations map to backend operations.

%

**APIs** are the foundation of an API Management service instance. Each **API** represents a set of operations available to app developers. Each **API** contains a reference to the backend service that implements the **API**, and its operations map to backend operations.

##

Operations in API Management are highly `_____`, with control over URL mapping, query and path parameters, request and response content, and operation response caching.

%

Operations in API Management are highly **configurable**, with control over URL mapping, query and path parameters, request and response content, and operation response caching.

##

`_____` are how APIs are surfaced to developers. `_____` in API Management have one or more APIs, and can be open or protected. Protected `_____` require a subscription key, while open `_____` can be consumed freely.

%

**Products** are how APIs are surfaced to developers. **Products** in API Management have one or more APIs, and can be open or protected. Protected **products** require a subscription key, while open **products** can be consumed freely.

##

When a product is ready for use by developers, it can be `_____`. Once `_____`, it can be viewed or subscribed to by developers. Subscription approval is configured at the product level and can either require an administrator's approval or be automatic.

%

When a product is ready for use by developers, it can be **published**. Once **published**, it can be viewed or subscribed to by developers. Subscription approval is configured at the product level and can either require an administrator's approval or be automatic.

##

`_____` are used to manage the visibility of products to developers.

%

**Groups** are used to manage the visibility of products to developers.

##

API Management has the following built-in groups:

- `_____`
- `_____`
- `_____`

%

- Administrators
- Developers
- Guests

##

API Management Group "`_____`": Manage API Management service instances and create the APIs, operations, and products that are used by developers.
Azure subscription administrators are members of this group.

%

API Management Group "**Administrators**": Manage API Management service instances and create the APIs, operations, and products that are used by developers.
Azure subscription administrators are members of this group.

##

API Management Group "`_____`": Authenticated developer portal users that build applications using your APIs. Developers are granted access to the developer portal and build applications that call the operations of an API.

%

API Management Group "**Developers**": Authenticated developer portal users that build applications using your APIs. Developers are granted access to the developer portal and build applications that call the operations of an API.

##

API Management Group "`_____`": Unauthenticated developer portal users, such as prospective customers visiting the developer portal. They can be granted certain read-only access, such as the ability to view APIs but not call them.

%

API Management Group "**Guests**": Unauthenticated developer portal users, such as prospective customers visiting the developer portal. They can be granted certain read-only access, such as the ability to view APIs but not call them.

##

API Management Group "`_____`" can also create custom groups or use external groups in an associated Azure Active Directory tenant to give developers visibility and access to API products. For example, create a custom group for developers in a partner organization to access a specific subset of APIs in a product. A user can belong to more than one group.

%

API Management Group "**Administrators**" can also create custom groups or use external groups in an associated Azure Active Directory tenant to give developers visibility and access to API products. For example, create a custom group for developers in a partner organization to access a specific subset of APIs in a product. A user can belong to more than one group.

##

`_____` represent the user accounts in an API Management service instance. `_____` can be created or invited to join by administrators, or they can sign up from the `_____` portal. Each `_____` is a member of one or more groups, and can subscribe to the products that grant visibility to those groups.

When `_____` subscribe to a product, they're granted the primary and secondary key for the product for use when calling the product's APIs.

%

**Developers** represent the user accounts in an API Management service instance. **Developers** can be created or invited to join by administrators, or they can sign up from the **developer** portal. Each **developer** is a member of one or more groups, and can subscribe to the products that grant visibility to those groups.

When **developers** subscribe to a product, they're granted the primary and secondary key for the product for use when calling the product's APIs.

##

With `_____`, an API publisher can change the behavior of an API through configuration. `_____` are a collection of statements that are executed sequentially on the request or response of an API. Popular statements include format conversion from XML to JSON and call-rate limiting to restrict the number of incoming calls from a developer.

`_____` expressions can be used as attribute values or text values in any of the API Management policies, unless the `_____` specifies otherwise. Some policies such as the Control flow and Set variable policies are based on `_____` expressions.

`_____` can be applied at different scopes, depending on your needs: global (all APIs), a product, a specific API, or an API operation.

%

With **policies**, an API publisher can change the behavior of an API through configuration. **Policies** are a collection of statements that are executed sequentially on the request or response of an API. Popular statements include format conversion from XML to JSON and call-rate limiting to restrict the number of incoming calls from a developer.

**Policy** expressions can be used as attribute values or text values in any of the API Management policies, unless the **policy** specifies otherwise. Some policies such as the Control flow and Set variable policies are based on **policy** expressions.

**Policies** can be applied at different scopes, depending on your needs: global (all APIs), a product, a specific API, or an API operation.
