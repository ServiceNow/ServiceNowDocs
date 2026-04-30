---
title: Create connector alias and connection credentials
description: Enter the connection URL and credential alias details for your API connector.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-20"
reading_time_minutes: 3
breadcrumb: [Creating your own API connector, Use the workspace, Security Posture Control, Security Operations]
---

# Create connector alias and connection credentials

Enter the connection URL and credential alias details for your API connector.

## Before you begin

You must have a set of test credentials handy to configure your API connector and test the connection. Note that you use these test credentials for building and testing the connector. These aren’t the connection URL and credentials that the system uses once your API connector is published. You must complete this step before you can proceed.

Select the **Learn how to create a connection and credential alias** link for more information before you start. You can keep this page open in your browser as a tab as you fill in the fields for this step. You can create and share these credentials across APIs so that you don't have to create and enter multiple sets of credentials if you want more than one instance of an API connector.

Role required: sn\_sec\_spc\_core.developer

## Procedure

1.  Fill in the Alias and Connection fields.

    **Note:** If a message is displayed that prompts you to change your application scope, update it to the `Security Posture Control API Connectors` scope as directed.

2.  Select the **Create new** link to the right of the Alias field to create a \(Credential\) alias.

    1.  In the Connection and Credential Aliases record, enter a unique name for your API connector's alias.

    2.  Select the search ![Magnifying glass](../../../common/image/List_SearchIcon.png) icon on the Parent Alias field and select one.

        If you select a parent alias from the list, this record points to another alias record. If you select a parent alias some fields on the form are no longer displayed, and you can submit your changes.

    3.  Select **Submit**.

    4.  Select the refresh icon \(![Rotating arrows that refresh the page](../../../reuse/icons/product-icons/sync-outline-24.svg)\) to see your alias on the list.

    5.  Select your alias.

    6.  Select the **Create new** link next to the Connection field.

        A new HTTP\(s\) Connection record is displayed. Fill out the fields to create a connection for your alias.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for the connection.|
        |Active|Record is activated by default.|
        |Credential|You must select a credential from the list.|
        |Domain|\(Optional\) Global is displayed.|
        |Connection Alias|Select a credential alias from the list. Alternatively, enter an alias. The connection alias must match the associated alias that you created or selected for the Alias field in the previous step.|
        |Connection URL|If the URL builder is not selected, enter the connection URL in `HTTP://` or `HTTPS://` format.|
        |Use MID Server|A MID Server isn’t required. If you select this check box, fill out the fields for your MID Server.|
        |Connection timeout|This value isn’t required. Leave this field empty to use the system default connection timeout value. Don't enter 0 as a value. Alternatively, enter a value for the number of milliseconds the system waits for a successful host connection. If a successful connection doesn’t occur during this time, the connection request times out.|

    7.  Select **Submit**.

    8.  Select the refresh icon \(![Rotating arrows that refresh the page](../../../reuse/icons/product-icons/sync-outline-24.svg)\) for the Connection field to see your connection on the list.

    9.  Select your connection.

        The base URL and credential are displayed in read-only fields. These connections are associated with the alias that you choose. This list isn’t a complete list.

        If you don’t see the Credential field, you can select the view connection link \(![Open link icon](../../../reuse/icons/product-icons/open-link-right-fill-24.svg)\) icon next to the Connection field.

        In the form that is displayed, add the Credential in the Credential field. You must have the credential field populated before you can save the record.

3.  Select **Update**.

4.  Select **Save and continue** to save your edits.

    You must save your changes before you can continue.

    After you save your edits, the [Select template](spc-sgc-template-stepper-3.md) step is displayed and highlighted on the stepper.


Select the view connection link \(![Open link icon](../../../reuse/icons/product-icons/open-link-right-fill-24.svg)\) if you see the following message: `There are no credentials associated with the selected connection. Please update the connection via the View connection button.`

