---
title: Reclaim user subscriptions in the Software Asset Workspace
description: Reclaim unused SaaS and SSO subscriptions in the Software Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/reclaim-user-subscription-saas-workspace.html
release: brazil
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Reclaiming user subscriptions, SaaS License Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Reclaim user subscriptions in the Software Asset Workspace

Reclaim unused SaaS and SSO subscriptions in the Software Asset Workspace.

## Before you begin

To reclaim user subscriptions in the Software Asset Workspace, you must request and activate the Software Asset Workspace \(sn\_sam\_workspace\) store application. See [Request Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/t_RequSoftwareAssetMgmt.md) for more details on requesting and activating the Software Asset Workspace \(sn\_sam\_workspace\) store application.

Role required: sam\_user

**Important:** The SaaS License Management SurveyMonkey integration doesn't support reclamation through the ServiceNow AI Platform. To reclaim a SurveyMonkey user subscription, you must reassign or delete the user from your SurveyMonkey team directly using the SurveyMonkey admin portal. After the user is removed from your team, you must update the state of the corresponding removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table. See [Reclaim SurveyMonkey user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaim-surveymonkey-subscription-workspace.md) for detailed instructions.

**Important:** The SaaS License Management monday.com integration does not support reclamation through the ServiceNow AI Platform. To reclaim a monday.com user subscription, you must deactivate the user on your monday.com account. After the user is deactivated, you must update the state of the corresponding removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table. See [Reclaim monday.com user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaim-monday-subscription-workspace.md) for detailed instructions.

**Important:** The SaaS License Management Roadmunk integration does not support reclamation through the ServiceNow AI Platform. To reclaim a Roadmunk user subscription, you must deactivate the user on your Roadmunk account. After the user is deactivated, you must update the state of the corresponding removal candidate to **Closed Skipped** so that the user subscription is removed from the Software Subscriptions \[samp\_sw\_subscription\] table. See [Reclaim Roadmunk user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaim-roadmunk-subscription-workspace.md) for detailed instructions.

## Procedure

1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **Software Asset Workspace**.

2.  To reclaim a user subscription that was not automatically identified by a software reclamation rule, create a software removal candidate.

    See [Create a software removal candidate in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/add-sw-removal-workspace.md) for detailed instructions on how to create a software removal candidate in the Software Asset Workspace.

3.  From the side menu of the Software Asset Workspace, navigate to **License operations** &gt; **Reclamation** &gt; **Removal candidates**.

4.  Reclaim user subscriptions.

    -   To reclaim all user subscriptions, select **Reclaim All**.

        **Note:** You must confirm before reclaiming all user subscriptions. Some users may still need their subscriptions even if they have no activity.

    -   To reclaim an individual user subscription, select a removal candidate and then select **Reclaim** on the Removal Candidate form.


## Result

After you reclaim a user subscription, the subscription record is deleted from the Software Subscriptions \[samp\_sw\_subscription\] table. The reclamation candidate state is set to **Closed Complete**. If the reclamation fails, the state is set to **Attention Required**. An error message is displayed at the top of the screen with additional details on how to resolve the error.

-   **[Reclaim SurveyMonkey user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaim-surveymonkey-subscription-workspace.md)**  
Reclaim unused SurveyMonkey subscriptions to reduce your total software costs.
-   **[Reclaim monday.com user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaim-monday-subscription-workspace.md)**  
Reclaim unused monday.com subscriptions to reduce your total software costs.
-   **[Reclaim Roadmunk user subscriptions in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaim-roadmunk-subscription-workspace.md)**  
Reclaim unused Roadmunk subscriptions to reduce your total software costs.

**Parent Topic:**[Reclaiming user subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/reclaiming-user-subscriptions-saas.md)

