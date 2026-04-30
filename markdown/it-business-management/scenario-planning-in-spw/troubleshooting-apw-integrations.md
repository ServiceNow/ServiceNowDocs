---
title: Managing Strategic Planning with Project Portfolio Management, Agile Development 2.0, and SAFe
description: Ensure that Strategic Planning is integrated properly with PPM, Agile Development 2.0, and SAFe with these guidelines.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Managing Strategic Planning with Project Portfolio Management, Agile Development 2.0, and SAFe

Ensure that Strategic Planning is integrated properly with PPM, Agile Development 2.0, and SAFe with these guidelines.

-   Do not change the filter condition of a table map after the records are interfaced. The already interfaced records might not match with the new filter condition and any change in the filter condition can result in data inconsistency. If you need to change the filter condition, ensure that the relevant attributes on the interfaced records are updated manually to avoid data inconsistency issues.
-   Whenever a table map is created, ensure that the relevant field maps and choice maps are also configured.
-   When an import job for a table map is running \(processing\), do not modify the table map or its field maps.
-   Using the **Converted to** field on the planning item form, you can identify the original record from which it was converted.
-   Ensure that the **Lookup field** and **Lookup column** values are added whenever the execution and alignment tables are referencing two different tables, while creating a field map for field type of reference or glide list.
-   If there is a data synchronization failure, check if:
    -   The **Integration error logs** related list within that Alignment integration record.
    -   The **Alignment table filter** \(for import\) and **Execution table filter** \(for export\) conditions are met.
    -   The **Active** flag in both the alignment integration and the table map is checked.
    -   The appropriate fields and choices are configured for each table map.
-   If you want to view the **Execution URL** field, configure the alignment planning item record to view it.
-   If the Execution URL field in your synced planning item\(s\) is blank, navigate to **All** &gt; **Strategic Planning** &gt; **Integrations** and select the required alignment integration. If any of the execution URL is missing, select the **Fix execution URL\(s\) for planning items** related link. This runs a job and updates the execution URL field.

    **Note:** The **Fix execution URL\(s\) for planning items** related link is only available when the execution URL is missing for any of the planning item.

-   A **Primary goal** field is introduced to the projects, demands, and epics table maps to support the integration of the **Goal** field between alignment and execution tables.
-   When you are trying to import or export a project, ensure that the demands \(that are a part of that project\) are synced.
-   You can create a table map for any execution table. If a table map is not created from one of the delivered tables \(pm\_portfolio, rm\_epic, dmn\_demand, pm\_project\) or does not extend from them, you are required to create a business rule to support the interfacing of the table map records. For more information on creating a business rule, see [Create a business rule to apply a custom table map configuration](../../apw-internal-integrations/task/create-a-bussiness-rule.md).

**Parent Topic:**[Strategic Planning Workspace reference](../../alignment-planner-workspace/reference/alignment-planner-workspace-reference.md)

