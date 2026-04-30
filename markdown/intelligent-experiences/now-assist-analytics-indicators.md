---
title: Now Assist Analytics indicators
description: Indicators for Now Assist Analytics include information about generative AI log metadata, deflection events, deflection event activities, deflection rate, and more.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-20"
reading_time_minutes: 1
keywords: [Now Assist Analytics, indicators, Platform Analytics Administration, GenAI, Generative AI]
breadcrumb: [Now Assist Analytics reference, Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Now Assist Analytics indicators

Indicators for Now Assist Analytics include information about generative AI log metadata, deflection events, deflection event activities, deflection rate, and more.

To access these indicators, navigate to **Platform Analytics Administration** &gt; **Indicators**. You must have Now Assist Analytics Admin \[sn\_na\_analytics\_admin\] role to access the indicators.

These indicators measure data on daily intervals. Data is only available for dates before the current date. If you want to see results from the current day, you must wait until the next day.

**Note:** The Generative AI Usage log \[sys\_gen\_ai\_usage\_log\] table is maint-only.

## Now Assist Analytics indicators

Now Assist Analytics indicators on your instance provide details about deflection events and activities, deflection rate, skill acceptance rate, and so on. The following table lists the indicators that are included in Now Assist Analytics, along with breakdowns and indicator sources.

<table id="table_ygl_rmk_bdc"><thead><tr><th>

Indicator

</th><th>

Indicator type

</th><th>

Breakdowns available

</th><th>

Indicator source table

</th><th>

Application

</th></tr></thead><tbody><tr><td>

Daily GenAI Deflection Events

</td><td>

Automated

</td><td>

-   By Deflection Source
-   By Deflection Event Outcome
-   By Deflection Event Outcome Type
-   By Query Resolution Status
-   By Deflection Log Source

</td><td>

Now Assist Analytics Deflection Event \[sn\_na\_def\_event\]

</td><td>

Now Assist Analytics

</td></tr><tr><td>

Daily GenAI Deflection Event Activities

</td><td>

Automated

</td><td>

-   By Deflection Event Activity Feedback
-   By Deflection Event Activity Type
-   By Deflection Event Activity Direction
-   By Deflection Source
-   By Deflection Log Source

</td><td>

Now Assist Analytics Deflection Event Activity \[sn\_na\_def\_event\_activity\]

</td><td>

Now Assist Analytics

</td></tr><tr><td>

Daily GenAI Log Metadata

</td><td>

Automated

</td><td>

-   By Feedback
-   By response accepted without edits
-   By Skills Config
-   By Skill Family

</td><td>

Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\]

</td><td>

Now Assist Analytics

</td></tr><tr><td>

GenAI Actions per day

</td><td>

Automated

</td><td>

-   By Skills Config
-   By GenAI Feature
-   By Skill Family
-   By Generative AI Skill Execution Modality

</td><td>

Generative AI Usage log \[sys\_gen\_ai\_usage\_log\]

</td><td>

Now Assist Admin console

</td></tr><tr><td>

Number of users who used GenAI actions per day

</td><td>

Automated

</td><td>

-   By Skills Config
-   By GenAI Feature
-   By Skill Family
-   By Generative AI Skill Execution Modality

</td><td>

Generative AI Usage log \[sys\_gen\_ai\_usage\_log\]

</td><td>

Now Assist Admin console

</td></tr><tr><td>

Acceptance rate

</td><td>

Formula

</td><td>

By Skills Config

</td><td>

Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\]

</td><td>

Now Assist Analytics

</td></tr><tr><td>

Acceptance rate without edits

</td><td>

Formula

</td><td>

By Skills Config

</td><td>

Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\]

</td><td>

Now Assist Analytics

</td></tr><tr><td>

Deflection Rate \(Self-Solved Performance\)

</td><td>

Formula

</td><td>

By Deflection Source

</td><td>

Now Assist Analytics Deflection Event \[sn\_na\_def\_event\]

</td><td>

Now Assist Analytics

</td></tr></tbody>
</table>**Parent Topic:**[Now Assist Analytics reference](now-assist-analytics-reference.md)

