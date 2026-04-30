---
title: Review and interpret automated root cause analysis
description: Review the analysis report and understand the root cause of performance issues. Use this information to optimize your processes.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automated root cause analysis, Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Review and interpret automated root cause analysis

Review the analysis report and understand the root cause of performance issues. Use this information to optimize your processes.

**Note:** You must have run automated root cause analysis to review and interpret the results. For more information, see [Run automated root cause analysis reports](../task/run-view-arca.md).

You must read and understand the automated root cause analysis results as follows.

![Automated root cause analysis result](../image/rca-annotated.png)

In the above example, the root cause analysis is run on the finding definition of type Rework. We are looking at records for which rework was done after the record was in Closed state. It shows why the records do not go to Process End after the Closed state.

As per this analysis, 13 of the incidents that were initially assigned to PO Group 8 had rework on Closed status. That number is 21% of the total number of incidents that were assigned to PO Group 8 and mined as part of this project. Incidents that were initially assigned to this group are 5.33 times more likely than any other group to have rework on Closed status.

After you have interpreted your results, you can select a particular influencer to view more details about it. Select an influencer, and select **Apply**. Another scheduled task will start, and you can view the progress and results in the scheduled tasks panel.

From the example, if PO Group 8 is applied, you will see results similar to the following:

![Automated root cause analysis details](../image/rca-analysis.png)

From this graph, you can analyse why some records are moving from Closed to Resolved before going to Process End.

**Parent Topic:**[Automated root cause analysis](auto-rca.md)

