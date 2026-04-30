---
title: Install Unified Security Exposure Management
description: Before you run the Unified Security Exposure Management application in your ServiceNow AI Platform instance, you must get entitlement and download the application from the ServiceNow Store, install it on your ServiceNow AI Platform instance, and complete a few installation steps in Setup Assistant.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Installing Security Exposure Management Workspace applications, Implement, Unified Security Exposure Management, Security Operations]
---

# Install Unified Security Exposure Management

Before you run the Unified Security Exposure Management application in your ServiceNow AI Platform instance, you must get entitlement and download the application from the ServiceNow Store, install it on your ServiceNow AI Platform instance, and complete a few installation steps in Setup Assistant.

## Before you begin

**Note:** This process applies only to applications that are downloaded to production instances. If you're downloading applications to non-production or development instances, it's not necessary to get entitlements. Proceed to [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

-   Verify that you have the required ServiceNow roles assigned for your instance.
-   The admin role is required for installation and assigning roles.

**Important:** Unified Security Exposure Management \(USEM\) is a major architectural upgrade to Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a successful upgrade.

For detailed information, refer [KB2556844](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556844) and [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](../../vulnerability-response/concept/migrating-to-usem.md) before proceeding.

Role required: admin

## Procedure

1.  To get entitlement and download the Unified Security Exposure Management core application, navigate to the ServiceNow Store.

2.  In the upper right of the page, click **Log In**.

3.  In the dialog that is displayed, enter your Now Support credentials and click **Login**.

4.  On the page that is displayed, if not selected, click the **ServiceNow Products** tab.

5.  To view the associated applications that you are eligible for with the Unified Security Exposure Management application, on the product list page, click the **Unified Security Exposure Management** product.

    The Eligible tab lists all the applications you are eligible for if you opt-in. For more information on an application, click a link.

6.  To get the Unified Security Exposure Management application, click **Opt-in**.

7.  To agree to the terms and conditions, at the prompt, select the check box and click **Accept**.

    A message is displayed that indicates you have successfully opted-in for the application. With the ServiceNow Products tab selected and displayed, a green check mark replaces the plus sign to the right of the Unified Security Exposure Management application.After you have accepted the terms and conditions and managed entitlements for any of the applications on the **ServiceNow Products** tab, on the Products List page, you can click the plus sign \(+\) to get entitlement and opt-in for the other applications on this page with a single click.

8.  Skip to step 10 to install the application on your ServiceNow AI Platform instance.

9.  Alternatively, to manage your entitlement for the Unified Security Exposure Management application on other ServiceNow AI Platform instances, follow these steps.

    1.  If the Manage Entitlement button is not displayed, click the Unified Security Exposure Management application on the Product List to display it.

    2.  With the Eligible tab selected, click **Manage Entitlement**.

    3.  In the Manage Entitlements for USEM dialog that is displayed, choose one.

    4.  Click **OK** or **Cancel** to continue.

        You are ready to activate plugins and install the application on your ServiceNow AI Platform instance\(s\).

10. Log in to the ServiceNow AI Platform instance that you want to install the Unified Security Exposure Management application on.

11. Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

12. From the applications listed, locate the Unified Security Exposure Management application, select a version from the choice list, and click **Install**.

    The Application installation dialog is displayed. Any dependencies that will be installed are displayed.

13. If you want demo data, select the Load demo data check box and click **Install**.

    **Note:** If you do not select the **Load demo data** check box, demo data is not available to install from the **Application Manager** later. For information on how to install or reinstall demo data after the initial installation, see the [Workaround to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0722909) article in the Now Support Knowledge Base.

    This installation may take some time. A message is displayed in the Install dialog after the application is successfully installed.

14. Click **Close**.

15. After installation is successfully completed, navigate to **Workspaces** &gt; **Security Exposure Management**.

16. Select **Administration**

17. Follow the instructions on the forms in each section.


