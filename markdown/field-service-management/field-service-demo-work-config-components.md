---
title: Field Service Demo Work Configuration components
description: Several type of components like tables, script includes, and business rules are installed for Field Service Demo Work Configuration.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service Demo Work Configuration components

Several type of components like tables, script includes, and business rules are installed for Field Service Demo Work Configuration.

Install the Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin for a Field Service Work Configurations demo workflow. For more information see [Configuring Field Service Work Configurations](../concept/configuring-work-configs.md).

## Tables

Field Service Demo Work Configuration for MRI Scanner breakfix workflow adds the following table.

<table id="table_byc_cx3_qfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Order MRI Scanner Break fix task \[wm\_mri\_scanner\_break\_fix\_task\]

</td><td>

Stores the details about the example workflow for Work Configurations. This table is added when Field Service Demo Work Configuration for Break fix is installed.

</td></tr></tbody>
</table>## SM Configuration

Field Service Demo Work Configuration for MRI Scanner breakfix workflow adds the following SM Configuration.

|SM Configuration|Description|
|----------------|-----------|
|MRI Scanner Break fix|Field Service Configuration example workflow for MRI Scanner breakfix.|

## Script includes

Field Service Demo Work Configuration for MRI Scanner breakfix workflow adds the following script includes.

<table id="table_zvc_5qn_qfc"><thead><tr><th>

Script includes

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MRIScannerBreakFixUtil

</td><td>

Utility functions for handling MRI Scanner breakfix workflows. **Note:** This script include is available only if Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin is installed.

</td></tr><tr><td>

MRIScannerDAO

</td><td>

DAO file that contains queries to handle database operations for MRI Scanner breakfix use-cases.**Note:** This script include is available only if Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin is installed.

</td></tr></tbody>
</table>## Field Service Questionnaire

Field Service Demo Work Configuration for MRI Scanner breakfix workflow adds the following questionnaire.

<table id="table_wgd_f44_qfc"><thead><tr><th>

Field Service Questionnaire

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MRI Scanner Break fix - Questionnaire

</td><td>

Field Service questionnaire for MRI Scanner breakfix demo workflow for Work Configurations.**Note:** The questionnaire is available only if Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin is installed.

</td></tr></tbody>
</table>## Work order summary template

Field Service Demo Work Configuration for MRI Scanner breakfix workflow adds the following work order summary template.

<table id="table_mfn_wt4_qfc"><thead><tr><th>

Work order summary template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Break fix - Field Service Work Order Summary

</td><td>

Work order summary template for MRI Scanner breakfix example workflow for Work Configurations.**Note:** The questionnaire is available only if Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin is installed.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

