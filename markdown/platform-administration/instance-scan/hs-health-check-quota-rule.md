---
title: Implement a check timeout threshold
description: Set the execution time of an individual check by implementing timeout system property. Setting of a timeout threshold prevents your instance from running a long check.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Timeout threshold, Configure, Instance Scan, Maintain and monitor, Administer]
---

# Implement a check timeout threshold

Set the execution time of an individual check by implementing timeout system property. Setting of a timeout threshold prevents your instance from running a long check.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter **sys\_properties.list**.

2.  From the System Properties list, select **glide.scan.process\_check.time\_out**.

    **Note:** If **glide.scan.process\_check.time\_out** is not present in the list, see [Create a new check timeout system property](hs-create-new-heath-check-timeout.md) for more information.

3.  In the **Value** field, set the execution time for the check in seconds.

    **Note:** The minimum allowed timeout threshold is 5 seconds. If you set the timeout to anything less than 5 seconds, the system still considers it to be 5 seconds. By default, it has been set to 600 seconds.


## Result

A timeout threshold for a check is set by the user. Individual checks will be cancelled after the set time threshold exceeds.

