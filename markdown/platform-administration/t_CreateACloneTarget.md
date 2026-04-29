---
title: Register target instance \(legacy\)
description: A clone target record specifies the instance URL and credentials used for cloning.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Register instance, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Register target instance \(legacy\)

A clone target record specifies the instance URL and credentials used for cloning.

## Before you begin

Role required: clone\_admin

If an error occurs while registering a target instance see [Troubleshooting for registering target instance](../reference/register-target-instance-troubleshooting.md).

## Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Clone Targets**.

2.  Select **New**.

3.  Enter the URL for the receiving instance \(target\).

    The system validates the instance enables clone targets and that High Availability Cloning is active. Production and demonstration instances fail these validation checks.

4.  Enter the basic authentication credentials for a user account with the admin role on the target instance.

    **Note:** To clone multiple targets from one source, you must raise separate clone requests for each target.

    The system validates the user credentials have `clone_admin and soap` access to the target instance.

5.  Select **Submit**.

    The system checks connectivity and validates the user credentials against the target instance.


