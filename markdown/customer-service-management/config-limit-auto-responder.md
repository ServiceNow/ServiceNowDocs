---
title: Limit the number of articles in Auto-Responder notifications for cases
description: Send the most relevant knowledge articles in Auto-Responder notifications for customer service cases by limiting the number of knowledge articles that are included.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Limit the number of articles in Auto-Responder notifications for cases

Send the most relevant knowledge articles in Auto-Responder notifications for customer service cases by limiting the number of knowledge articles that are included.

## Before you begin

-   Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).
-   Set the application scope to Customer Service using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Search for `Case [sn_customerservice_case]`.

3.  Click the **Case \[sn\_customerservice\_case\]** link in the **Name** column corresponding to the row containing the **Case Email Autoresponder KB Search** search context.

4.  In the Email Configurations related list, double-click the value in the Limit column for the **Case auto-responder recommendations** row.

5.  Enter the maximum number of knowledge articles you want to include in the Auto-Responder email notifications for customer service cases and click the save icon \(![Save icon.](../image/save.png)\).

    The maximum allowed limit value is 20. If you enter a limit value of more than 20, the Auto-Responder email notification includes up to 20 articles only.

6.  On the Table Configuration form, click **Update**.


