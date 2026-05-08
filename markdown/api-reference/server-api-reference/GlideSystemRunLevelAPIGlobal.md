---
title: GlideSystemRunLevel - Global
description: The GlideSystemRunLevel API provides methods to get and set the current system run level.Retrieves the current system run level.Switches the system run level.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSystemRunLevel- Global

The GlideSystemRunLevel API provides methods to get and set the current system run level.

Setting the system run level allows applications to change or limit their features based on operational toggles. For more information about using operational toggles, see Operational toggles.

The system run level can be set to one of the defined system run levels.

-   Fully Operational
-   Slightly Degraded
-   Moderately Degraded
-   Severely Degraded

The system run level set on one node is synchronized to all nodes in the instance.

The admin role is required to use this API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSystemRunLevel – getCurrentLevel\(\)

Retrieves the current system run level.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xvs_t35_qpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The current system run level.Possible values:

-   fully\_operational
-   slightly\_degraded
-   moderately\_degraded
-   severely\_degraded

</td></tr></tbody>
</table>Gets the current system run level.

```
var currentRunLevel = sn_run_level.GlideSystemRunLevel.getCurrentLevel();
gs.info(currentRunLevel);
```

Output:

```
fully_operational
```

## GlideSystemRunLevel – switchLevel\(String newLevel\)

Switches the system run level.

|Name|Type|Description|
|----|----|-----------|
|newLevel|String|The ID value of the new system run level. This value is from the **ID** field in the System Run Level \[sys\_run\_level\] table.|

<table id="table_xvs_t35_qpb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

ID of the previous system run level.Possible values:

-   fully\_operational
-   slightly\_degraded
-   moderately\_degraded
-   severely\_degraded

</td></tr></tbody>
</table>Sets the system run level to Slightly Degraded.

```
sn_run_level.GlideSystemRunLevel.switchLevel('slightly_degraded');
```

Output:

```
SystemRunLevel requested to change from: fully_operational to: slightly_degraded
```

