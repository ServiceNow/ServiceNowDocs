---
title: Configure definition properties
description: You can configure additional capabilities and configuration options for the definition ruleset.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine properties, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure definition properties

You can configure additional capabilities and configuration options for the definition ruleset.

<table id="table_up4_2sx_2hc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Definition Synchronization

</td><td>

Allows you to push new definitions and definition updates to production. After that, changes flow from the production instance to any test instances listed in the **My SN Instances** related list.

</td></tr><tr><td>

Enable Instance Specific Definitions

</td><td>

When enabled, an additional field will appear on all definition records, **SN Instances to Run On**. This will allow you to specify definitions to:

 -   Run on production instance\(s\) only
-   Run on all sub-production instances
-   Run on specified instances

If you select this option, an additional field allows you to determine specific instances for this definition to run on.

Only instances defined in the **My SN Instances** related list can be selected.


 Definitions will only run on the instances they are configured for. Otherwise, all definitions will run \(as long as the definition is marked “active”\).

 **Important:** If this is enabled and the **My SN Instances** related list does not contain the current instance, no scans will run for it.

</td></tr><tr><td>

Override Instance-Specific Definitions For Definition Scanning

</td><td>

-   Overrides instance-specific Scan Engine definitions when scanning for findings against a specific definition using **Scan instance for this finding**.
-   Helpful for testing a single production-only definition in a lower environment or running a single sub-production definition against production.

 **Note:** This property only applies if you enable instance-specific Scan Engine definitions.

</td></tr><tr><td>

Override Instance-Specific Definitions For Update Set Scans

</td><td>

-   Overrides instance-specific Scan Engine definitions when scanning update sets.
-   Helpful when promoting an update set. Retrieved update sets can be scanned against all active definitions, even if the definition doesn’t apply to the instance.

 **Note:** This property only applies if you enable instance-specific Scan Engine definitions.

</td></tr></tbody>
</table>