---
title: Using Virtual Agent Topic Recommendations
description: Use the Topic Recommendations app to identify pre-built Virtual Agent topics that can be quickly implemented in your organization. Topic Recommendations uses Intent Discovery to analyze data from your organization and to find relevant pre-built topics that your organization can benefit from, and new topics that would be useful to create.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using Virtual Agent Topic Recommendations

Use the Topic Recommendations app to identify pre-built Virtual Agent topics that can be quickly implemented in your organization. Topic Recommendations uses Intent Discovery to analyze data from your organization and to find relevant pre-built topics that your organization can benefit from, and new topics that would be useful to create.

The Topic Recommendations app lets you evaluate the common use cases that Virtual Agent can help resolve or deflect. You can use Topic Recommendations with Virtual Agent topics that use either keyword or NLU topic discovery. Use it to do the following:

1.  Choose the ServiceNow data to analyze \(configure analysis\).
2.  Analyze your existing data \(run the analysis you configured\).
3.  Review the analysis results and use pre-built solutions:
    -   Duplicate a pre-built topic suggestion, such as a topic from ITSM Virtual Agent Conversations \(available from the ServiceNow Store\).
    -   \[NLU only\] Add an intent to your model and a new empty topic. You must provide the flow for the new topic in Virtual Agent Designer.

The Topic Recommendations app requires NLU Workbench and ITSM Virtual Agent Conversations from the ServiceNow Store. The Australia release of Topic Recommendations supports only ITSM Virtual Agent recommendations. Although Topic Recommendations uses NLU Workbench for machine learning purposes, it does not require that NLU be enabled in Virtual Agent.

For information about the apps that are automatically installed with Topic Recommendations, see [Update Topic Recommendations](../task/install-tr.md).

## Required plugins

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Topic Recommendations requires the following plugins and ServiceNow Store applications. Ensure that they are activated before you install Topic Recommendations.
    -   **Required ServiceNow plugins**
        -   **Glide Virtual Agent \(com.glide.cs.chatbot\)**

            Activates all the plugins needed to run Virtual Agent Pro. For details, see [Activate Virtual Agent](../task/activate-virtual-agent.md).

            **Note:** Starting with the San Diego release, the Topic Recommendations app is automatically installed when you initially activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\). Subsequent updates for this app must be installed from the ServiceNow Store.

        -   **NLU Workbench \(NLU topic discovery only\)**

            Activates the plugins needed to run Natural Language Understanding in your instance. For more information, see Activate the NLU Workbench.

    -   **Required ServiceNow Store applications**
        -   **Intent Discovery \(NLU discovery only\)**

            Identifies user intents from analyzing incident/case data. To learn more, see Intent Discovery.

        -   **ITSM Virtual Agent Conversations**

            Provides pre-built IT service management conversations to help your organization quickly deploy automated self-service conversations. For more information, see ITSM Virtual Agent.


## Items installed with Topic Recommendations

The following items are installed with Topic Recommendations:

-   Scheduled jobs: **Run Topic Recommendation Reports** for running Topic Recommendation reports at scheduled times.
-   The following tables are installed:

<table id="table_xc4_gtn_44b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default settings for Topic Recommendations\[sn\_topic\_recommend\_default\_setting\]

</td><td>

The source data \(table and text field\), taxonomy, and filters used when running a Topic Recommendations analysis

</td></tr><tr><td>

Installed recommended topics\[sn\_topic\_recommend\_topic\_staging\]

</td><td>

Topics generated for recommended topics

</td></tr></tbody>
</table>
## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## What to do

-   [Get started with Topic Recommendations](getting-started-topic-recommendations.md)
-   [Define default recommendation settings](../task/define-tr-settings.md)
-   [Run a Topic Recommendation analysis](../task/run-tr-analysis.md)
-   [Add recommended topics and intents to Virtual Agent](../task/add-tr-results-va.md)
-   [Link a topic recommendation to an existing Virtual Agent topic](../task/link-tr-existing-va-topic.md)
-   [Unlink a topic recommendation from an existing Virtual Agent topic](../task/unlink-tr-va-topic.md)
-   [Troubleshoot issues with Topic Recommendations](tr-troubleshooting.md)

