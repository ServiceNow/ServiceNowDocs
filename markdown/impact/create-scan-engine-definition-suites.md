---
title: Customize Scan Engine definition suites
description: Follow these steps to create or modify Scan Engine definition suites.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/create-scan-engine-definition-suites.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize Scan Engine definitions, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Customize Scan Engine definition suites

Follow these steps to create or modify Scan Engine definition suites.

## Before you begin

Role required: Scan Engine admin \(`sn_se.scan_engine_admin_role` role\)

## Procedure

1.  Create Definition Suites
2.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definition Suites.**.

3.  Select **New**.

4.  Fill in the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Number|Unique identifier of the definition suite. This number is generated automatically.|
    |Active|Makes the definition suite active and useable.|
    |Short Description|Brief description of the definition suite.|
    |Description|Detailed description of why the suite was created.|

5.  Modify Scan Engine Definition Suites

    **Note:** Role required: Scan Engine admin \(`sn_se.scan_engine_admin`\).

    While only Scan Engine admins can modify definitions, any user with the Scan Engine user role can view them.

6.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definition Suites**.

7.  Select a suite number to open its details and modify its properties.

    Related lists appear at the bottom of the screen.

<table id="table_elk_g4x_2hc"><thead><tr><th>

List

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Scan Engine Definitions

</td><td>

Displays the definitions attached to this suite. To add a definition to the suite:1.  Select **Edit**.
2.  Use the filter to sort the **Collection** list.
3.  To add a definition to the collection, select it, and then select the right arrow to move it to the Workflow Engine field.

You can add multiple definitions.

You can move definitions out of the suite using the left arrow.

4.  Select **Save**.


</td></tr><tr><td>

Relevant Findings

</td><td>

Displays findings found during on-demand or instance scans as defined by the definitions in the suite.

</td></tr></tbody>
</table>
**Parent Topic:**[Customize Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/view-modify-scan-engine-properties.md)

