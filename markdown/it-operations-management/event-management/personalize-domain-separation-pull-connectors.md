---
title: Personalize domains for pull connector events to use in event creation
description: Configure pull connectors to personalize domain separation of events so you can use them to create events in domains other than the user's currently logged-in or MID Server domain.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Connector domain personalization, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Personalize domains for pull connector events to use in event creation

Configure pull connectors to personalize domain separation of events so you can use them to create events in domains other than the user's currently logged-in or MID Server domain.

## Before you begin

Make sure that you have the following setup:

-   You have read access to the domain information table for the evt\_mgmt\_integration role \(default table: core\_company\). For more information, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   You enabled the **evt\_mgmt.connector\_enable\_custom\_domain\_separation** system property .
-   You installed the following plug-ins on your ServiceNow instance:

    -   Event Management **com.glideapp.itom.snac** plug-in
    -   Event Management connectors **sn\_em\_connector** plug-in
    -   Domain Support - Domain Extensions Installer **com.glide.domain.msp\_extensions.installer** plug-in
    You can download the plug-ins from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do).


Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances** &gt; **.**

2.  On the **Connector Instances** list, deactivate the connector instance of the connector for which you want to configure domain separation by selecting it and clearing the **Active** check box.

3.  Select **Update**.

4.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

5.  From the **Connector Definitions** list, select your connector definition.

6.  Determine whether all events should be created in a provided domain or determined by a domain provided in the payload of each event.

    1.  In the **Connector Parameters** table, double-click **Insert a new row**

    2.  Choose the event creation domain definition location.

        -   To have all events be created in the provided domain, enter `payloadDomainInfoFieldValue` in the **Name** column.
        -   To have events be created in the domain provided in the payload of the event, enter `payloadDomainInfoFieldName` in the **Name** column.
        **Note:** If both the **payloadDomainInfoFieldValue** and the **payloadDomainInfoFieldName** are provided, the domain provided in the payload of the event takes precedence.

    3.  Select **Update**.

7.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

8.  On the **Connector Instances** page, select your connector instance from the list.

9.  In the Connector Instance Values list, provide a value in the **Value** field of the parameters.

<table id="choicetable_bfv_4yr_3zb"><thead><tr><th align="left" id="d654994e292">

Parameter

</th><th align="left" id="d654994e295">

Value

</th></tr></thead><tbody><tr><td id="d654994e301">

**__payloadDomainInfoFieldValue__**

</td><td>

The value that will be used to match the domain record. For example, ServiceNow.

</td></tr><tr><td id="d654994e311">

**__payloadDomainInfoFieldName__**

</td><td>

The key in the payload that has the domain identifier. For example, if the payload key **company** holds the domain identifier, then the value in the **Value** column would provide the company information. For example:

-   **company**

\{

“source”: “Solarwinds”,

“host”: “127.0.0.1”,

“company”: “ServiceNow”

\}

**Note:** Dot-walking isn’t supported.

</td></tr></tbody>
</table>10. Select **Save**.

11. Select **Test Connector** to verify the connection between the MID Server and the connector.

    -   If the test is successful, a confirmation message appears.
    -   If the test fails, a message provides instructions to correct the problem.
    On a successful test, an onscreen message appears. If the test fails, follow the onscreen message instructions to correct the problem and then run another test.

    **Note:** Use a network tool such as `ping` to verify whether the credentials are correct and network connection from the MID Server to the connector server.

12. After the connector is verified, select the **Return to Connector Instance** link.

13. Activate the connector instance by selecting **Active** and **Update**.

14. Configure the domain for events by providing domain metadata through the connector parameters.

    For example, to use the User \[sys\_user\] table for a single connector instance in the **Connector Definitions** form, create parameters with the following names, and add their values in the **Connector Instance** form.

    -   **connectorDomainInfoTableName** - sys\_user

        **Note:** The table must be domain separated.

    -   **connectorDomainInfoColumnName** - user\_name
    -   **connectorDomainIdColumnName** - sys\_domain
    -   **connectorDomainPathColumnName** - sys\_domain\_path
    For more information, see [Connector domain metadata](../reference/connector-domain-metadata.md).

    | | | |
    |---|---|---|
    | | | |
    | | | |
    | | | |
    | | | |


## Result

The Event Management connector is set up for domain separation.

**Parent Topic:**[Event Management Connectors domain personalization](../concept/domain-separation-connectors-personalization.md)

