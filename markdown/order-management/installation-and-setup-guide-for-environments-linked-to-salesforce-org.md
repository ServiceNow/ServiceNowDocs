---
title: Installation and setup guide for environments linked to Salesforce orgs
description: Step-by-step instructions for setting up CPQ in an environment linked to a Salesforce org.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Installation and setup guide for environments linked to Salesforce orgs

Step-by-step instructions for setting up CPQ in an environment linked to a Salesforce org.

## Before you begin

Provide the username of a user in the org who will serve as the first CPQ admin user. This user will need to grant other users access after they have attempted to access the CPQ Admin once and appear in the User Access list of users. For more information, see [User access](please_share_your_feedback_on_admin_assist_responses.md).

Provide CPQ Support with the following information:

-   The Org ID of your org \(found in Setup &gt; Company Information\)
-   the My Domain URL of the org \(found in Setup &gt; My Domain\)

The CPQ DevOps team will provision the environment. Once ready, Support will confirm with your CPQ custom URL.

**Note:** If your Salesforce site was refreshed from another previously CPQ connected Salesforce site, uninstall the CPQ connected app before continuing. It holds metadata associated with the CPQ environment connected to the original Salesforce site. To uninstall, navigate to Setup &gt; Manage Connected Apps &gt; **Logik Connected App** &gt; Uninstall.

![Connected applications screen](../images/cpq-manage-connected-apps-uninstall.png)

Role required: Admin

## About this task

If your environment has never had CPQ installed, start at step 1. If you are upgrading existing packages, start at step 7.

## Procedure

1.  Navigate to your CPQ custom URL, and click the Settings tab in the navigation menu.

2.  Create a Refresh Token user name.

    The user name can be any userʼs username, but CPQ recommends a user with a system administrator profile.

3.  When prompted in the pop-up window, allow access for the CPQ API User connected app.

    If you are using an integration user that is not a system Admin, the following are the necessary requirements for the integration user \(or a permission set associated with that user/profile\):

    -   The user must be API enabled
    -   The user will need Create and Edit access for the following objects:
        -   LGK\_\_ConfigurationLineItem\_\_c
        -   LGK\_\_ConfigurationFieldData\_\_c
        -   SBQQ\_\_QuoteLine\_\_c
    -   The user will need Read/View All access to the following objects:
        -   Product2
        -   Pricebook2
        -   PricebookEntry
    -   For subscription management, the user with also need Read/View All access to the ProductSellingModel object.
4.  In a new browser, navigate to your CPQ custom URL again and confirm that the Refresh Token user name was updated correctly.

5.  Click reset again to obtain a new refreshToken, or navigate to https://&lt;YourLogikURL&gt;/refreshToken.

6.  Enter Salesforce setup, and search in the Quick Find box for Connected Apps oAuth Usage.

    1.  Find the Logik Connected App and click **Install**.

    2.  Click **Allow**.

    3.  Edit oAuth policies.

        Permitted users should be set to **Admin approved users are pre-authorized**.

    4.  Scroll to Manage Profiles, and link to the system administrator profile or any other profiles that will be using CPQ as an admin.

7.  Click the gear icon in the upper right and go into the “Setup” page for your SFDC org.

    If you are upgrading the Logik Base Managed Package from one major version to a newer major version, \(for example, from 1.x to 2.x\), please submit a support case noting this. CPQ needs to update the package version for your environment in our database.

8.  Navigate to Installed Packages.

    If you are only upgrading your existing CPQ packages, this is the only step you must complete.

    1.  Install the Logik Base Managed Package and select **Install for All Users**.

        -   If your org logs in through test.salesforce.com or has sandbox in the My Domain URL of the org, click [here](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDm000000cYuyIAE).
        -   If your org logs in through login.salesforce.com, click [here](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tDm000000cYuyIAE).
        The installation key is `Logik.io-2025!`

    2.  If using with Salesforce CPQ, ensure that Salesforce CPQ is installed and is version 244.2 or later, install the CPQ Extension for Salesforce CPQ package.

        -   If your org logs in through test.salesforce.com or has sandbox in the My Domain URL of the org, click [here](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDm000000cYvDIAU).
        -   If your org logs in through login.salesforce.com, click [here](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tDm000000cYvDIAU).
        The installation key is `Logik.io-2025!`

