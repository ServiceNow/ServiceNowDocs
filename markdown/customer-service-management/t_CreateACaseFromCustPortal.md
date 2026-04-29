---
title: Create a product case from the Customer Service Portal
description: Create a case about a question or issue on a product from the Customer Service Portal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Customer Service Portal, Customer communication, Use, Customer Service Management]
---

# Create a product case from the Customer Service Portal

Create a case about a question or issue on a product from the Customer Service Portal.

## Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.partner, sn\_customerservice.customer\_admin, or sn\_customerservice.partner\_admin, sn\_acct\_consumer.consumer

## Procedure

1.  Go to the Customer Service Portal by accessing your instance URL and adding a /csm suffix.

2.  Right-click in the form header and choose **Case** &gt; **Create Product Case**.

3.  On the form, fill in the fields.

    **Note:** Depending on your role, you might not see the **Account** and **Contact** fields.

<table id="table_czw_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The account for which the case is being created.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for this case.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer for this case. **Note:** This field is active only when the Customer Data Models for B2B2C plugin is installed. Once Account is selected, only consumers belonging to the account are displayed.

</td></tr><tr><td>

Asset

</td><td>

The asset tag number or the serial number of the asset associated with this case.

</td></tr><tr><td>

Product

</td><td>

The product model of the asset. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\). If you select an asset in the **Asset** field, this field is auto-populated if the associated product information is available in the asset record. A product may be associated with multiple assets.

</td></tr><tr><td>

Priority

</td><td>

The available assigned priorities are:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)


</td></tr><tr><td>

Subject

</td><td>

A brief description of the customer question, issue, or problem.**Note:** When you start entering the subject, the application searches for relevant content in the knowledge bases configured for the portal. the results are displayed in the **Related Content** list.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the customer question, issue, or problem.

</td></tr></tbody>
</table>    **Note:** Currently, the **Save as Draft** option is not optimized for Customer Service Management portals and, it is inactive by default.

4.  Select **Submit**.


## Result

The case is created, assigned a case number, and added to the creator's case list. To view this list, select the **My Lists** tab on the Customer Service Portal header and select **All Cases** in the left pane.

