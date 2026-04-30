---
title: Get entitlement for a GRC product or application
description: The first step in installing an application is to verify that the application or the product and its associated applications have valid ServiceNow entitlements.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Download a GRC application from the ServiceNow Store for the first time, GRC and the ServiceNow Store, Governance, Risk, and Compliance]
---

# Get entitlement for a GRC product or application

The first step in installing an application is to verify that the application or the product and its associated applications have valid ServiceNow entitlements.

## Before you begin

Role required: admin

Individuals performing entitlement must have a Now Support account and have permission to request applications for the instances under consideration.

**Note:** This process applies only to applications downloaded to production instances. If you are downloading applications to sub-production or development instances, it is not necessary to get entitlements. Proceed to [Activate a ServiceNow Store application](https://www.servicenow.com/docs/access?context=activate-entitled-store-app&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

## Procedure

1.  Navigate to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

    ![ServiceNow Store Certified Apps screen](../../security-incident-response/image/store.png)

2.  Click **Login** and log in using your HI credentials.

3.  Click the **ServiceNow Products** tab to view all available ServiceNow products.

    Integrations and other types of content are shown on the **Certified Apps** tab.

    ![GRC applications on the ServiceNow Store](../image/grc-bearded-guy.png)

    **Note:** For the sake of this example, assume you are acquiring entitlement for the Risk Management product.

4.  Click the product name of the product you are getting entitlement to.

    All applications associated with the product you are entitling are listed. When you have obtained entitlement to the core product, the applications listed under it are also entitled.

    ![Risk Management products](../image/risk-mgmt-product-list.png)

5.  Click **Opt-in** to verify that you have entitlement to the product and the applications listed.

    You are prompted to read and accept the ServiceNow terms and conditions. ![Terms and Conditions](../../security-incident-response/image/terms-conditions.png)

6.  Select the check box and click **Accept**.

7.  Notice that a check mark appears next to the product name and the Manage Entitlements button appears.

    ![Manage entitlements for Risk Management](../image/risk-manage-entitlement.png)

    The check mark indicates that you have subscribed to the product and its associated applications. It is time to manage your entitlements. This is a one-time process for this product and any other products you want to install in the future.

8.  Click **Manage Entitlements** to change the instances affected by the applications to which you are entitled.

    ![Managing entitlements for your company](../image/grc-manage-entitlement-dialog.png)

9.  After you have agreed to the ServiceNow Terms and Conditions and managed entitlements, you can entitle other products by clicking the plus sign \(+\) next to the product name.

    **Note:** You are now ready to activate the product.


