---
title: Signed PDF summaries for closed work orders
description: In Field Service Management, customers can digitally sign and confirm work orders that are closed with the Closed Complete or Closed Incomplete state. A PDF summary of the signed work order is then created.You can activate the Field Service - Signature Pad plugin \(com.snc.wo\_signature\_pad\) for Field Service Management if you have the admin role.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Signed PDF summaries for closed work orders

In Field Service Management, customers can digitally sign and confirm work orders that are closed with the Closed Complete or Closed Incomplete state. A PDF summary of the signed work order is then created.

The summary includes the completed tasks, parts used and returned, incidental expenses, and the time required to complete the work. The PDF also includes the name and signature of the customer.

**Related topics**  


[Create a signed PDF summary for a work order](../task/create-wo-pdf-summary.md)

## Activate Field Service Signature Pad

You can activate the Field Service - Signature Pad plugin \(com.snc.wo\_signature\_pad\) for Field Service Management if you have the admin role.

### Before you begin

Field Service Management - Signature Pad requires you to install the Field Service Management plugin \(com.snc.work\_management\). For more information, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

Role required: admin.

### About this task

The following items are installed with Field Service Management - Signature Pad:

-   Tables
-   Script Includes

For more information, see [Field Service - Signature Pad components](../reference/fsm-signed-pdf-components.md).

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service - Signature Pad plugin \(com.snc.wo\_signature\_pad\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


### Result

The Field Service - Signature Pad plugin when activated successfully adds the Signature Capture and PDF Order Summary configurations in the Field Service Configuration page.

**Note:** You must enable [**Signature Capture** and **PDF Order Summary**](../../planning-and-policy/task/t_ConfigureFieldService.md#PDFSummaryOptions) to generate the signed PDF summary of a closed work order.

