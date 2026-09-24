---
title: Show more information in the Share Dashboard window
description: Clarify users, groups, and roles in the Share Dashboard window so users can share with the right audience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/share-db-ref-qualifiers-more-info.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Share a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Show more information in the Share Dashboard window

Clarify users, groups, and roles in the **Share Dashboard** window so users can share with the right audience.

## Before you begin

Role required: admin

Reference qualifiers enable you to show more information when you search for users, groups and roles to share a dashboard with. For example, can add the email address and role to the user, so you can distinguish Jo User in support from Jo User in sales.

**Note:** If you're in the wrong application, select the link to edit the record.

\[Omitted image "app-mismatch-msg-sched-export.png"\] Alt text: Mismatched application message with link to edit the record

For more information on reference qualifier funcationality, see [Reference qualifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_ReferenceQualifiers.md).

## Procedure

1.  Navigate to **par\_dashboard\_permission\_list.do** to open the PAR Dashboard Permissions table.

2.  Right-click in the column header row and select **Configure** &gt; **Dictionary**.

    \[Omitted image "ref-qual-config-dictionary.png"\] Alt text: Menu path from table header to Configure &gt; Dictionary

3.  Open the dictionary entry for the User permission.

    \[Omitted image "ref-qual-dictionary-user.png"\] Alt text: Dictionary entries table with the User permission highlighted

4.  Select the Preview User button \[Omitted image "InfoIcon.png"\] Alt text: info buttonnext to User on the **Columns** tab to open the its dictionary entry.

5.  On the Attributes tab, create the attribute for `Reference auto completer columns` with the value `name;email;department` and select **Save**.


## Result

When you share a dashboard or data visualization, users with similar names are distinguished by email address and department.

\[Omitted image "ref-qual-in-action.png"\] Alt text: Dashboard sharing modal showing three employees with the same name but different email addresses. Two are in the same department but their email addresses distinguish them as well.

## What to do next

**Parent Topic:**[Share a Platform Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/share-db-in-ac.md)

