---
title: Topic Recommendations settings
description: Use the Topic Recommendations settings page to configure analysis reports based on your ServiceNow data.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Topic Recommendations interface reference, Using Virtual Agent Topic Recommendations, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Topic Recommendations settings

Use the Topic Recommendations settings page to configure analysis reports based on your ServiceNow® data.

You can find the Topic Recommendations settings in the Conversational Interfaces Chat Settings \(**All** &gt; **Conversational Interfaces** &gt; **Settings**\) under Virtual Agent. When you first install Topic Recommendations, nothing is configured, so the settings page appears empty.

![The Topic Recommendations settings page is empty until you configure reports.](../images/tr-settings-new-install.png "Empty Topic Recommendations settings page")

Once configured, you can view or edit analysis reports on this page.

![The Topic Recommendations settings page with two configured reports by data source: sc_request and incident.](../images/tr-settings-configured.png "Configured Topic Recommendations settings")

## Topic Recommendations analysis settings

When you create or edit a Topic Recommendations analysis record, specify the information in the following form.

<table id="table_kb4_hyn_m4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

ServiceNow table that contains the data to be analyzed.

</td></tr><tr><td>

Field analyzed

</td><td>

Field \(string column\) in the table to be analyzed. For example, the **Short description** in the Incident table.

</td></tr><tr><td>

Taxonomy

</td><td>

Comprehensive list of intents for a specific business application, such as ITSM.

</td></tr><tr><td>

Filter by

</td><td>

Condition builder for filtering the records to be analyzed. Click **Set conditions** to open the condition builder.The default filter is **\[Created\] \[after\] \[Last 90 days\]**.

</td></tr><tr><td>

Frequency

</td><td>

The schedule for running the analysis, which is triggered through the Run Topic Recommendation Reports scheduled job:-   None
-   Every Month
-   Every 3 Months
-   Every 6 Months
-   Every 12 Months

**Note:** If you're using a non-production instance for testing, set the analysis schedule in your production instance so that it and your analysis history are retained. The intent discovery process works best in a single instance, where data is not promoted between instances.

</td></tr></tbody>
</table>**Related topics**  


[Configure analysis reports for Topic Recommendations](../task/define-tr-settings.md)

