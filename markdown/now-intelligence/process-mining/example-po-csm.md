---
title: Example of Process Mining for CSM
description: Analyze a process for customer service cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Content pack for Customer Service Management, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Example of Process Mining for CSM

Analyze a process for customer service cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.

Say you are a process analyst in the ACME corporation where you must submit analysis on current processes associated with customer service cases. You use the Analyst Workbench to access the mined processes for the **Customer Service Cases** project.

You would analyze the case process flow and suggest ways to improve the processes by using the following workflow:

1.  Select **View in Workspace** from the **Customer Service Cases** project definition. The Analyst Workbench is opened in a new tab.

    You observe that the customer service case records take an average duration of 16 days to close a case.

2.  View metrics of the process map by setting the Primary Metric and Secondary Metric lists to **Unique Occurrences** and **Average Duration**, respectively.
3.  Refine the process map by selecting **Refine** and selecting a connection width to see the full list of metrics.

    You observe that the **Work In Progress - Awaiting Info** transition state is taking more than two days.

4.  In the **Filters** tab, set the Breakdown filters list to **Assignment group** and use the activity filter to view the process flow between the **Work In Progress - Awaiting Info** and **Work In Progress** activities.
5.  In the **Routes** tab, you want to see all the records that took longer than average duration of two days between the selected activities so you select **Most records** in the Sort by list. You then select any process paths to view the cases in that route.

    You observe that most of the cases are related to emails.

6.  Add notes to the project by selecting the notes icon \(![](../image/notes-icon.png)\) and submit an analysis.

    In your notes, you suggest using a standardized template for improving the email transactions between agents and customers.


![Example: Process Mining Analyst Workbench for CSM](../image/example-po-csm2.png "Process Mining for customer service cases")

**Parent Topic:**[Content pack for Customer Service Management](csm-integration-po.md)

**Related topics**  


[Analyzing and getting process insights](analyze-get-process-insights.md)

[Content pack for Customer Service Management](csm-integration-po.md)

