---
title: Create a confidential record
description: Create a record and mark it as confidential so that you can make sure that only the users with a specific role can access it.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Confidential records, Common GRC features, Governance, Risk, and Compliance]
---

# Create a confidential record

Create a record and mark it as confidential so that you can make sure that only the users with a specific role can access it.

## Before you begin

Role required: sn\_grc.admin, sn\_grc.business\_user who has opened the risk event, sn\_audit.user, sn\_compliance.user, sn\_esg.user, sn\_risk.user

## Procedure

1.  Navigate to **All &gt; Administration &gt; GRC Properties**.

2.  Select **Yes** for **Enable record level confidentiality** property and select **Save**.

    Perform the following steps by logging in with the sn\_grc.business\_user role or a module specific role as defined in the Role required section.

3.  Navigate to the record that should be marked as confidential and select **Confidentiality** tab.

4.  On the **Confidentiality** tab, select the **Confidential** option.

    The Allowed users and Allowed groups lists are displayed. The user who enables the **Confidential** option is auto-appended to the Allowed users list by default.

5.  To add more users, update the Allowed users list.

    Allowed users can update the confidential record.

6.  To add more groups, update the Allowed groups list.

    Allowed groups can update the confidential record.

7.  Select **Update**.


## Result

The selected record is marked as confidential. Only the users who belong to the Allowed users list or the Allowed groups list can access this confidential record.

**Parent Topic:**[Confidential records](../concept/confidential-records.md)

