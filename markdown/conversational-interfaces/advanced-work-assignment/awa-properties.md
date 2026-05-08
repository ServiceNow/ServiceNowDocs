---
title: Properties for Advanced Work Assignment
description: The Advanced Work Assignment Properties page provides configuration options for AWA.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Properties for Advanced Work Assignment

The Advanced Work Assignment Properties page provides configuration options for AWA.

If you have the admin role, you can create or change these properties by navigating to **System Properties** &gt; **All Properties**.

<table id="table_ytc_kkb_mv"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWA Routing Look-Back Time**com.glide.awa.routinglookback**

</td><td>

AWA defaults to routing work items created within the last 10 minutes. If a work item is created after 10 minutes has passed, it isn’t considered for AWA routing. For work items that are created outside of the default 10-minute window, create this system property to expand the AWA routing look-back time:-   **Name**: `com.glide.awa.routinglookback`
-   **Type**: **Integer**
-   **Value**: Number of seconds

For example, set the property **Value** to 86400 \(24 hours\) to cover a full shift for any missed work items.

-   **Description**: `Number of seconds AWA looks back for routing once the work items are eligible for AWA.`

**Note:** This property affects all service channels in the system.

</td></tr><tr><td>

Disable Query business rules**glide.awa.query\_br\_disable**

</td><td>

If the property is enabled, AWA disables before query business rules during its execution. For example, if enabled, an instance can have a custom before-query business rule on the interaction table without affecting how AWA routes or assigns interactions.-   **Type**: true \| false
-   Default value: true
-   Location: **System Properties** &gt; **All Properties**

</td></tr><tr><td>

Bypass AWA Queue Max Wait Time**glide.awa.bypass\_max\_wait\_time.enabled**

</td><td>

This property overrides the queue's max wait time value with the assignment rule's timeout value to help prevent work items from disappearing prematurely in an agent's inbox.

</td></tr><tr><td>

Enable/disable execution of subflows**glide.awa.enable\_routing\_subflow**

</td><td>

Enables/disables the execution of subflows defined on the AWA queues when work items are routed.-   **Type**: true \| false
-   Default value: false

</td></tr></tbody>
</table>For information on adding a system property, see Add a system property.

