---
title: Configure extension point for Product search API
description: The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point provides the configuration that punchout suppliers can use to ensure that all details about their product, such as product's name, brand, manufacturer, price, availability, SKU, and so on, is displayed in Shopping Hub.View the format of the sn\_spend\_intg.ThirdPartySystemApiExtension extension point.Create script include that enables you to display all the products details for the punchout supplier in Shopping Hub.Create an extension instance to associate the punchout supplier's script include with the sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure punchout for third-party site purchases, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure extension point for Product search API

The sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point provides the configuration that punchout suppliers can use to ensure that all details about their product, such as product's name, brand, manufacturer, price, availability, SKU, and so on, is displayed in Shopping Hub.

**Parent Topic:**[Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md)

## View the third-party system API extension point format

View the format of the sn\_spend\_intg.ThirdPartySystemApiExtension extension point.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, search for `sn_spend_intg.ThirdPartySystemApiExtension` and then select the link to open the extension point.

    View the format of the extension point script.


## Create script include for punchout supplier products

Create script include that enables you to display all the products details for the punchout supplier in Shopping Hub.

### Before you begin

Role required: admin

### About this task

Ensure that the application scope is set to Shopping Hub.

### Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Script Includes**.

2.  Select **New**.

3.  On the Script Include form, fill in the fields.

<table id="table_mfv_c51_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the script include.

</td></tr><tr><td>

API Name

</td><td>

Read-only and auto-populated API name.

</td></tr><tr><td>

Application

</td><td>

The application where this script include resides. For example, Shopping Hub.

</td></tr><tr><td>

Accessible from

</td><td>

Sets which applications can access this script include.

</td></tr><tr><td>

Glide AJAX callable

</td><td>

Makes the script include available to client scripts, list/report filters, reference qualifiers, or if specified as part of the URL.

</td></tr><tr><td>

Mobile callable

</td><td>

Option to make the script include available on the mobile device.

</td></tr><tr><td>

Sandbox enabled

</td><td>

Option to let a client make changes to their script include without causing global affecting.

</td></tr><tr><td>

Active

</td><td>

Enables the script include when selected. Deselect the active field to disable the script include.

</td></tr><tr><td>

Description

</td><td>

Provides descriptive content regarding the script include.

</td></tr><tr><td>

Script

</td><td>

The server-side script to run when called from other scripts.The script must define a single JavaScript class or a global function. The class or function name must match the Name field.

</td></tr><tr><td>

Protection policy

</td><td>

Protection policy for script includes published as part of a custom application.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Create extension instance for the scripted extension point

Create an extension instance to associate the punchout supplier's script include with the sn\_spend\_intg.ThirdPartySystemApiExtension scripted extension point.

### Before you begin

Role required: admin

### About this task

An extension instance is a registered instance of a scripted extension point that links a script include with a scripted extension point.

**Note:** Ensure that the application scope is set to Shopping Hub.

### About this task

### Procedure

1.  Select All and in the search filter, enter **sys\_extension\_instance.LIST**, and then press enter or return on your keyboard.

2.  Select **New**.

3.  In the **Point** field, enter **sn\_spend\_intg.ThirdPartySystemApiExtension**.

4.  In the **Class** field, select the script include that you created.

    For more information, see [Create script include for punchout supplier products](configure-ext-point-punchout.md#).

5.  In the **Order** field, enter a number.

    When multiple extension instances are available, the one with the least order value takes precedence.

6.  Select the **Active** check box.

7.  Select **Submit**.


