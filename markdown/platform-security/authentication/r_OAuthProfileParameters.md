---
title: OAuth parameters for default profile support
description: The default profile feature requires a set of parameters that you can use with the setParameter\(\) API to specify the OAuth requestor, a context for the request, and the provider profile.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [OAuth Outbound, OAuth Inbound and Outbound authentication, Authentication, Access Management]
---

# OAuth parameters for default profile support

The default profile feature requires a set of parameters that you can use with the setParameter\(\) API to specify the OAuth requestor, a context for the request, and the provider profile.

In the OAuth provider scenario, you must set three parameters that tell the OAuth provider which OAuth profile to use by default. When these three parameters are set, the access token is saved in the instance database. Use the parameters with GlideOAuthClientRequest.

|Parameter|Description|
|---------|-----------|
|`oauth_requestor`|The sys\_id of the object, which can be a user record or an email account.|
|`oauth_requestor_context`|Descriptor that provides context for the OAuth requestor. As a good practice, use the name of the table where the `oauth_requestor` object is saved.|
|`oauth_provider_profile`|The sys\_id of the OAuth profile record that is the default \(see [Specify an OAuth profile](https://www.servicenow.com/docs/access?context=t_SpecifyAnOAuthProfile&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)\).|

You do not need to use parameters to set the grant type and scope because the values are configured in the OAuth profile record. If you do not use the parameters, you can use the GlideOAuthClientRequest API methods setScope and setGrantType. For additional information, see [setScope](https://www.servicenow.com/docs/access?context=c_GlideOAuthClientRequest&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) and [setGrantType](https://www.servicenow.com/docs/access?context=c_GlideOAuthClientRequest&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

