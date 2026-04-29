---
title: Discovery probe management
description: Several discovery probes and their associated sensors are included with Discovery. You rarely need to modify probes or sensors. But you might need to set parameters to control the behavior of a particular probe or align versions of customized probes.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery probe management

Several discovery probes and their associated sensors are included with Discovery. You rarely need to modify probes or sensors. But you might need to set parameters to control the behavior of a particular probe or align versions of customized probes.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## What you can do

These are the things you can do with probes and sensors:

-   **Review the base system probes**

    Review the [List of Discovery probes](r_ListOfDiscoveryProbes.md) to see the probes that exist in the base system. Probes need to be active on classifiers for Discovery to trigger the probes. However, not all probes are active on classifiers as more patterns replace probes and sensors. To see a list of patterns, see [Available discovery patterns](../../service-mapping/concept/available-patterns.md).

-   **Create or modify a probe**

    You can [create a new probe](../task/modify-a-probe.md) to discover additional CIs that Discovery does not find with the base system probes or patterns, or modify an existing probe to collect additional information on the type of CI. After you create or modify a probe, test it. You can also create multiprobes and multisensors. See [Create a Discovery multiprobe](r_MultiprobesIncludedWithDiscovery.md#) for more information.

-   **Upgrade to the latest version of a probe or sensor**

    If you upgrade your instance, the Discovery application is also updated, along with components like probes and sensors. However, if you customized any probes or sensors, they do not upgrade. You need to copy your customizations to a text file, upgrade the probes and sensors, and reapply your customizations. See [Align versions of customized probes and sensors](../task/t_AlignVerCustProbeSens.md) for more information.

-   **Set probe parameters**

    Probe parameters control several aspects about how probes function. With each probe provided in the base system, certain parameters are allowed. These are specified in the [list of Discovery probes](r_ListOfDiscoveryProbes.md). See [Set probe parameters](../task/t_SetProbeParameters.md) for instructions on how to set a parameter.

-   **Review probe permissions**

    Certain probes need permissions to run on the target machines or CIs that you are trying to discover. See [Discovery probe permissions](r_AdditionalPermissions.md) for more information.


-   **[Create or modify a probe](../task/modify-a-probe.md)**  
Create a new probe to discover additional CIs or modify an existing probe to collect additional information. After you create or modify a probe, test it.
-   **[Discovery probe permissions](r_AdditionalPermissions.md)**  
Several probes require additional permissions to run.
-   **[Set probe parameters](../task/t_SetProbeParameters.md)**  
Use probe parameters to control the behavior of a particular probe every time it is triggered.

**Parent Topic:**[Discovery probes and sensors](../concept/c_DiscoveryProbesAndSensors.md)

