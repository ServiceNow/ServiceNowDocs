---
title: Now Assist Guardian CSM filters
description: Activate base system Now Assist Guardian CSM filters to automatically detect sensitive content in case conversations using the emotional tone of the message.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Now Assist Guardian CSM filters

Activate base system Now Assist Guardian CSM filters to automatically detect sensitive content in case conversations using the emotional tone of the message.

## Before you begin

Role required: admin

-   Now Assist for CSM must be enabled in your environment.
-   Virtual Agent must be configured with topics for handling sensitive content scenarios.

## About this task

Guardian filters analyze case conversation content using Now Assist's sentiment analysis engine and detect sensitive or high-risk content. When a filter detects content matching its configured criteria, it redirects the user to a Virtual Agent topic to handle that type of sensitive issue. Now Assist Guardian filters for CSM identify cases that contain sensitive content such as data breaches, legal threats, or reputational risks. By activating these filters, you can confirm that cases involving critical issues are flagged and handled appropriately, reducing response times and improving risk mitigation.

|Filter name|What it detects|Example use case|
|-----------|---------------|----------------|
|**Active Data Loss or security breach**- Refers to issues related to security incidents that can put sensitive data at risk. It can include questions about ongoing security incidents, confidential information, or personally identifiable information.|Content indicating unauthorized data access, data ex filtration, or active security incidents|Customer reports that their account credentials were exposed in a third-party breach|
|**Threatening legal action**- Refers to issues that may arise in business-to-business or business-to-customer interactions related to legal action. It includes any threats to sue and questions related to past and present litigation.|Language suggesting the customer intends to pursue legal remedies or regulatory complaints|Customer states they will contact their attorney or file a complaint with regulatory authorities|
|**Reputational incident/issue**- Refers to issues related to the reputation of either the service provider or the customer. It includes any content that could be perceived as harmful to the reputations of either party.|Content that could damage the organization's public image or brand reputation|Customer threatens to share negative experiences on social media or with industry publications|

## Procedure

1.  Navigate to `https://<instance-name>.service-now.com/now/now-assist-admin/filters`.

2.  Locate the filter you want to activate in the filter list.

    There are 3 filters available- **Active Data Loss or security breach**, **Threatening legal action**, **Reputational incident/issue** to choose from.

3.  Select **Activate**.

4.  In the **General details** step, review or edit the filter name and description if needed.

    -   **Filter name**: The display name shown in the admin interface
    -   **Description**: Explanation of what the filter detects
    -   **Filter group**: Edit priority order for the filter in each given filter group it belongs to
5.  Select **Save and Continue**.

6.  In the **Sample phrases** step, add example phrases that the filter should detect.

    -   Enter phrases that represent the type of content you want to identify.
    -   Add multiple sample phrases to improve detection accuracy.
7.  Select **Save and Continue**.

8.  In the **Applicability** step, select which Virtual Agents this filter applies to.

    You can apply the filter to one or more Virtual Agent configurations.

9.  Select **Save and Continue**.

10. In the **Filter topic** step, review the Virtual Agent topic that users will be redirected to when sensitive content is detected.

    **Tip:** Select **Preview topic in Virtual Agent** to customize the redirect topic in Virtual Agent Designer.

11. Select **Save and Continue**.

12. In the **Review and activate** step, review all configurations.

13. Select **Activate** to enable the filter.


## Result

The filter is now active and will detect sensitive content in case conversations for the selected Virtual Agents. When matching content is detected, users are redirected to the configured Virtual Agent topic.

## What to do next

Test the filter by creating a test case with sample phrases that should trigger detection. Monitor filter performance and adjust sample phrases as needed to improve accuracy.

**Related topics**  


[bundle-platai.now-assist-guardian]

