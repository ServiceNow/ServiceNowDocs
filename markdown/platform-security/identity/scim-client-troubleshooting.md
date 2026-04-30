---
title: Troubleshoot SCIM Client
description: Troubleshooting actions can help resolve common issues when setting up or running the SCIM Client.
locale: en-US
release: zurich
product: Identity
classification: identity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Troubleshoot SCIM Client

Troubleshooting actions can help resolve common issues when setting up or running the SCIM Client.

<table id="table_mxt_czm_htb"><thead><tr><th>

Issue

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Response contains the following message:

 ```
“message":"Unable to access the
table core_company with id: 0c441abbc6112275000025157c651c89,
Please cross check the Access control rules"
```

</td><td>

The message is displayed if the API is called in a user context and the user does not have access to the table.

 You must make sure that the scriptable API is called in the system context.

</td></tr><tr><td>

Response contains the following message:

 ```
{"message":"User Not Authenticated","detail":"
Required to provide Auth information”}
```

</td><td>

-   Make sure that the token is generated through the corresponding REST message and it is valid.
-   Make sure that the scriptable API is called in the system context.

</td></tr><tr><td>

Response contains the following message:

 ```
Script execution failed, the reason is:
Cannot cast java.lang.Integer to java.lang.String 
```

</td><td>

In the SCIM attribute mapping, if the field is defined to fetch from a script with this issue, then make sure that the return type should always be a string.

</td></tr><tr><td>

Response contains the following message:

 ```
"status": "400", 
"scimType": "invalidValue", 
"detail": "Manager id : 02826bf03710200044e0bfc8bcbe5ds8 
doesn't exist"  
```

</td><td>

For any SCIM attribute that expects the ID, then that ID is always of the provider system. Make sure the ID that is passed in the payload is valid in the provider system.

</td></tr></tbody>
</table>## Areas to check for troubleshooting

The following are some of the areas that can be checked for troubleshooting errors when using the SCIM Client:

-   If any issue is found while running any of the scriptable APIs, see the SCIM Client logs section.

    |Field|Description|
    |-----|-----------|
    |Request ID|Unique ID that represents a scriptable API called.|
    |SCIM Provider|Provider name for which the API is called.|
    |Resource|Name of the resource for which the API is called.|
    |Resource ID|The ID for which the API is called. For deletion, the ID represents the resource ID in the provider system and the ID is in the client system.|
    |Action|API that is called|
    |Status|Status of the log as a success or failure|
    |Message|Success or error message. The error message can be from the SCIM provider or because of configuration issues in the SCIM Client.|

-   Check the request body by configuring and viewing outbound calls. To learn more, see [Outbound web services logging](https://www.servicenow.com/docs/access?context=outbound-request-logging&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Update log levels by adding the content-type, testing the sample, and navigating to corresponding the HTTP Method form in the REST message of the corresponding provider.
-   If the request body is truncated, then increase the limit by using system property **glide.outbound\_http.content.max\_limit**.

