---
title: Domain separation and the Password Reset application
description: Domain separation is supported in the Password Reset application. A password reset process that you define in any domain is isolated from a process that you create in any other domain. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and the Password Reset application

Domain separation is supported in the Password Reset application. A password reset process that you define in any domain is isolated from a process that you create in any other domain. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works in Password Reset

Domain separation for Password Reset is applied at the process level. The admin configures the following elements to define a password reset process: A connection to a credential store, user groups that can use the process, method of identification, and verifications to use during the process.

-   A connection to the credential store where user credentials \(like username/password\) are securely stored. Each connection inherits the domain setting from a template called a connection type. Each connection type is tied to a domain \(the connection type record has a domain field\). There are uniqueness constraints on connection names within a domain.
-   One or more user groups on the ServiceNow instance that can use the password reset process. User accounts are members of one or more domains — they use the standard ServiceNow domain separation. When a user enrolls to use one of the password reset processes that is configured for the organization, the user is allowed to choose only from the processes in the user’s domain.
-   The identification — the method that the end user employs to claim identity for the public password reset or password change process. Each identification inherits the domain setting from a template called an identification type. Each identification type is tied to a domain \(the identification type record has a domain field\). There are uniqueness constraints on identification names within a domain.
-   One or more verifications — methods to verify the identity of the person who is attempting to reset the password. Each verification inherits the domain setting from a template called a verification type. Each verification type is tied to a domain \(the verification type record has a domain field\). There are uniqueness constraints on verification names within a domain.
-   All Password Reset tables have a domain column.
-   Password Reset process tables include a **sys-overrides** column on business rules, UI actions, and so on.
-   The Password Reset application is built using Orchestration. Orchestration supports "Data only" domain separation — the data security model of separating visibility of data from one domain to another.

## Password Change process

The Password Change application extends the Password Reset application by letting admins define how users change their passwords. A service desk-assisted process is not supported. An admin must publish the URL for the self-service password change form.

The Password Change application enables an end user to change a password over the Internet using a browser on any supported interface, including mobile devices. The end user can select from any configured process in the end user’s domain \(or child domain of an end user’s domain\).

A password change process uses the same elements as a password reset process \(connections, user groups, identifications, and verifications\), with the same domain-separation features.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

