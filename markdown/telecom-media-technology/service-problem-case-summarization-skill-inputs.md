---
title: Inputs for the service problem case summarization skill
description: The service problem case summarization skill includes the inputs that identify the table and fields that are used when a service problem case summary is generated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/service-problem-case-summarization-skill-inputs.html
release: brazil
topic_type: reference
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Skill inputs, Reference, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Inputs for the service problem case summarization skill

The service problem case summarization skill includes the inputs that identify the table and fields that are used when a service problem case summary is generated.

You can configure the input in the following service problem case summarization stages:

-   General details
-   View input
-   Customize prompt
-   Define availability
-   Select display
-   Review and activate

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
-   Diagnostic Task

Fields:

    -   Description
    -   Short description
    -   Work notes
    -   state
    -   sys id
-   Resolution Task

Fields:

    -   Description
    -   Short description
    -   Work notes
    -   state

</td></tr><tr><td>

Input templates

</td><td>

-   Verify
-   Diagnose
-   Repair
-   Test &amp; Resolve
-   Close

</td></tr></tbody>
</table>