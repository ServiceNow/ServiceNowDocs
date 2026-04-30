---
title: Removed features and products in Yokohama
description: Cumulative release notes summary on features that were removed from Yokohama features and products.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 4
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Removed features and products in Yokohama

Cumulative release notes summary on features that were removed from Yokohama features and products.

Some features were removed as part of Yokohama product updates.

<table id="rn-summary-removed-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Change Management

</td><td>

Change Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Dynamic Translation

</td><td>

The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is no longer available because IBM has withdrawn this translation service. For more information, see [IBM Watson Language Translator Service spoke](https://www.servicenow.com/docs/access?context=ibm-translation-spoke&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Field Service Management

</td><td>

The approval for new requests workflow was removed from the Field Service Management Business Process configuration. Existing customers that use this workflow are unaffected. New customers can use ServiceNow® Workflow Studio to build the approval for the new requests workflow. For more information on Workflow Studio, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

ITOM Optimization

</td><td>

-   In the **Resource Block** &gt; **Operations** &gt; **Steps**, within the **Add Operations Steps** dialog box, the **Invoke Workflow** option has been removed from the Operation Type field.
-   In the **Resource Block** &gt; **Operations** &gt; **Steps**, within the **Add Operations Steps** dialog box, the **Workflow** check box has been removed from the Add Operations Steps field.
-   In the **Cloud Catalog Items**, under the **Operation Implementation** drop-down list, the **Workflow** option has been removed.

</td></tr><tr><td>

Impact

</td><td>

The Expert Connect Accelerator is no longer supported as of Yokohama.

</td></tr><tr><td>

Integration Hub

</td><td>

**Important:**

-   Starting with the Yokohama release, Microsoft Teams Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Microsoft Teams Graph Spoke provides the latest experience for this functionality.

For more information, search for the term `Microsoft Teams Spoke for ServiceNow IntegrationHub` in [Plugins planned for deprecation](../eol/plugin-changes-v-to-y.md#).

-   Starting with the Yokohama release, Gremlin Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Spoke Generator provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr><tr><td>

MID Server

</td><td>

-   When upgrading to the Yokohama release, 3DES will be permanently removed from MID Server to improve security. See [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950) for more information.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

[Yokohama Patch 12](../quality/yokohama-patch-12.md)

-   Spoke generation has been removed from Now Assist for Creator. See the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website for additional information.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   Starting with version 2.0.1 of AI Agents for Observability, the sn\_obs\_aia.admin role, previously required to configure AI agents in the Analyze alert impact agentic workflow, has been removed. Users must now have the credential\_admin and connection\_admin roles instead.
-   Starting with version 2.0.1 of AI Agents for Observability, the prompt `How severe is this alert?` no longer appears in the Analyze alert impact agentic workflow.

</td></tr><tr><td>

Password Reset

</td><td>

Password Reset workflows are deprecated and have been replaced by flows in the base system for most users. zBoot users must still use the Password Reset flows.

</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   Related documents related list will be hidden for both the workspace and classic view for a regulatory alert.
-   The entity class configuration has been removed and is no longer necessary for conducting an assessment. You can select the entities now when you send the risk assessment.
-   Starting with the Yokohama release, all open assessments for a regulatory alert, whether they’re risk assessments or regulatory assessments, aren’t marked as canceled and remain open even after an alert is marked as applicable.

</td></tr><tr><td>

Service Level Management

</td><td>

Service Level Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Service Reliability Management

</td><td>

The **Alerts** tab has been removed from the Reliability tasks page.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   The `now-sdk convert` command has been removed. Use the `now-sdk init` and `now-sdk transform` commands instead.
-   The `now-sdk fetch` command has been removed. Use the `now-sdk transform` command instead.

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

The **All categories** option has been removed from the **Categories** tab in Shopping Hub due to low usage and its impact on system performance.

</td></tr><tr><td>

Subscription Management

</td><td>

The Custom tables chart has been removed from the subscription details page.

</td></tr><tr><td>

Usage Insights

</td><td>

-   Automatic actions in the mobile app, including tap and swap.
-   Filtering by crashed/offline sessions in mobile applications.
-   Option to tag/favorite for users/sessions.
-   Geographic map view of sessions.
-   Users flow
-   Insights

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](../release-notes-summaries.md)

