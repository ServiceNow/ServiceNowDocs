---
title: Assign OT admin roles with ServiceNow Otto for Setup
description: Create users and assign the necessary Operational Technology \(OT\) admin roles to users managing configuration and operational control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/assign-ot-admin-roles-sn-otto-setup-ot.html
release: australia
topic_type: task
last_updated: "2026-08-22"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Setup, Operational Technology]
---

# Assign OT admin roles with ServiceNow Otto for Setup

Create users and assign the necessary Operational Technology \(OT\) admin roles to users managing configuration and operational control.

## Before you begin

Role required: admin

## Procedure

1.  Access the Admin Home by logging in to your instance or navigating to **All** &gt; **Admin Center** &gt; **Admin Home**.

2.  Locate and select the **Operational Technology** card.

3.  In the **Configure your product** section, select **Configure** to open the configuration console.

4.  In the **Operational Data** section, expand the **Role Assignment** module and select **Assign Admins**.

5.  In the **User** field, search for and select the admin user to assign an OT admin role to.

6.  In the **Roles** field, select one or more admin roles as needed.

    The Implementation Agent \(sn\_ia\_config.ia\_user\) role and at least one admin role are required to complete this step.

7.  Select **Assign roles**.

    Any roles already assigned to the selected user are skipped.

8.  When you're finished assigning admin roles, select **Mark as configured**.


## Result

If all role assignments are successful, you see a `Roles assigned successfully` alert.

If there are errors during the role assignment process, you will see an alert. For more information about error causes and alerts for OT Setup, see [Role assignment alerts for Operational Technology Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/alerts-ot-setup.md).

**Parent Topic:**[Use Operational Technology Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/use-ot-setup.md)

