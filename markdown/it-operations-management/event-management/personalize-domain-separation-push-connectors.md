---
title: Personalize domains for push connector events to use in event creation
description: Configure push connectors to personalize domain separation of events so you can use them to create events in different domains other than the user's currently logged-in or MID Server domain.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Connector domain personalization, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Personalize domains for push connector events to use in event creation

Configure push connectors to personalize domain separation of events so you can use them to create events in different domains other than the user's currently logged-in or MID Server domain.

## Before you begin

Make sure that you have the following setup:

-   You have read access to the domain information table for the evt\_mgmt\_integration role \(default table: core\_company\). For more information, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   You enabled the **evt\_mgmt.connector\_enable\_custom\_domain\_separation** .system property.
-   You installed the following plug-ins in the ServiceNow AI Platform® instance:
    -   Event Management \(**com.glideapp.itom.snac**\)
    -   Event Management connectors \(**sn\_em\_connector**\)
    -   Domain Support - Domain Extensions Installer \(**com.glide.domain.msp\_extensions.installer**\)

        You can download the plug-ins from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do).


Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Push Connectors**.

2.  Open a push connector.

3.  On the **Push Connector** screen, scroll down to the **Push Connector Configurations** list and select **New**.

    **Note:** If this list is not displayed, you must create a push connector configuration parameter. For more information, see [Create a push connector configuration parameter](create-push-connector-configuration-parameter.md).

4.  In the **Push Connector Configurations** screen, determine whether events should be created in the provided domain or the domain provided in the payload of each event.

<table id="choicetable_jm5_rmb_d1c"><thead><tr><th align="left" id="d251651e187">

Domain creation location

</th><th align="left" id="d251651e190">

Parameter and values

</th></tr></thead><tbody><tr><td id="d251651e196">

**The provided domain**

</td><td>

-   **Field name**: payloadDomainInfoFieldValue
-   **Value**: domain-identifier


</td></tr><tr><td id="d251651e218">

**The domain provided in the payload of each event**

</td><td>

-   **Field name**: payloadDomainInfoFieldName
-   **Value**: field-name-in-payload
 Example: If the payload key “company” holds the domain identifier, then “company” is the value.

 -   **“company”**

\{

“source”: “Solarwinds”,

“host”: “127.0.0.1”,

“company”: “ServiceNow”

\}

</td></tr></tbody>
</table>    **Note:** If both the **payloadDomainInfoFieldValue** and the **payloadDomainInfoFieldName** parameters are provided, then the **payloadDomainInfoFieldName** takes precedence.

5.  Select **Submit**.


## Result

Events are created in the domain referred to by the domain identifier.

**Note:** The table that stores domain information records \(for example, core\_company\) must be domain separated. For more information, see [Domain-separate a custom table](https://www.servicenow.com/docs/access?context=bp-ds-custom-table&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[Event Management Connectors domain personalization](../concept/domain-separation-connectors-personalization.md)

**Related topics**  


[Integrate with push connectors](configure-listener-transform-script.md)

[Connector domain metadata](../reference/connector-domain-metadata.md)

