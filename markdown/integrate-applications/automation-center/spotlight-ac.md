---
title: Working with ServiceNow Spotlight feature
description: Use the ServiceNow Spotlight feature to auto-calculate automation request scores. Scores define the execution priority of the automation request. The higher the score, the higher the priority of the automation request.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Automation Center, Workflow Data Fabric]
---

# Working with ServiceNow Spotlight feature

Use the ServiceNow Spotlight feature to auto-calculate automation request scores. Scores define the execution priority of the automation request. The higher the score, the higher the priority of the automation request.

ServiceNow Spotlight calculates scores when an automation request is created or updated. It's calculated only when the automation request is in the **New** or **Deferred** state.

If there’s any special need to have a different score than the auto-computed score, you can manually update the **Score** field. When you do that:

-   The flag **Score manually altered** is turned on.
-   The Spotlight score is computed and calculated in the **Score auto calculated** field.

You can switch over to using computed score by emptying the **Score** field or setting it to 0. After you save the request record, the system will populate the Spotlight score \(if any\) in the **Score** field.

-   **[Configuration Settings for ServiceNow Spotlight](spotlight-config.md)**  
To use the ServiceNow Spotlight feature, set the configuration settings.
-   **[Default criteria](default-spotlight-criteria.md)**  
ServiceNow Spotlight is available with default criteria. Each field provides a score based on the default criteria.
-   **[Set up ServiceNow Spotlight](../task/setup-spotlight.md)**  
Set up ServiceNow Spotlight to start using and getting the benefits of this feature. The Spotlight feature automatically calculates the execution priority of the automation requests.

**Parent Topic:**[Configuring Automation Center](automation-center-setup.md)

