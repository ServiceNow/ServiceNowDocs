---
title: Properties installed with Developer Sandboxes
description: The system properties available in Developer Sandboxes govern application behavior, enabling developers to configure and optimize their testing environments effectively.
locale: en-US
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Installing, Developer Sandboxes, Developing your application, Building applications]
---

# Properties installed with Developer Sandboxes

The system properties available in Developer Sandboxes govern application behavior, enabling developers to configure and optimize their testing environments effectively.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

These properties are available for Developer Sandboxes.

<table id="table_ek4_ct3_xhc"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

glide.dev\_sandbox.num.controller

</td><td>

Number of nodes that run as a controller.-   Type: number
-   Default value: 2

</td><td>

-   Can't be 0.
-   Increasing converts unassigned nodes to controller nodes.
-   Decreasing converts unassigned nodes to nodes.
-   More controller nodes mean you get fewer sandboxes.

</td></tr><tr><td>

glide.dev\_sandbox.node.healthy\_time\_min

</td><td>

Time in minutes that a node is considered healthy. An unhealthy node that's assigned to a sandbox can be remediated by assigning it to another sandbox. Remediation is the process of detecting a sandbox that should be running on a node but isn't, and then assigning another node to run on the sandbox.

-   Type: number
-   Default value: 10

</td><td>

-   Increasing this value keeps a sandbox node up longer, so remediation happens less frequently.
-   Decreasing it takes a node down faster, so remediation occurs more frequently.
-   Do not set this value lower than the time it takes a node to restart, roughly 3 minutes. During a restart, the node is still considered healthy to prevent the remediator from reassigning sandboxes to another node.

</td></tr><tr><td>

glide.dev\_sandbox.node.poll\_interval\_seconds

</td><td>

Number of seconds between status checks for a node expected to go offline in the sys\_cluster\_state table, which contains the nodes that are assigned to an instance.-   Type: number
-   Default value: 10

</td><td>

-   Generally doesn't need to be changed.
-   Used during sandbox retirement to determine how often a node is checked for being set to offline.
-   Increasing means the polling happens more often.
-   Decreasing means that the polling happens less often.

</td></tr><tr><td>

glide.dev\_sandbox.node.poll\_timeout\_min

</td><td>

Number of minutes to wait for a node to shutdown, and have a **Status** of Offline in sys\_cluster\_state table.-   Type: number
-   Default value: 2

</td><td>

-   Generally doesn't need to be changed.
-   Used during sandbox retirement to determine how long to check for a sandbox node to be set to offline.
-   Increasing means the polling happens longer.
-   Decreasing means that the polling completes faster.

</td></tr><tr><td>

glide.dev\_sandbox.default\_table\_config

</td><td>

Default table config in Developer Sandboxes.-   Type: string
-   Default value: shared\_table
-   Other possible values:
    -   shared\_table
    -   full\_copy
    -   zero\_copy

</td><td>

-   The full\_copy value isolates tables but uses much more database space and can make sandbox creation slower, especially with large datasets.
-   The zero\_copy value also isolates tables with less initial disk space, but starts empty and may consume more space as data is added.

</td></tr><tr><td>

glide.dev\_sandbox.dsb\_db\_copier\_threads

</td><td>

Number of concurrent table creations in a sandbox.-   Type: number
-   Default value: 1
-   Other possible values: 1-5

</td><td>

-   Increasing threads can create more contention and load when creating sandboxes.
-   **Warning:** Do not change this value without consulting your account manager.


</td></tr><tr><td>

glide.db.dsb.data\_copy\_processor.threads 

</td><td>

Number of data copy plans to run concurrently during sandbox creation.-   Type: number
-   Default value: 1
-   Other possible values: 1-5

</td><td>

-   This value is multiplied by the glide.dev\_sandbox.dsb\_db\_copier\_threads value.
-   Increasing threads can create more contention and load when creating sandboxes.
-   **Warning:** Do not change this value without consulting your account manager.


</td></tr><tr><td>

glide.db.dsb.data\_copy\_processor.chunk\_copy.threads

</td><td>

Number of data copiers running at a time for each table.-   Type: number
-   Default value: 5
-   Other possible values: 1-5

</td><td>

-   This value is multiplied by the glide.dev\_sandbox.dsb\_db\_copier\_threads and glide.db.dsb.data\_copy\_processor.threads values.
-   Decreasing this value slows down sandbox creation.

</td></tr><tr><td>

glide.dev\_sandbox.cleanup\_retries

</td><td>

Number of retries the Developer Sandboxes destroy code attempts to do clean up any leftover Developer Sandboxes tables.-   Type: number
-   Default value: 3

</td><td>

 

</td></tr><tr><td>

glide.dev\_sandbox.backup\_tables

</td><td>

Tables that will be preserved for recreating developer sandboxes post clone.-   Type: string
-   Default value: sys\_repo\_config

</td><td>

Comma-delimited list of tables to preserve. If a table has is referenced here, its content in each sandbox is saved and preserved during clones, then restored post-clone in the re-created sandbox\(es\).

 This property is effective only when Developer Sandboxes are enabled via the glide.dev\_sandbox.enabled property, and impacts only sandboxes.

</td></tr><tr><td>

glide.dev\_sandbox.export.poll\_interval\_seconds

</td><td>

Frequency in seconds that the controller node checks if a sandbox has completed exporting its altered update sets.This property is used only when exporting sandbox update sets before an instance upgrade begins.

-   Type: number
-   Default value: 10

</td><td>

Decreasing the value may help the upgrade go faster but at the cost of extra checks.

</td></tr><tr><td>

glide.dev\_sandbox.export.poll\_timeout\_min

</td><td>

How long the controller node waits for a sandbox to export its altered update sets before an instance upgrade.If the timeout limit is hit, the upgrade continues regardless of export state.

-   Type: number
-   Default value: 10

</td><td>

-   Decreasing the value may result in unexported updates.
-   Increasing the value helps to ensure that changes are exported, but can delay the upgrade.

</td></tr><tr><td>

glide.dev\_sandbox.node.healthy\_time\_min

</td><td>

Time window in which a node must report to sys\_cluster\_state to be considered healthy and included in sandbox capacity calculations.-   Type: number
-   Default value: 10

</td><td>

 

</td></tr><tr><td>

glide.dev\_sandbox.lifecycle.max\_concurrent\_events

</td><td>

Maximum limit of concurrent sandbox allocations/retirements events.-   Type: number
-   Default value: 5

</td><td>

Increasing the value enables more concurrent allocations/retirement, but could overload the database.

</td></tr></tbody>
</table>