9.  For CPQ usage, navigate to Installed Packages again.

    1.  Find Salesforce CPQ and click **Configure**.

    2.  In Additional Settings &gt; External Configurator URL, update to `https://<YourLogikURL>/ui/configure`, and click **Save**.

    3.  Check the box next to Third Party Configurator, and click **Save**.

10. Add your domain \(https://&lt;YourLogikURL&gt;\) to the 'Logik.io Admin Custom Settings' object in Salesforce.

    If needed, set a runtime client token to use Logik with the Salesforce Partner Community.

11. Click **Save**.

12. For CPQ usage: Navigate to “App Manager” and find Salesforce CPQ/CPQ/QuoteQuickly.

    This item can have different names depending on your org settings.

    1.  Open the dropdown menu on the right and click `Edit`.

    2.  In Available Tabs, find “Configuration Line Items” and “Configuration Field Data Sets”, and add them to Selected Tabs.

        If desired, adjust the order of Selected Tabs to make them more easily accessible.

    3.  Save.

13. Navigate to “Trusted URLs” and click **New Trusted URL**.

    Give the new URL the following settings, and then click **Save**.

    -   In the API Name section, give the URL a name, such as "ServiceNow CPQ." \(It can be any name so long as you can reference it later.\)
    -   Add your domain to the URL section. \(If you want to make sure this setting retain access after an SFDC refresh, enter `https://*logik.io` to ensure that any logik.io site is trusted.
    -   Check `Active`.
    -   Set the CSP Context to **All**.
    -   In CSP Directives, check the **frame-src \(iframe content\)** and **img-src \(images\)** options.
14. Go to the Object Manager and use the Quick Find box in the top right to search for the Product object, and select the option whose API name is Product2.

    1.  Navigate to Page Layouts and click **Page Layout Assignments**.

    2.  Find the page layout assigned to system administrator or other profiles needing CPQ Admin access \(as determined when setting up Logik Connected App above\).

    3.  Select the page layout assigned to the system administrator.

    4.  Drag **View Logik.io Setup** and **Logik.io Enabled** to the desired section of the page layout \(usually the top\).

15. Navigate to Salesforce CPQ to confirm that the new tabs are visible.

16. In the Product tab, confirm that there is a new view called **Logik.io View**.

17. Test by creating or editing a product and checking **Logik.io Enabled** box, checking **Active Box**, and then saving and assigning it a Price Book entry.

    -   On the new product’s detail page, follow the Click Here link under **View Logik.io Setup** to ensure access to CPQ Admin.
    -   If you receive the error "Cannot get Configurable Product. Product &lt;ProductId&gt; is not available in cache" when you try to access a configurable product, you may have skipped the refresh token user setup at the top of this page. Create the user and try again.
    -   If you are able, please grant CPQ a user with the email address of provisioning@logik.io and we can verify the setup once you have completed it.

-   If you receive the error "Cannot get Configurable Product. Product &lt;ID&gt; is not available in cache" when you try to access a configurable product, you may have skipped step 2 to create a Refresh Token user name. Repeat step 2.
-   If you receive an "OAuth Error" with the code OAUTH\_APPROVAL\_ERROR\_GENERIC when you try to access your Logik URL, your user is blocked by recent changes Salesforce has made to connected apps. To resolve the problem, add the following text to your Salesforce My Domain URL, and then click **Allow**:

    -   For the Logik Connected App:

        ```
        /identity/app/AppInstallApprovalPage.apexp?app_id=0Ci5e000000bn6b&app_org_id=00D5e000005AHE7
        ```

    -   For the Logik API User Connected App:

        ```
        /identity/app/AppInstallApprovalPage.apexp?app_id=0Ci5e000000L18c&app_org_id=00D5e000005AHE7
        ```

    You are then able to follow the complete installation instructions.


