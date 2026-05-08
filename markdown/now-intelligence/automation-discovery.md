---
title: Automation Discovery
description: ServiceNow Automation Discovery helps you identify automation opportunities for your workflows. Use the discovery reports to implement or improve automation solutions like Virtual Agent \(VA\), and Agent assist.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Platform Analytics]
---

# Automation Discovery

ServiceNow® Automation Discovery helps you identify automation opportunities for your workflows. Use the discovery reports to implement or improve automation solutions like Virtual Agent \(VA\), and Agent assist.

## Summary usage

**Important:** Starting with the Zurich release, Automation Discovery is deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in Australia. Support will be withdrawn in a future release. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Automation Discovery analyzes your records to help you identify opportunities for automation.

With the app, you can run discovery reports that analyze a specified dataset of records against a pre-built taxonomy. The model identifies over 180 possible opportunities for automation from your records. Think of the opportunities as intents that the system can respond to your users' queries automatically.

The report groups records by the predicted opportunity for automation. For uncategorized records, the report groups the records together in related clusters.

For applications such as Virtual Agent, Automation Discovery helps you implement automation opportunities that can lead to deflections and faster incident resolutions.

## Installation

Automation Discovery is available from the ServiceNow Store. For more information, see [Install Automation Discovery](../task/install-automation-discovery.md).

## Language support

Automation Discovery supports English, Spanish, French, German, and Japanese instances, for reports created using the **ITSM** taxonomy.

Reports created using the **Predictive AIOps** taxonomy support only English, because that model's training data consists of English log messages.

## Discovery reports

![Automation Discovery Reports list that shows all created reports.](../images/automation-discoveryT3.png)

The **Automation Discovery Reports** page lists your created reports. For each report, the page lists the following information:

|Column|Description|
|------|-----------|
|Name|Name given to the report during creation.|
|Data Source|Source of the records analyzed.|
|Model|Taxonomy for running the report against.|
|Automation Opportunities|Number of different pre-built intents that match with your records.|
|Not Categorized|Number of clustered groups that contain utterances that do not match the pre-built topics.|
|Total Records|Number of records analyzed in the report.|
|Run Date|Time and date of the most recent run.|
|Frequency|Number of times to run the report.|
|Status|Status of the report.|

To create a new report, see [Create an Automation Discovery report](../task/create-auto-discovry-report.md).

To view results, select the name of the report.

## Report breakdown

For each successful report, the report page shows information about automation opportunities.

![Automation Discovery report page for an incident-based report.](../images/automation-discoveryT1.png)

The report groups matching records together by opportunity. In this example, Automation Discovery found 125 opportunities for automation from the thousands of incidents analyzed. Several records group to the same opportunities because the incidents match the same intents.

Deflections refer to incidents that could have been immediately resolved through automation. Automation Discovery adds up all the records that match an automation opportunity to get the **Possible Deflections** number. Some opportunities have matching pre-built VA topics, marked as **Virtual Agent Ready.**

MTTR or mean time to resolve refers to the average amount of time it takes to resolve incidents. The report multiplies the number of matching records by the MTTR to get the **Estimated Time Savings** for the top 10 opportunities.

![Automation Opportunities list item expanded. Shows the opportunity in more detail and actions you can take.](../images/automation-discoveryT2.png)

The **Automation Opportunities** tab lists the automation opportunities that match your data. Select the list icon on each row to see more information about the records for that opportunity.

The **Not Categorized** tab shows the clusters of records that do not match prebuilt intents. The report attempts to group uncategorized records into clusters based on similarities. Click the list icon on each row to see more information about the records in that cluster.

## Adding opportunities to Topic Recommendations

Virtual Agent Topic Recommendations helps you improve the automation for Virtual Agent. You can add automation opportunities from your Automation Discovery reports to Topic Recommendations.

The **Actions You Can Take** card shows what you can do with the automation opportunities from your reports. For opportunities that are **VA Ready**, select **Open Topic Recommendations** to add the opportunity to Topic Recommendations.

In Topic Recommendations, you can add topics to your Natural Language Understanding \(NLU\) models and to Virtual Agent. If you add an opportunity to a model, the **Action Taken** shows the corresponding intent or model.

To learn more see Using Virtual Agent Topic Recommendations and NLU models.

You can also create custom topics for opportunities that are not VA ready. For more information about creating custom topics, see [Creating Virtual Agent Topics](https://developer.servicenow.com/dev.do#!/learn/learning-plans/quebec/servicenow_application_developer/app_store_learnv2_virtualagent_quebec_creating_topics) on the ServiceNow Developer Site.

## Sharing and flagging

You can share your discovery reports with other members on your team. On a report page, click **Share Report** to open the report sharing pop-up.

![Pop-up menu for sharing a report.](../images/share_report.png)

You can share the report with the provided link or by sending the report via email.

**Note:** User must have the nlu\_admin or nlu\_user role to view Automation Discovery reports.

You can also flag specific automation opportunities that you want to highlight. To flag an opportunity, click the flag icon. To include flagged items when you share the report, select the **Include Flagged Items** check box.

## Properties

The Automation Discovery **Properties** page lets you control the settings for the discovery reports.

Setting a minimum and maximum number of records helps you control the amount of data that you want to analyze. You can also set the number of unique unmatched records for clustering to work on your report.

Enabling sampling of data before clustering is run can help speed up the report generation. However, the report clusters a smaller amount of the unmatched records.

**Related topics**  


[bundle-convint.virtual-agent-landing-page]

