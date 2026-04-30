---
title: Skill inputs for Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Use inputs for each skill to configure how and when a skill is used.
locale: en-US
release: xanadu
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist for Telecommunications, Media and Technology \(TMT\), Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Skill inputs for Now Assist for Telecommunications, Media and Technology \(TMT\)

Use inputs for each skill to configure how and when a skill is used.

## Overview of service problem case

Depending on the selected skill, you can configure inputs. These settings determine how a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a service problem case summary, resolution notes summary, and test summary.

## Service problem case summarization skill

The service problem case summarization skill includes the inputs that identify the table and fields that are used when a service problem case summary is generated.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

<table id="table_bsy_bdp_5bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Service Problem Case \[sn\_sprb\_mgmt\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Resolution notes generation skill

The resolution notes generation skill includes the inputs that identify the table and fields that are used when the resolution notes are generated for a service problem case.

In this release, you can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on.

<table id="table_yng_4jp_5bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Service Problem Case \[sn\_sprb\_mgmt\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments

</td></tr></tbody>
</table>## Test summarization skill

For the test summarization skill includes the inputs that identify the table and fields that are used when a test summary is generated.

The following table lists the inputs that you can configure for the test summarization skill of the Service Problem Case feature.

|Input|Description|
|-----|-----------|
|Input table|Test Run \[sn\_st\_mgmt\_test\]|
|Input field|Name|

<table id="table_g5c_ntm_1cc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Test Measure \[sn\_st\_mgmt\_test\_measure\]

</td></tr><tr><td>

Input field

</td><td>

-   Metric name
-   Metric description
-   Value
-   Rule violation

</td></tr></tbody>
</table>