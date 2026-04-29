---
title: Create the Client Credentials system property
description: Create the glide.oauth.inbound.client.credential.grant\_type.enabled system property to use Client Credentials grant type for OAuth inbound integrations.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client Credentials, Old Inbound integrations experience, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Create the Client Credentials system property

Create the `glide.oauth.inbound.client.credential.grant_type.enabled` system property to use Client Credentials grant type for OAuth inbound integrations.

## Before you begin

Role required: oauth\_admin

Plugin required: OAuth 2.0.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Select **New**.

3.  On the form, fill the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the property you’re creating. In this case, `glide.oauth.inbound.client.credential.grant_type.enabled`.|
    |Description|Type a brief, descriptive phrase describing the function of the property.|
    |Type|Select the appropriate data type from the list. In this case, `true| false`.|
    |Value|Set the desired value for the property. In this case, `true` to enable the client credentials grant type for OAuth inbound integrations.|

    ![Client Credentials property](../images/create-cc-sys-prop.png)

    **Note:** Other fields in the form such as Choices, Ignore cache, Private, Read roles, and Write roles can be configured according to your requirements.

4.  Select **Submit**.

    **Note:** If the **Ignore cache** check box is selected, the system flushes the server cache when the parameter is changed.

    Next, you must create an OAuth client \(OAuth API endpoint for external client\) and add OAuth Application User field to the OAuth client record.


