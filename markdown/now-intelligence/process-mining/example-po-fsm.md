---
title: Content pack for Field Service Management \(FSM\)
description: Analyze a process for work order tasks and identify bottlenecks to minimize delays in the workflow for a better customer experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/example-po-fsm.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Automatic content pack delivery, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for Field Service Management \(FSM\)

Analyze a process for work order tasks and identify bottlenecks to minimize delays in the workflow for a better customer experience.

This content pack loads automatically when Field Service Management is installed on your instance and the relevant tables are present. For more information, see [Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md).

## Templates shipped with content pack

|Content pack|Template name|Table|
|------------|-------------|-----|
|Field Service Management|Standard template for Work Orders|wm\_order|
|Standard template for Work Order Tasks|wm\_task|

## What you get with this content pack

This content pack analyzes your work order and work order task processes. It gives you visibility into common process issues, such as:

-   Work orders and tasks that take longer than expected to complete
-   Rework, such as tasks that get sent back between teams
-   Deviations from the expected process flow
-   Work that stalls with a particular team longer than expected

## Example

In this example, you're a process analyst in the ACME corporation where you must submit an analysis on current processes associated with work order tasks. You use Analyst workbench to access the mined processes for the **Standard template for Work Order Tasks** project definition.

You would analyze the work order process flow and suggest ways to improve the processes by using the following workflow:

1.  Select **Analyst workbench**.
2.  View standalone analysis of all the records in the process map by setting the **Breakdowns** list to **Assignment group**, and select **Apply**.
3.  Refine the process map by selecting **Refine** and selecting a connection width to see the full list of metrics.

    You observe and analyze that the reason for the delay in scheduling the tasks.

4.  Filter the data to view the records by selecting **Show records** &gt; **View**.

    You observe that most of the tasks are related to installation.

5.  Add notes to the project by selecting the notes icon \(\[Omitted image "notes-icon.png"\] Alt text: notes icon\) and submit an analysis.

    In your notes, you suggest review the reason for higher dispatch time in the installation tasks.


\[Omitted image "example-po-fsm1.png"\] Alt text: Example: Process Mining Analyst workbench for FSM

**Parent Topic:**[Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md)

**Related topics**  


[Process Mining for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/process-opt-fsm.md)

