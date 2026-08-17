---
title: Install billing account
description: You can install the billing account application \(com.snc.billing\_account\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren't already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/install-billing-account.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Configuring billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Install billing account

You can install the billing account application \(com.snc.billing\_account\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren't already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Order Management](https://store.servicenow.com/store/app/813bab2a1b246a50a85b16db234bcb8e) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The billing account application has a modular plugin structure:

-   Base plugin \(com.snc.billing\_account\): Independent core functionality for billing account management
-   CSM integration: Install com.sn\_customerservice and com.snc.cs\_base to enable billing account integration with core CSM capabilities and the Related Party Framework
-   CSM Workspace support: Install com.snc.uib.csm\_agent\_workspace to enable CSM Workspace support for billing account integration
-   Household functionality: Install com.snc.household for household-related billing scenarios
-   Install Base and Sold Product functionality: Install sn\_install\_base for product inventory integration

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select **New** from the billing accounts record.

3.  On the form, fill in the fields.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the billing account.

</td></tr><tr><td>

Number

</td><td>

Internal unique number identifying the billing account.

</td></tr><tr><td>

Billing account type

</td><td>

Organization or user type associated with this billing account.When the **Billing account type** field has no value, the displayed fields vary by view type:

-   default view displays **Company** and **User** fields.
-   case view displays **Account**, **Contact**, and **Consumer** fields.


</td></tr><tr><td>

Parent billing account

</td><td>

References the parent billing account.

</td></tr><tr><td>

Status

</td><td>

Indicates the current state of the billing account.

</td></tr><tr><td>

Account

</td><td>

Customer account to which this billing account belongs.In the default view, this field appears when the billing account type is Customer account.

</td></tr><tr><td>

Contact

</td><td>

Customer contact to which this billing account belongs.In the default view, this field appears when the billing account type is Customer account.

</td></tr><tr><td>

Consumer

</td><td>

Consumer to which this billing account belongs.In the default view, this field appears when the billing account type is Consumer.

</td></tr><tr><td>

Start date

</td><td>

Date when the billing account is set to active.

</td></tr><tr><td>

End date

</td><td>

Date when the billing account is closed or terminated.

</td></tr><tr><td>

Currency

</td><td>

Currency used for transactions in this billing account.

</td></tr><tr><td>

Active

</td><td>

Status of the configuration. By using this functionality, you can enable or disable this configuration.

</td></tr><tr><td>

Description

</td><td>

Description of the billing account.

</td></tr></tbody>
</table>4.  Select **Submit** to create billing account record.

    You can create a billing account directly from an account or consumer record by using the **Billing Accounts** related list. When you create a billing account this way, the source **Customer** and the **Billing account type** are set automatically:

    -   While creating from an account record, the billing account type is set to **Customer account**.
    -   While creating from a consumer record, the billing account type is set to **Consumer**.
    You can change the billing account type before you save the record.


