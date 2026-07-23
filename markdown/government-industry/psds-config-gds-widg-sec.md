---
title: Configure widget security in the GDS Service Portal by role
description: Configure widget security to verify that your GDS Service Portal widgets are being accessed only by the intended audience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-gds-widg-sec.html
release: australia
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Manage Portal Access by role, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure widget security in the GDS Service Portal by role

Configure widget security to verify that your GDS Service Portal widgets are being accessed only by the intended audience.

## Before you begin

Role required: admin or sp\_admin

## About this task

There are several ways to configure widget security:

-   Restrict the widget to users with a login only \(authenticated users\)
-   Restrict the widget to users with certain roles only
-   Restrict which tables a public widget can access and return data from for guest \(unauthenticated\) users

When you configure widget security, configure the page security accordingly so that users can access the widget via the page on which it appears. For more information, see [Configure page security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-page-sec.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Open the record of the widget to configure.

3.  On the form, configure the widget security.

<table id="choicetable_n5r_xyt_hkb"><thead><tr><th align="left" id="d27053e113">

Option

</th><th align="left" id="d27053e116">

Procedure

</th></tr></thead><tbody><tr><td id="d27053e122">

**Restrict the widget to authenticated users**

</td><td>

Unselect the check box next to **Public** and leave the **Roles** field blank. This will display the widget to ALL users with a login.

</td></tr><tr><td id="d27053e137">

**Restrict the widget to certain roles**

</td><td>

1.  Clear the **Public** check box.
2.  Next to **Roles**, select the edit icon \(\[Omitted image "edit-icon.png"\] Alt text: Edit icon\).
3.  In the Roles related list, select a role by moving it from the **Available** list to the **Selected** list.
4.  Select **Done**.


</td></tr></tbody>
</table>4.  Select **Update**.


## What to do next

For more information on configuring portal access by role, see [Managing portal access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/portal-security.md).

**Parent Topic:**[Manage role-based access to pages and widgets in GOV.UK Design System Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-man-acc.md)

**Previous topic:**[Configure page security in the GDS Service Portal by role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gds-page-sec.md)

**Next topic:**[Configure the Grants Management Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-grants-management-portal.md)

