---
title: System components installed with Nokia Altiplano
description: System properties control how the connector operates, including discovery options and performance settings.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# System components installed with Nokia Altiplano

System properties control how the connector operates, including discovery options and performance settings.

<table id="table_ghf_tcy_vfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_sgc\_altiplano.enable\_onu\_discovery**

</td><td>

Enable or disable discovery of ONU devices and logical connections between OLT and ONU. -   Default value: True
-   Location: **All**&gt;**Service Graph Connectors**&gt;**Nokia Altiplano**&gt;**Properties** or **System Properties** \[sys\_properties\] table filtering by the name ‘\*altiplano’

</td></tr><tr><td>

**sn\_sgc\_altiplano.devices\_list\_batch\_size**

</td><td>

Controls the batch size for Altiplano REST API calls.-   Default value: 1000
-   Location: **All**&gt;**Service Graph Connectors**&gt;**Nokia Altiplano**&gt;**Properties** or **System Properties** \[sys\_properties\] table filtering by the name ‘\*altiplano’

</td></tr><tr><td>

**sn\_sgc\_altiplano.parallel\_number\_of\_data\_source\_jobs**

</td><td>

Number of parallel jobs for collecting Altiplano data \(requires "Enable parallel loading" setting\).-   Default value: 2
-   Location: **All**&gt;**Service Graph Connectors**&gt;**Nokia Altiplano**&gt;**Properties** or **System Properties** \[sys\_properties\] table filtering by the name ‘\*altiplano’

</td></tr><tr><td>

**sn\_sgc\_altiplano.onu\_ci\_class**

</td><td>

Defines whether ONUs are stored as `ONU` or `ONT` CI class. -   Default value: ONU
-   Location: **All**&gt;**Service Graph Connectors**&gt;**Nokia Altiplano**&gt;**Properties** or **System Properties** \[sys\_properties\] table filtering by the name ‘\*altiplano’

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Service Operations Management reference](components-installed-with-tsom.md)

**Related topics**  


[Telecom Discovery via Nokia Altiplano](../concept/service-graph-connector-for-nokia-altiplano.md#)

[Configure Nokia Altiplano service graph connector](../concept/configuring-service-graph-connector-nokia-altiplano.md)

