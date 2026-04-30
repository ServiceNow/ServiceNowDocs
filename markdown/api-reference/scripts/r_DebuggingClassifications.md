---
title: Debugging classifications
description: You must add a system property to enable classification debugging.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Debugging classifications

You must add a system property to enable classification debugging.

## Debugging classifications

The resulting log entries list the name of each classifier that runs, along with all the names and values that are available to the criteria in the classifier. To log debugging information about classifications, add the following system property.

<table id="table_fj2_sjk_s4"><thead><tr><th>

System Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.discovery.debug.ci\_identification**

</td><td>

Enables debugging information for process classification.-   Type: true \| false
-   Default Value: false
-   Location: Add to the System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Parent Topic:**[Debugging scripts](../concept/script-debug-overview.md)

