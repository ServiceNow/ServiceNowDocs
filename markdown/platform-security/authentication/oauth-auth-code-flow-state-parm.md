---
title: Authorization code flow state parameter requirement
description: The glide.oauth.state.paramater.required system property enables the State parameter to be required in an OAuth request for authorization code flow.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth authorization code grant flow, Old inbound integrations experience, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Authorization code flow state parameter requirement

The glide.oauth.state.paramater.required system property enables the State parameter to be required in an OAuth request for authorization code flow.

## State parameter

Role required: none.

Beginning in the Madrid release, the system property **glide.oauth.state.parameter.required** adds a State parameter for an OAuth request. For zbooted instances, the property is true. For upgraded instances, the property is not present, so the State parameter is not enabled. The State parameter is a string value, and should not contain special characters. The State parameter cannot be empty or “ ”.

## Validating the state parameter

Create an endpoint for clients to access the instance. Initiate an authorization code flow for an oauth\_auth.do. For example:

```
http://myinstance.service-now.com/oauth_auth.do?grant_type=authorization_code&client_id=e9dba45b380d1300e676ccc91cef468f&response_type=code
```

If you do not specify the state parameter in the request, you get an error and the authorization code is not returned.`Missing State parameter in request.`

Adding the State parameter to the request:

```
http://myinstance.service-now.com/oauth_auth.do?grant_type=authorization_code&client_id=e9dba45b380d1300e676ccc91cef468f&response_type=code&state=123
```

Adding the State parameter redirects you to the login screen and the regular authorization code flow returns the authorization code.

**Note:** The response URL contains the state parameter passed in the request. In the example, the added parameter is `state=123`.

If the authorization code flow starts from oauth\_initiator.do:

```
http://myinstance.service-now.com/oauth_initiator.do?oauth_requestor_context=sys_rest_message&amp;oauth_requestor=eab8341fec0d1300964f214a2c2fcf67&amp;oauth_provider_profile=dfa8f01fec0d1300964f214a2c2fcf51&amp;response_type=code
```

The State parameter is automatically added when redirected by oauth\_auth.do.

```
http://myinstance.service-now.com/oauth_auth.do?response_type=code&amp;state=-790938844&amp;redirect_uri=http://10.11.95.5:16001/oauth_redirect.do&amp;client_id=e9dba45b380d1300e676ccc91cef468f
```

