---
title: Create a new check timeout system property
description: Create a new timeout threshold property for a check if the glide.scan.process\_check.time\_out system property is not present. Setting of a timeout threshold prevents your instance from running a long check.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Implement a check timeout threshold, Timeout threshold, Configure, Instance Scan, Maintain and monitor, Administer]
---

# Create a new check timeout system property

Create a new timeout threshold property for a check if the **glide.scan.process\_check.time\_out** system property is not present. Setting of a timeout threshold prevents your instance from running a long check.

## Before you begin

Role required: admin.

## Procedure

1.  In the navigation filter, enter **sys\_properties.list**.

2.  Click **New** to create a new timeout system property.

3.  In the **Name** field, enter **glide.scan.process\_check.time\_out**.

4.  In the **Value** field, enter the check execution time in seconds.

    **Note:** The minimum allowed timeout threshold is 5 seconds. If you set the timeout to anything less than 5 seconds, the system still considers it to be 5 seconds. By default, it has been set to 600 seconds.


