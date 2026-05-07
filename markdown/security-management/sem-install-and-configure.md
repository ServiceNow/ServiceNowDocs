---
title: Install Unified Security Exposure Management
description: Before you run the Unified Security Exposure Management application in your ServiceNow AI Platform instance, you must get entitlement and download the application from the ServiceNow Store and install it on your ServiceNow AI Platform instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 3
breadcrumb: [Installing Security Exposure Management Workspace applications, Implement, Unified Security Exposure Management, Security Operations]
---

# Install Unified Security Exposure Management

Before you run the Unified Security Exposure Management application in your ServiceNow AI Platform instance, you must get entitlement and download the application from the ServiceNow Store and install it on your ServiceNow AI Platform instance.

## Before you begin

**Note:** This process applies only to applications that are downloaded to production instances. If you're downloading applications to non-production or development instances, it's not necessary to get entitlements. Proceed to [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

-   Verify that you have the required ServiceNow roles assigned for your instance.
-   The admin role is required for installation and assigning roles.

**Important:** Unified Security Exposure Management \(USEM\) is a major architectural upgrade to Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a successful upgrade.

For detailed information, refer [KB2556844](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556844) and [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](../../vulnerability-response/concept/migrating-to-usem.md) before proceeding.

Role required: admin

## Procedure

1.  To get entitlement and download the Unified Security Exposure Management core application, navigate to the ServiceNow Store.

    In the ServiceNow Store, you must verify that you have entitlements \(or licenses\) to the application and its dependent applications. After you have logged in, you can use the menu in the upper right with your initials to manage entitlements and opt-in.

2.  In the upper right of the page, select **Log In**.

3.  In the dialog that is displayed, enter your Now Support credentials and select **Login**.

4.  On the page that is displayed, if not selected, select the **ServiceNow Products** tab.

5.  To view the associated applications that you're eligible for with the Unified Security Exposure Management application, on the product list page, select the **Unified Security Exposure Management** product.

6.  To get the Unified Security Exposure Management application, select **Opt-in**.

7.  Select **Request Install** to download the application.

8.  Log in to the ServiceNow AI Platform instance that you want to install the Unified Security Exposure Management application on.

9.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

10. From the applications listed, locate the Unified Security Exposure Management application, select a version from the list, and select **Install**.

    The Application installation dialog is displayed. Any dependencies that will be installed are displayed.

11. After installation is successfully completed, select **Close**.

12. Navigate to **Workspaces** &gt; **Security Exposure Management**.

13. Select **Administration**

14. Follow the instructions on the forms in each section.

    **Note:**

    If you want to use a version of a supported application that is compatible with Unified Security Exposure Management \(USEM\), see [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](../../vulnerability-response/concept/migrating-to-usem.md) for more information about USEM and the Unified Security Exposure Management migration.

    If you do not intend to upgrade to Unified Security Exposure Management, install a version that is lower than v30.x of an application and for upgrades to its supported third-party integration applications.


