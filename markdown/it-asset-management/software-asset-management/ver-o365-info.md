---
title: Determine and verify Microsoft 365 subscription information in your ServiceNow instance
description: Determine the exact software subscription information to be pulled from the Microsoft 365 admin center and verify if complete subscription information is pulled accurately to ServiceNow.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Determine and verify Microsoft 365 subscription information in your ServiceNow instance

Determine the exact software subscription information to be pulled from the Microsoft 365 admin center and verify if complete subscription information is pulled accurately to ServiceNow.

## Before you begin

Role required: sam\_admin

## Procedure

1.  Filter with the Microsoft 365 integration profile you created to determine the exact software subscription information to be pulled from Microsoft 365 admin center to ServiceNow.

    This subscription includes all subscriptions available on the Microsoft 365 admin center.

2.  Verify with the Microsoft 365 admin if complete subscription information is pulled accurately to ServiceNow.

    **Note:**

    Software Asset Management pulls the last activity date for Microsoft 365 products using a combination of Microsoft System Center Configuration Manager \(SCCM\) integration and Microsoft 365 integration.

3.  If your Microsoft 365 subscription data isn’t getting pulled into Software Asset Management, verify your integration setup:

    1.  On the Integration Profile form, open the REST message record by selecting the Preview icon ![](../image/preview-icon.png) next to the **REST message** field.

    2.  Select **Open Record** in the record preview.

    3.  On the Rest Message form, select the **Get OAuth Token** related link.

        **Note:** For the role required to perform this step, refer to the [Minimal user permissions](../concept/integrate-with-microsoft.md) table.

    4.  On the OAuth flow verification dialog box, view the status of the OAuth flow to determine whether your integration is set up correctly.

        -   If the `OAuth token flow completed successfully` message appears, your integration is set up correctly.
        -   If the `OAuth flow failed` message appears, your integration isn’t set up correctly. Use the information in this message to identify the errors in your integration setup.
4.  If your Power BI usage isn’t getting pulled into Software Asset Management, verify the status of your Power BI API connection.

    1.  On the Integration Profile form, select and hold \(or right-click\) the form header.

    2.  Select **Show XML**.

        **Note:** If the **Show XML** option isn't visible in the default view, you can customize the view. Select and hold \(or right-click\) the form header and then select **View** &gt; **custom integration**.

    3.  Under **&lt;xml&gt;** &gt; **&lt;samp\_sw\_subscription\_profile&gt;** &gt; **&lt;custom\_properties&gt;**, view the **powerBIAPIStatus** property to determine the status of your Power BI API connection.

        -   If the **powerBIAPIStatus** property is set to **success**, the Power BI API connection was successful.
        -   If the **powerBIAPIStatus** property is set to **failed**, the Power BI API connection wasn’t successful. Verify that you’ve followed all the integration setup steps correctly. You can also check your logs for more information about any errors in your integration setup.
5.  If the **User** field in the Software Subscription \[samp\_sw\_subscription\] table is empty, you can map the field with an associated user.

    For more information, see [Associate a user with subscription records](map-user-data.md).


