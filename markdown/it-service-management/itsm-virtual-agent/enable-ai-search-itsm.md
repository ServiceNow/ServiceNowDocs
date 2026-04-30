---
title: Enabling AI Search in Issue Auto Resolution
description: You can enable AI Search as a fallback mechanism in Issue Auto Resolution when there are no matching intents found for the incident.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Issue Auto Resolution for ITSM Virtual Agent, Pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Enabling AI Search in Issue Auto Resolution

You can enable AI Search as a fallback mechanism in Issue Auto Resolution when there are no matching intents found for the incident.

## Applying AI Search for Issue Auto Resolution Configuration

When there are no intent matches found for Issue Auto Resolution, AI Search can be applied for the fallback capability. To use AI Search as fallback:

-   Open the Auto-Resolution Configuration record.
-   Navigate to the **AI Search** tab.
-   Select the **Apply AI Search** check box to enable fallback.

You can see the following AI Search settings from the IAR configuration record which will be used when there are no intent matches for the topic.

-   **EVAM definition**: The entity view action mapper definition is set to **Virtual Agent Search** by default.
-   **Search application**: The default application for AI Search fallback is set to **Service Portal default Search Application**.
-   **AI Search display topic**: The AI Search display topic that is provided by default is the **IAR - AI Search** topic.
-   **Search results portal**: The default portal for AI Search fallback is set to the **Service Portal**.

To support AI Search fallback, ITSM Virtual Agent provides the following intent to topic mappings.

|Auto-resolution intent|Matched topic|
|----------------------|-------------|
|RepositoryAccess|Repository Access \(Template\)|
|Emailissues|Email Issues \(Template\)|
|RSAToken|RSA Token \(Template\)|
|LocalAdminAccess|Local Admin Access \(Template\)|
|CollaborationSoftwareIssues|Collaboration Applications \(Template\)|

Whenever you try to create an incident using Email or Self-service as the channel that triggers IAR, you will receive the relevant recommendations.

There are three types for recommendations, KBs, Catalogs, and VA Topics. For example, if you create an incident and check for its email notifications, you will be shown various recommendations \(including KBs and Catalogs\) for the incident resolution from Issue Auto Resolution.![IAR triggered email notification with KB and Catalog recommendations.](../image/email-notif-rcmndtn-kb.png)

In case there is a matched VA topic from the intent to topic mapping, in that case, you will not receive the KB and Catalog recommendations, but the VA topic name, such as "VA Topic: Printer Issues \(Template\)" in the email notification.![IAR triggered email notification with VA topic recommendation.](../image/email-notif-rcmndtn-vatopic.png)

Once you click **View recommendations** from your email notification, you will be directed to the Service Portal incident which now has a **Recommendations** tab from where you can read the KB and mark the recommendation as helpful and resolve it.

**Note:** In case the recommendations have a catalog item as the recommended option and you create the catalog request from the Recommendations tab, an email notification is triggered and the incident gets auto-closed in 24 hours.![IAR triggered email notification for incident requested.](../image/email-notif-recmndtn-incident-req.png)

**Parent Topic:**[Issue Auto Resolution for ITSM Virtual Agent](itsm-va-auto-resolution.md)

