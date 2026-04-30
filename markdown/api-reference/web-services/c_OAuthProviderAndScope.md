---
title: OAuth profiles and scopes
description: In the OAuth provider scenario, profiles and scopes specify the grant type, authorization type, and level of access.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use a third-party OAuth provider, Configure a message with OAuth, Outbound REST authentication, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# OAuth profiles and scopes

In the OAuth provider scenario, profiles and scopes specify the grant type, authorization type, and level of access.

In the OAuth provider scenario, the OAuth profile refers to a combination of a grant type and at least one scope. The scope specifies the access that the user has to the protected resource, such as **read** or **write**. You can create a profile for each third-party provider and obtain the specific set of scopes from the provider. See [Specify an OAuth profile](../task/t_SpecifyAnOAuthProfile.md) and [Specify an OAuth scope](../task/t_SpecifyAnOAuthScope.md) for more information. The instance also uses OAuth profiles when a REST call specifies OAuth 2.0 authentication. The instance auto-creates a default profile for each third-party provider record that you create. There can be only one default profile.

Specify the following parameters, which are saved in the OAuth Requestor Profile \[OAuth\_requestor\_profile\] table:

|Parameter|Description|
|---------|-----------|
|`oauth_requestor`|The sys\_id of the object, which can be a user record or an email account.|
|`oauth_requestor_context`|Descriptor that provides context for the OAuth requestor. As a good practice, use the name of the table where the `oauth_requestor` object is saved.|
|`oauth_provider_profile`|The sys\_id of the OAuth profile record that is the default \(see [Specify an OAuth profile](../task/t_SpecifyAnOAuthProfile.md)\).|

When the user attempts to authenticate, the provider accesses the OAuth Requestor Profile table to look for the user. If the user is found, the authentication is successful. If not, the provider accesses the default profile to determine the grant type and how to proceed with the authentication.

-   **[Specify an OAuth profile](../task/t_SpecifyAnOAuthProfile.md)**  
An OAuth profile includes the grant type that the third-party OAuth provider needs to obtain access to the restricted resource.
-   **[Specify an OAuth scope](../task/t_SpecifyAnOAuthScope.md)**  
Specify the OAuth scopes that you get from the provider. Scopes can be any level of access specified by the provider, such as read, write, or any string, including a URL.

**Parent Topic:**[Use a third-party OAuth provider](../task/t_UseAThirdPartyOAuthProvider.md)

