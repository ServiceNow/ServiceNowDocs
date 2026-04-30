---
title: Troubleshoot issues with Topic Recommendations
description: Investigate and resolve unexpected behavior with Topic Recommendations, or find answers to common questions.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Virtual Agent Topic Recommendations, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Troubleshoot issues with Topic Recommendations

Investigate and resolve unexpected behavior with Topic Recommendations, or find answers to common questions.

For information about using Topic Recommendations, see [Quick start for Topic Recommendations](getting-started-topic-recommendations.md).

**Note:** Topic Recommendations tries to train the model when you add new topics to Virtual Agent. If an error occurs during training, the topic is still added, but the model remains in a draft state.

<table id="table_wgk_kyg_mrb"><thead><tr><th>

Issue

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Topic Recommendations page is blank

</td><td>

No analysis reports have been configured.[Configure an analysis report](../task/define-tr-settings.md). You can also install or activate ITSM Virtual Agent Conversations, which will add default configurations to Topic Recommendations. For more information, see [Set up ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=setup-itsm-virtual-agent&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Error when adding topics to Virtual Agent

</td><td>

Check the error log for details:1.  Navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **Errors**.
2.  Find the entry that has a value of **sn\_topic\_recommend** in the Source column.

The Message field displays the error.

**Note:** If model training fails while adding topics, Topic Recommendations will ignore those errors and continue to add your recommendations. In this case, you will be notified that the models are in draft state.


</td></tr><tr><td>

Reports have intent matches, but no pre-built topic matches

</td><td>

Make sure ITSM Virtual Agent Conversations is installed and activated for the instance. If the app is installed, then none of the pre-built topics address the issues found in your reports. For more information, see [Set up ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=setup-itsm-virtual-agent&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Analysis reports are not available in production instances

</td><td>

This is the expected behavior. Analysis reports and Intent Discovery are designed to live in one instance only. Added topics and NLU models are made available in a "new" instance, but the Topic Recommendations reports do not move between instances.

</td></tr><tr><td>

Analysis report is stuck and says "Analysis in progress"

</td><td>

Check the status in the Discovery Report Definitions table:1.  Navigate to **All** &gt; **sn\_nlu\_discovery\_report\_definition.list**.
2.  Sort the table on the Created column, and then find the name of the affected analysis definition.
3.  If the Status column is empty, the analysis failed. Try running it again.

 You can also navigate to **NLU Workbench** &gt; **Intent Discovery** to see if something went wrong in the intent discovery process. For more information, see [Intent Discovery](https://www.servicenow.com/docs/access?context=intent-discovery&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Adding new topics takes longer than expected

</td><td>

Try the following:-   Navigate to **All** &gt; **sn\_topic\_recommend\_topic\_staging.list** and view the Status column to see what stage topic generation is in. Training models can take some time.
-   Navigate to **All** &gt; **System Logs** &gt; **Events** to see which event ran last or if the event is queued.
-   If the reason for failure is not clear, navigate to **All** &gt; **sn\_topic\_recommend\_topic\_staging.list** and change the value of the Status field to `Error`. You can then try to add the recommendation again.

</td></tr><tr><td>

Can't generate a report with less than 10,000 or more than 300,000 records

</td><td>

Topic Recommendations currently supports a minimum of 10,000 records and a maximum of 300,000 records. This is done for performance and to ensure a statistically significant data set.

</td></tr><tr><td>

Model is not preselected in the app

</td><td>

If you are upgrading from Quebec and this is your use of the Topic Recommendations app, you must select a model. Once you select a model, Topic Recommendations preserves the selection.

</td></tr><tr><td>

Unmigrated model support

</td><td>

While you are encouraged to migrate your models to groups, Topic Recommendations does not require models to be grouped.

</td></tr><tr><td>

Unlinked topics

</td><td>

You don't have to link all recommendations. Topic linking is a way to "acknowledge" a recommendation if you have an existing topic.

</td></tr><tr><td>

The **Topics/Requests VA Can Handle** tab is not displayed

</td><td>

System property `glide.ui.escape_all_script` is not set to True.

Navigate to **ALL &gt; sys\_properties.list** \(or **ALL sys\_properties\_list.do**\). Search for and select `glide.ui.escape_all_script`, then set its Value to **True**.

</td></tr></tbody>
</table>