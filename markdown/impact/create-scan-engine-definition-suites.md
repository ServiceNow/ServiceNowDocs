---
title: Create Scan Engine definition suites
description: Follow these steps to create Scan Engine definition suites.You can modify a definition suite to further customize and refine its scanning criteria.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# Create Scan Engine definition suites

Follow these steps to create Scan Engine definition suites.

## Before you begin

Role required: Scan Engine admin \(`sn_se.scan_engine_admin_role` role\)

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definition Suites.**.

2.  Select **New**.

3.  Fill in the fields as needed.

<table id="choicetable_o2k_3nx_2hc"><tbody><tr><td id="d28902e97">

**Number**

</td><td>

The unique identifier of the definition suite. This number is generated automatically.

</td></tr><tr><td id="d28902e106">

**Active**

</td><td>

Makes the definition suite active and useable.

</td></tr><tr><td id="d28902e115">

**Short Description**

</td><td>

Brief description of the definition suite.

</td></tr><tr><td id="d28902e124">

**Description**

</td><td>

Detailed description of why the suite was created

</td></tr></tbody>
</table>
## View and modify Scan Engine definition suites

You can modify a definition suite to further customize and refine its scanning criteria.

### Before you begin

Role required: Scan Engine admin \(`sn_se.scan_engine_admin`\).

While only Scan Engine admins can modify definitions, any user with the Scan Engine user role can view them.

### Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definition Suites**.

2.  Select a suite number to open its details and modify its properties.

    You can edit the same fields you configured in [Create Scan Engine definition suites](create-scan-engine-definition-suites.md#).

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
