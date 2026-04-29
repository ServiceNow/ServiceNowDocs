---
title: Set up the Virtual Agent integration with Facebook Messenger \(Legacy\)
description: Configure the Virtual Agent integration for Facebook Messenger and associate the app with your instance.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Legacy setup and configuration, Configure, Conversational Integration with Facebook Messenger, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up the Virtual Agent integration with Facebook Messenger \(Legacy\)

Configure the Virtual Agent integration for Facebook Messenger and associate the app with your instance.

## Before you begin

You should already have the following:

-   Facebook page \(see [https://www.facebook.com/pages/creation/](https://www.facebook.com/pages/creation/) for more information\)
-   Facebook developer account \(see [https://developers.facebook.com/](https://developers.facebook.com/) for more information\)
-   Facebook app \(see [https://developers.facebook.com/quickstarts](https://developers.facebook.com/quickstarts) for more information, make note of the app secret that is generated\)

Roles required:

-   virtual\_agent\_admin and external\_app\_install\_admin or admin
-   Administrator for third-party applications

## Procedure

1.  In Facebook developer, navigate to **Messenger** &gt; **Settings**.

    1.  Locate the Token Generation section.

    2.  From the page list, select the Facebook page you created and make note of the Page Access Token that is generated.

    3.  Locate the Webhooks section and click **Setup Webhooks**.

    4.  On the New Page Subscription pop-up window that displays, enter these fields:

        |Field|Value|
        |-----|-----|
        |Callback URL|Your ServiceNow instance URL followed by `/api/now/v1/cs/adapter/messenger/message`|
        |Verify Token|`nowbot`|
        |Subscription Fields|Select **messages** and **messaging\_postbacks**|

    5.  Click **Verify and Save**.

2.  In your ServiceNow instance, enter `hash_message_verification.list` in the Filter navigator.

    1.  In the Hash Message Verifications form, click **New** to create a new record.

    2.  Enter these fields:

        |Field|Value|
        |-----|-----|
        |Name|Name that helps to identify this record. This field may default to `sample-fb-messenger-inbound-app-token` but this default can be changed.|
        |Description|Description for the record|
        |Secret|App secret of your Facebook Messenger app \(the secret was generated when you created the app\)|

    3.  Click **Submit**.

3.  In your ServiceNow instance, enter `token_verification.list` in the Filter navigator.

    1.  In the Token Verifications form, click **New** to create a new record.

    2.  Enter these fields:

        |Field|Value|
        |-----|-----|
        |Name|Name that helps to identify this record. This field may default to `sample-fb-messenger-outbound-app-token` but this default can be changed.|
        |Description|Description for the record|
        |Token|Page access token of your Facebook Messenger app \(from step 1b of this procedure\)|

    3.  Click **Submit**.

4.  In your ServiceNow instance, enter `message_auth.list` in the Filter navigator.

    1.  In the Message Auth page, click **New** to create a new record.

    2.  Enter these fields:

        |Field|Value|
        |-----|-----|
        |Name|Name that helps to identify this record. This field may default to `sample-fb-messenger-app` but this default can be changed.|
        |Provider|Name of the provider|
        |Inbound message verification|Name specified on the Hash Message Verifications form \(this token verifies if the request is actually from the provider\)|
        |Outbound message creation|Name specified on the Token Verification form \(this token interacts with the provider on behalf of the user\)|

    3.  Click **Submit**.

5.  In your ServiceNow instance, enter `sys_cs_adapter_configuration_page_messenger.list` in the Filter navigator.

    1.  In the Facebook Messenger Adapter Configuration Page, click **New** to create a new record.

    2.  Enter these fields:

        |Field|Value|
        |-----|-----|
        |App Type|Defaults to Facebook Messenger and cannot be changed|
        |Messenger Page ID|Your page ID \(the page ID can be found in the URL of the Facebook page\)|
        |Name|Name that helps to identify this record. This field may default to `sample-fb-messenger-app` but this default can be changed.|
        |Provider Auth|Name specified on the Message Auth page|

6.  Click **Submit**.

7.  Configure whether users should be prompted to link their profile to their ServiceNow profile.

    1.  In the Navigation filter, enter `sys_properties.list`.

    2.  Navigate to and click **va.messenger.account.auth**.

    3.  In the **Value** field, enter **true** or **false**.

<table id="table_ihb_fnt_qjb"><tbody><tr><td>

true

</td><td>

Prompt users to link their account to their ServiceNow profile. Users who link their account to their ServiceNow profile can access all topics and also chat with a live agent. Users who do not link their account can access only guest topics.

</td></tr><tr><td>

false

</td><td>

Do not prompt users to link their account to their ServiceNow profile. Users can access only guest topics but can still chat with a live agent.

</td></tr></tbody>
</table>    4.  Click **Update**.


**Parent Topic:**[Legacy setup and configuration](../concept/legacy-va-fb-messenger-setup.md)

