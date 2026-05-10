---
title: Configure widget security
description: Configure widget security to ensure that your widget is being accessed only by the intended audience.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure widget security

Configure widget security to ensure that your widget is being accessed only by the intended audience.

## Before you begin

Role required: admin or sp\_admin

## About this task

There are several ways to configure widget security:

-   Restrict the widget to users with a login only \(authenticated users\)
-   Restrict the widget to users with certain roles only
-   Restrict which tables a public widget can access and return data from for guest \(unauthenticated\) users

When you configure widget security, configure the page security accordingly so that users can access the widget via the page on which it appears. For more information, see [Configure page security by role](configure-page-security.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Open the record of the widget to configure.

3.  On the form, configure the widget security.

<table id="choicetable_n5r_xyt_hkb"><thead><tr><th align="left" id="d36978e103">

Option

</th><th align="left" id="d36978e106">

Procedure

</th></tr></thead><tbody><tr><td id="d36978e112">

**Restrict the widget to authenticated users**

</td><td>

Clear the **Public** check box and leave the **Roles** field blank.

</td></tr><tr><td id="d36978e127">

**Restrict the widget to certain roles**

</td><td>

1.  Clear the **Public** check box.
2.  Next to **Roles**, select the edit icon \(![Edit icon](../image/edit-icon.png)\).
3.  On the Roles window, select a role by moving it from the **Available** list to the **Selected** list.
4.  Select **Done**.


</td></tr><tr><td id="d36978e172">

**Restrict which tables public widgets can access for guest users**

</td><td>

1.  Select the **Public** check box.

**Note:** Public widgets are accessible by any user even if the **Roles** list contains roles.

2.  Specify the tables that public widgets can access for guest users.

This applies to widgets that accept the table input parameter only.

    1.  In the **Public Table Allow List** related list, select **New**.
    2.  In the **Tables** field, select a table from which guest users can access data in the widget.
    3.  Select **Submit**.
    4.  Repeat these steps to add additional tables.
3.  In the **Server script** field, call the SPWidgetAccessControl API before any call to GlideRecord\(options.table\) and GlideRecordSecure\(options.table\). For example:

    ```javascript
if(!new global.SPWidgetAccessControl().hasPublicAccess(options.table, $sp, options, input)){
		gs.warn("Deny access to table which is not public: " + options.table);
		data.isValid = false;
		return;
	}
    ```

The parameters passed with SPWidgetAccessControl should be the same as those passed with GlideRecord\(options.table\) and GlideRecordSecure\(options.table\). For details on the SPWidgetAccessControl API, see [SPWidgetAccessControl - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/SPWidgetAccessControlGlobalAPI.md).

4.  Select **Save**.


</td></tr></tbody>
</table>4.  Select **Update**.


**Parent Topic:**[Managing portal access](../concept/portal-security.md)

