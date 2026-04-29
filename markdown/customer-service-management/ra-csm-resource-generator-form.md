---
title: Resource generator inputs form
description: The form provides information about the generator type and generator inputs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a resource generator, Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Resource generator inputs form

The form provides information about the generator type and generator inputs.

## Resource Generators form fields

The Task Intelligence Admin Console \(com.sn\_ti\_admin\) plugin must be installed for selecting the Task Intelligence Classification resource generator type.

**Note:**

-   You can enter static values for the generator input fields. If the **Generator type** is Flow or Decision table, you can use the pill picker to select dynamic values. The context record is available for selection in the pill picker.
-   If a context input is defined for a context, it appears in the pill picker for selection. The context inputs are supported for Flow and Decision table generator types only.

<table id="table_urf_5cf_ztq"><thead><tr><th>

Generator type

</th><th>

Generator inputs

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Flow

</td><td>

Generator

</td><td>

The subflow for the resource generator.

</td></tr><tr><td>

Inputs for flow

</td><td>

Inputs for the selected subflow.

</td></tr><tr><td rowspan="2">

Decision table

</td><td>

Generator

</td><td>

The decision table for the resource generator.

</td></tr><tr><td>

Inputs for decision table

</td><td>

Inputs for the selected decision table.

</td></tr><tr><td rowspan="2">

Similarity

</td><td>

Similarity definitions

</td><td>

The similarity solution definition to find records that are relevant to the context record.

</td></tr><tr><td>

Top N Results

</td><td>

The number of records to return from the most relevant records found by the similarity solution definition.

</td></tr><tr><td>

Scripting

</td><td>

Script include

</td><td>

The script include record, which is an implementation of the ScriptingGeneratorFactory template.**Note:** To access the script includes, you must have the script\_include\_admin role.

</td></tr><tr><td rowspan="2">

AI search

</td><td>

Search field

</td><td>

The context field on which the AI search is performed.

</td></tr><tr><td>

Top N results

</td><td>

The number of records to return from the AI search.

</td></tr><tr><td rowspan="2">

Similarity with Trend

</td><td>

Similarity definitions

</td><td>

The similarity solution definition to find records that are relevant to the context record.

</td></tr><tr><td>

Trend definitions

</td><td>

The trend definition you want to associate with this solution definition.

</td></tr><tr><td rowspan="2">

Classification

</td><td>

Classification definition

</td><td>

The classification definition with a classification solution to return the predicted values or record references for a field on a table.

</td></tr><tr><td>

Top N Results

</td><td>

The number of values or records to return from the values or records predicted by the classification definition.

</td></tr><tr><td rowspan="2">

Task Intelligence Classification

</td><td>

Solution

</td><td>

The solution record that contains configuration for recommended input fields and recommended output fields for prediction. The solution also contains preferences whether the fields are auto-filled or recommendation messages are displayed.

</td></tr><tr><td>

Top N Results

</td><td>

The number of values or records to return from the relevant records predicted by the solution definition.

</td></tr></tbody>
</table>