---
title: Install and configure the ServiceNow application for the IBM QRadar offense ingestion integration
description: Before you run the integration on your ServiceNow AI Platform instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the ServiceNow application for the IBM QRadar offense ingestion integration

Before you run the integration on your ServiceNow AI Platform® instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If you have not installed the IBM QRadar application from the ServiceNow Store for the integration, see [Install a Security Operations integration](../../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After you have successfully installed the application, navigate to **Integrations** &gt; **Integrations Configurations** and locate the IBM QRadar tile.

3.  To configure the application, click **New**.

4.  Alternatively, if a **Configure** button is displayed on a tile, click it to edit an existing configuration.

5.  In the **Offense Ingestions Configuration** dialog that is displayed, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d216230e158">

Field

</th><th align="left" id="d216230e161">

Description

</th></tr></thead><tbody><tr><td id="d216230e167">

**Name**

</td><td>

Name of the IBM QRadar console or the IBM QRadar instance used for the integration.Spaces are supported for names, but parentheses are not supported.

</td></tr><tr><td id="d216230e185">

**IBM QRadar API Base URL**

</td><td>

Host URL for your IBM QRadar instance.**Note:** You need to enter only the URL and the port number here. For example, https://ibm-qradar.com:8443. If the port number is 443, it need not be explicitly entered.

</td></tr><tr><td id="d216230e200">

**IBM QRadar Dashboard URL**

</td><td>

The URL for the IBM QRadar dashboard or the console. This URL is used to auto construct the hyperlinks for offenses in the IBM QRadar dashboard. Enter only the host URL, for example, https://qradar.com. Do not include the .jsp in the URL, for example, https://qradar.com/console/qradar/jsp/QRadar.jsp is an invalid format.

 **Note:** If the dashboard URL is not available, enter the IBM QRadar API Base URL here.

</td></tr><tr><td id="d216230e224">

**IBM QRadar API Version**

</td><td>

Version 10 and above are supported.

</td></tr><tr><td id="d216230e237">

**IBM QRadar API Authorized Service Token \(on premises\)**

</td><td>

The IBM QRadar authorized service token is used for authentication. The authorized service token must have the following minimum user roles: **Offenses**, **Log Activity**, and **Network Activity** along with a user security profile that has no restrictions. To generate the authorized service token, follow these steps:

-   In the IBM QRadar console, navigate to the **Admin** tab and click **Authorized Services**.
-   If a valid authorized service token exists, check the expiry date and use this token.
 If an authorized service token is not available, follow these steps:

-   In the IBM QRadar, navigate to the **Admin** tab and click **Authorized Service**.
-   Click **Add Authorized Service** and create a token with the user role and security profile. Ensure that you specify an expiry date for a long validity period.


</td></tr><tr><td id="d216230e305">

**IBM QRadar API Authorized Service Token \(for QRoC\)**

</td><td>

If you are using IBM QRadar on Cloud \(QRoC\), use the self service application to generate the authorized service token with admin user role and admin security profile for authentication.

</td></tr><tr><td id="d216230e317">

**On Premises Deployment**

</td><td>

Default is disabled. If this option is enabled, you must specify a MID Application Name.

 If you are using IBM QRadar on Cloud \(QRoC\), verify that the check box is cleared.

</td></tr><tr><td id="d216230e335">

**MID Application Name**

</td><td>

Specify a MID Server Application that is set up in your environment. If you do not have a Mid Server Application configured,you must create a new MID Server application for this integration. **Note:** The MID Server Application can be configured only by users with system administrator role.

</td></tr></tbody>
</table>    ![Minimum User Roles](../image/ibm-qradar-min-roles.png "Minimum User Roles")

    To create a new MID Server Application, follow these steps:

    -   Navigate to **MID Server** &gt; **Applications** and click **New**.
    -   Enter a name for the MID Server Application and select a MID Server to be used as the default.
    -   Deselect the Included in application ALL check box and click **Save**.

        ![IBM QRadar: Configure MID server](../image/ibm-qradar-config-midserver.png)

    -   Click **Edit**. In the **Edit Members** page, select all available MID Servers, move them to the MID Servers List, and click **Save**. Depending on the availability, one of the MID Servers configured with the MID Server Application will be used.
6.  Enter the configuration details and specify the MID Server Application you have created.

    ![IBM QRadar: configuration tile](../image/ibm-qradar-config-tile.png)

    The source that you configure on the **IBM QRadar Offense Ingestion Configuration** form can be reused for multiple ServiceNow AI Platform profiles as long as each profile ingests offenses.

7.  Click **Submit**.

    After it is successfully validated and submitted, each IBM QRadar server configuration is saved on the Security Integrations page as a tile. If your saved configuration tiles are not displayed on the Security Integrations page, on the top right corner of the page, from the Show Configurations choice list, click **Yes**.

    **Note:** If you encounter some issues with the IBM QRadar domain segmentation feature, contact IBM QRadar Customer Support for assistance.


## What to do next

You have successfully installed and configured the application. The next step is to create the profile.

