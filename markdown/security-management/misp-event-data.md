---
title: MISP event data
description: You can review the MISP event data so that you can see detailed information about the MISP events.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MISP event data

You can review the MISP event data so that you can see detailed information about the MISP events.

## MISP event data in the list view

Access the list view from **MISP** &gt; **MISP Event Data**.

Use the list view to get a quick overview of the MISP event data.

<table id="table_bw5_bgk_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event ID

</td><td>

Event ID that is assigned by MISP when the event was first created or imported into the MISP server.

</td></tr><tr><td>

Info

</td><td>

Short description of the event.

</td></tr><tr><td>

Analysis

</td><td>

Current stage of the analysis for the event with the following possible options:-   Initial: The analysis is just beginning
-   Ongoing: The analysis is in progress
-   Completed: The analysis is complete

</td></tr><tr><td>

Threat Level

</td><td>

Risk level of the event. Incidents can be categorized into three different threat categories \(low, medium, high\). This field can be left as undefined. The following are the options:-   Low: General mass malware
-   Medium: Advanced Persistent Threats \(APT\)
-   High: Sophisticated APTs and 0-day attacks

</td></tr><tr><td>

MISP Tags

</td><td>

Tags that are associated with the MISP event.

</td></tr><tr><td>

MISP Galaxies

</td><td>

Galaxies that are associated with the MISP event.

</td></tr><tr><td>

Owner Org

</td><td>

Organization that owns the event on the MISP instance. This field is visible only to administrators.

</td></tr><tr><td>

Creator Org

</td><td>

Organization that created the event on the MISP instance.

</td></tr><tr><td>

Distribution

</td><td>

Distribution of the individual attribute. An attribute can have a different distribution level than the event.

</td></tr><tr><td>

MISP Event Hyperlink

</td><td>

Link to the MISP event that is stored on the MISP server.

</td></tr><tr><td>

MISP Source

</td><td>

MISP source where the event is created.

</td></tr></tbody>
</table>## MISP event data in the form view

Use the form view to get detailed information about the MISP events.

<table id="table_ffz_j3k_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event ID

</td><td>

Event ID that is assigned by MISP when the event was first created or imported into the MISP server.

</td></tr><tr><td>

UUID

</td><td>

ID that uniquely identifies events and attributes.

</td></tr><tr><td>

Creator Org

</td><td>

Organization that created the event on the MISP instance.

</td></tr><tr><td>

Owner Org

</td><td>

Organization that owns the event on the MISP instance. This field is visible only to administrators.

</td></tr><tr><td>

Creator User

</td><td>

User who created the event in MISP.

</td></tr><tr><td>

Last Change

</td><td>

Date that the event was last modified.

</td></tr><tr><td>

MISP Source

</td><td>

MISP source where the event is created.

</td></tr><tr><td>

Created date \(in MISP\)

</td><td>

Date that the event was created or first imported in the MISP server.

</td></tr><tr><td>

Threat Level

</td><td>

Risk level of the event. Incidents can be categorized into three different threat categories \(low, medium, high\). This field can be left as undefined. The following are the options:-   Low: General mass malware
-   Medium: Advanced Persistent Threats \(APT\)
-   High: Sophisticated APTs and 0-day attacks

</td></tr><tr><td>

Analysis

</td><td>

Current stage of the analysis for the event with the following possible options:-   Initial: The analysis is just beginning
-   Ongoing: The analysis is in progress
-   Completed: The analysis is complete

</td></tr><tr><td>

Distribution

</td><td>

Distribution of the individual attribute. An attribute can have a different distribution level than the event.

</td></tr><tr><td>

Published

</td><td>

Status of whether the event has been published or not. Publishing allows the attributes of the event to be used for all eligible exports and notifies users that have subscribed to the event alerts.

</td></tr><tr><td>

MISP Event Hyperlink

</td><td>

Link to the MISP event that is stored on the MISP server.

</td></tr><tr><td>

Info

</td><td>

Short description of the event.

</td></tr><tr><td>

Tags \(Local\)

</td><td>

Tags that are available on the host organization's MISP instance to enable tagging for synchronization and export filtering. MISP events are not modified when you use local tags. Local tags are always stripped before being synchronized with other MISP instances and sharing communities.

</td></tr><tr><td>

Tags \(Global\)

</td><td>

Tags that are available globally to be shared and synchronized with other MISP instances and sharing communities. When you add global tags to MISP instances, you can modify events.

</td></tr><tr><td>

Galaxies \(Local\)

</td><td>

Galaxies that are available on the host organization's MISP instance for synchronization and export filtering. MISP events are not modified when you use local galaxies. These local galaxies are always stripped before being synchronized with other MISP instances and sharing communities.

</td></tr><tr><td>

Galaxies \(Global\)

</td><td>

Galaxies that are available globally to be shared and synchronized with other MISP instances and sharing communities. When you add global galaxies, MISP you can modify events.

</td></tr></tbody>
</table>