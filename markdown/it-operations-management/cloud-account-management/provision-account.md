---
title: Provision a cloud account
description: Provision a cloud account as an admin through Cloud Workspace.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Creating a cloud account, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Provision a cloud account

Provision a cloud account as an admin through Cloud Workspace.

## Before you begin

Confirm that the cloud context has been configured. For more information, see [Creating configurations](../concept/cam-config.md).

Discovery must have been performed on the cloud admin portal.

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Requests**.

2.  On the Account requests page, select the **Approved requests** tile.

3.  Select the account to provision.

4.  In the **Select cloud context** section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Cloud Provider|This field is automatically set to the cloud provider platform in the request.|
    |CAM configuration|Configuration name of the cloud organization.|
    |Organizational unit \(appears for AWS\)|Organizational unit \(OU\) are the list of units populated automatically after discovery is run.|
    |GovCloud Organization \(appears for AWS GovCloud requests\)|The AWS GovCloud organization to which the GovCloud account will be invited.|
    |GovCloud Organizational unit \(appears for AWS GovCloud requests\)|The Organizational unit \(OU\) to which the GovCloud account will be moved.|
    |Management group \(appears for Azure\)|Management groups help you manage multiple subscriptions by applying governance settings that automatically apply to all subscriptions within them. This field is automatically set to the management group found after discovery is performed.|

5.  If you are provisioning an Azure account, determine whether to use an existing billing account or create and add a new billing account.

<table id="choicetable_ovb_tlr_dfc"><thead><tr><th align="left" id="d127143e217">

Option

</th><th align="left" id="d127143e220">

Action

</th></tr></thead><tbody><tr><td id="d127143e226">

**Add an existing billing account**

</td><td>

Select an existing account from the drop-down list.

</td></tr><tr><td id="d127143e235">

**Create and add a new single account**

</td><td>

1.  Select the Create new billing account icon \(![Create new billing account icon](../../../reuse/icons/product-icons/plus-outline-24.svg)\).
2.  Select **Single account**.
3.  In the **Account name** field, enter the account name.
4.  In the **Display name** field, enter the display name.
5.  Select **Add**.


</td></tr><tr><td id="d127143e280">

**Create and add new bulk accounts**

</td><td>

1.  Select the Create new billing account icon \(![Create new billing account icon](../../../reuse/icons/product-icons/plus-outline-24.svg)\).
2.  Select **Bulk upload**.
3.  Search for and select the Tenant name.
4.  Below the **Enter API response** field, select the link [Azure playground](https://learn.microsoft.com/en-us/rest/api/billing/billing-accounts/list?view=rest-billing-2024-04-01&tabs=HTTP#code-try-0).
5.  Sign in to your Azure portal.
6.  From the Azure portal, copy the sample JSON response that appears under the **EnrollmentAccountsListByBillingAccount** section.
7.  In the Cloud Account Management application, paste the sample JSON response in the **Enter API response** field.
8.  Select **Add**.


</td></tr></tbody>
</table>6.  If you are provisioning an Azure account, determine whether to use an existing enrollment account or create and add a new enrollment account.

    An enrollment account is a management unit within a billing account for organizations with an Enterprise Agreement \(EA\) that is used to organize and control Azure subscriptions and resources.

<table id="choicetable_x33_4wr_dfc"><thead><tr><th align="left" id="d127143e370">

Option

</th><th align="left" id="d127143e373">

Action

</th></tr></thead><tbody><tr><td id="d127143e379">

**Enrollment account**

</td><td>

Select an existing account.

</td></tr><tr><td id="d127143e388">

**Create and add a new single account**

</td><td>

1.  Select the Create new enrollment account icon \(![Create new enrollment account icon](../../../reuse/icons/product-icons/plus-outline-24.svg)\).
2.  Select **Single account**.
3.  In the **Account name** field, enter the account name.
4.  In the **Display name** field, enter the display name.
5.  Search for and select the Tenant name.
6.  Select **Add**.


</td></tr><tr><td id="d127143e437">

**Create and add new bulk accounts**

</td><td>

1.  Select the Create new enrollment account icon \(![Create new enrollment account icon](../../../reuse/icons/product-icons/plus-outline-24.svg)\).
2.  Select **Bulk upload**.
3.  Search for and select the Tenant name.
4.  Below the **Enter API response** field, select the link [Azure playground](https://learn.microsoft.com/en-us/rest/api/billing/enrollment-accounts/list-by-billing-account?view=rest-billing-2024-04-01&tabs=HTTP#code-try-0).
5.  Sign in to your Azure portal.
6.  From the Azure portal, copy the sample JSON response that appears under the **EnrollmentAccountsListByBillingAccount** section.
7.  In the Cloud Account Management application, paste the sample JSON response in the **Enter API response** field.
8.  Select **Add**.


</td></tr></tbody>
</table>7.  Provide a comment.

    1.  In the **Work notes** section, enter your comments in the **Comments** text field.

    2.  Select **Post Comment**.

8.  At the top-right corner of the screen, select **Provision**.

9.  In the dialog box, confirm the provisioning request by selecting **Yes**.


## Result

Based on the defined context, Cloud Account Management creates a subscription account within the specified cloud organization and AWS organization unit or Azure management group.

