---
title: Create an integration
description: You can create an integration and add the associated integration card to the Security Integrations screen. This procedure is intended for partners who create third-party integrations.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Operations Integration Configurations, ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Create an integration

You can create an integration and add the associated integration card to the Security Integrations screen. This procedure is intended for partners who create third-party integrations.

## Before you begin

Role required: sn\_sec\_cmn.admin

**Audience:**Partners who create third-party integrations.

## Procedure

1.  In the navigation filter, type sn\_sec\_core\_integration\_item.list and press the **Enter** key.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the integration.|
    |Plugin ID|The plugin that must be activated to use the integration.|
    |Order|Indicates the order that this integration card appears.|
    |Banner Text|Click the link, select an image or logo to appear in the integration card, and click **OK**.|
    |Installed|Read-only field that indicates whether the plugin has already been installed.|
    |Configurable|Indicates whether you can configure the integration.|
    |Categories|Used for filtering the integration cards.|
    |Short description|A description of the integration that appears in the tooltip hint for the card.|
    |Description|A longer description of the integration.|

4.  Right-click the form header and select **Save**.

    The **Integration and Configurations** related list appears. You can use this related list to define configuration options for the integration. These options appear when you click the **Configuration** button on the associated integration card.

5.  Click **New**.

6.  Fill in the fields on the form, as appropriate.

<table id="table_hcc_1pk_bw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

The name of the integration item.

</td></tr><tr><td>

Name

</td><td>

The plugin that must be activated to use the integration.

</td></tr><tr><td>

Integration

</td><td>

Displays the integration for which you are defining integration items

</td></tr><tr><td>

Order

</td><td>

Indicates the order in which this integration item appears.

</td></tr><tr><td>

Type

</td><td>

From the list, select the type of field:-   String
-   Integer
-   Decimal
-   Date
-   Boolean
-   Password
-   IPv4
-   IPv6
-   URL


</td></tr><tr><td>

Value

</td><td>

Enter the value associated with the **Type** selected. If a value that is invalid for the selected **Type** is entered, no records are retrieved when the integration is run. For example, if you select the URL type and enter a value of 12.32.23.10, no records are retrieved.

</td></tr></tbody>
</table>7.  Click **Submit**.


**Parent Topic:**[Security Operations Integration Configurations](../../security-operations-common/concept/third-party-integrations.md)

**Related topics**  


[Activate and configure third-party integrations](../../security-operations-common/task/install-config-3rd-party-integs.md)

