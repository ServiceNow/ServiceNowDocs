---
title: Performance Analytics diagnostics
description: Identify and diagnose configuration issues using predefined scripts that examine the database for invalid records and provide suggestions to resolve issues.To determine if any configuration issues could impact your Performance Analytics implementation, run diagnostics. You can select whether to run one diagnostic or all diagnostics. The diagnostics examine the subset of Performance Analytics records to which they logically apply.To determine if any of the configuration details of a record could impact your Performance Analytics implementation, run the set of all applicable diagnostics on that record.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Performance Analytics diagnostics

Identify and diagnose configuration issues using predefined scripts that examine the database for invalid records and provide suggestions to resolve issues.

Each diagnostic consists of a script or database query with a severity code, message text, and suggested solution. Diagnostics are read-only. You cannot create or edit diagnostics.

You can run one or all diagnostics against all applicable records, or you can run all applicable diagnostics against one record.

**Warning:** Performance Analytics diagnostics do not apply to Platform Analytics artifacts. For example, an indicator that is not used in any widgets might still be used in a Platform Analytics data visualization, but the diagnostics are not able to recognize that use.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

## Execute diagnostics for all records

To determine if any configuration issues could impact your Performance Analytics implementation, run diagnostics. You can select whether to run one diagnostic or all diagnostics. The diagnostics examine the subset of Performance Analytics records to which they logically apply.

### Before you begin

Role required: sn\_pa\_diagnostics.pa\_diagnostic

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Diagnostics**.

2.  Select the diagnostic you want to run.

    To run all active diagnostics, click **Execute All** from the list.

3.  Click **Execute Diagnostic**.

    The diagnostics script is canceled automatically if it takes longer than 2 minutes to run.

4.  After the diagnostic completes, click **View Result**.


### What to do next

If a diagnostic returns a warning or error, review the provided solution and take steps to resolve the issue.

## Run all active diagnostics for one record

To determine if any of the configuration details of a record could impact your Performance Analytics implementation, run the set of all applicable diagnostics on that record.

### Before you begin

Role required: sn\_pa\_diagnostics.pa\_diagnostic

### Procedure

1.  Navigate to **Performance Analytics** and open a list of any components: indicators, indicator sources, breakdowns, breakdown sources, widgets, or others.

2.  Locate and open the record of interest.

3.  Click the link **Run diagnostics**.

    A dialog opens to show the progress of the diagnostics.

4.  When the diagnostic run is complete, click **View Result** in the progress dialog.


### What to do next

If a diagnostic returns a warning or error, review the provided solution and take steps to resolve the issue.

