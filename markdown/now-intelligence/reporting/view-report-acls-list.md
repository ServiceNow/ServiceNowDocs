---
title: The report\_view ACLs list
description: View the entire list of report\_view ACLs and their associated roles to have a higher-level view of the access control on your instance.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACL Assessment for Reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# The report\_view ACLs list

View the entire list of report\_view ACLs and their associated roles to have a higher-level view of the access control on your instance.

Each instance has a different number of report\_view ACLs. The number depends on the plugins activated on the instance.

To view the report\_view ACLs list, navigate to **All** &gt; **Reports** &gt; **ACL Assessment for Reports** &gt; **Report View ACLs List**.

## report\_view ACLs list columns

ACLs apply to only one role at a time. There can be multiple instances of an ACL if there are multiple roles that it applies to. For example, the same ACL grants greater report access to an admin than to an itil user.

|Column|Description|
|------|-----------|
|ACL|The name of the report\_view ACL.|
|Active|Indicates whether the ACL is active. True/False.|
|Application|The application the ACL applies to.|
|Package|The plugin associated with the ACL.|
|Description|What the ACL prevents or allows for the associated role.|
|Role|The name of the role the ACL applies to.|
|Description|Description of the role.|

**Parent Topic:**[ACL Assessment for Reports](../concept/report-view-acl-dashboard.md)

