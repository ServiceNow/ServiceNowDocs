---
title: Configure the webhook registry
description: Configure a callback URL for communication between the Legal Matter Management and Legal Tracker applications.
locale: en-US
release: zurich
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Legal Matter Management with outside counsel, Configure, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure the webhook registry

Configure a callback URL for communication between the Legal Matter Management and Legal Tracker applications.

## Before you begin

Ensure you have installed and activated Legal Tracker spoke. For more information, see [Legal Tracker](https://www.servicenow.com/docs/access?context=legal-tracker-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

Role required: admin, sn\_lg\_ops.legal\_fulfiller

## About this task

Configuring the webhook registry is required to synchronize updates in the External Matter record in the Legal Matter Management from the Legal Tracker application. After successful configuration, the Health status of the configuration must be Healthy. If the status is Broken, synchronization of the updates fails.

## Procedure

1.  Set the application scope to Legal Matter Management.

2.  If the application scope is not set correctly, perform the following:

    1.  Select the Application scope icon \(![Application scope icon](../../workplace-calendar-synchronization/image/application-scope-globe-icon.png)\).

    2.  Select the option **Application scope**.

    3.  In the filter navigator, search for and select Legal Matter Management.

    4.  Refresh the page.

3.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

4.  Select **Label** for the Search scope and enter `webhook`.

5.  Select **Legal Tracker Webhook Registry** from the list.

6.  Select **Show Form** from the Related Links section.

7.  In the Description field, enter the description of the webhook.

8.  In the Token field, fill in the details.

    1.  Select the Lookup using the list icon ![Lookup using list icon.](../../workplace-case-mgmt/image/search-icon.png).

    2.  Select **New**.

    3.  Fill in the details in the **Token Verification New Record** form.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the token.|
        |Description|Description of the token.|
        |Token|Password to access the token.|

    4.  Select **Submit**.

9.  In the Name field, enter the name of the webhook.

10. Right-click in the page header and select **Save**.

11. Select **Callback URL**.

    In the info message that appears, the Callback URL is displayed. Copy this URL to use in the Callback URL field in the Legal Tracker platform.

12. Log in to your Legal Tracker instance and select the settings icon \(![Settings icon](../image/settings.png)\).

13. In the Integrations section, select **Webhooks**.

14. In the Matters section of the Webhooks page, select **Add a new webhook**.

15. On the form, fill in the fields.

<table id="table_j4j_sj1_yyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Callback URL

</td><td>

The Callback URL information copied from the Token Verification page.

</td></tr><tr><td>

Events

</td><td>

Events for which automated information is available on the Legal Matter. The available options are:The **Create** and **Update** check box must be selected to receive the information in the associated Legal Matter for any new or modification made in the Legal Tracker platform.

</td></tr><tr><td>

Secret key

</td><td>

Password to access the webhook information.

</td></tr></tbody>
</table>16. Select **Save &amp; close**.


## Result

The webhook for the Legal Tracker application is successfully configured and the matter updates in Legal Tracker will be synced to Legal Matter Management and the details can be seen in external matter records. For a working webhook configuration, the Health status must be Healthy. For any wrong configurations, the Health status is shown as Broken.

**Parent Topic:**[Configure Legal Matter Management to engage with outside counsel using Legal Tracker](../concept/configurations-for-legal-tracker-integration.md)

