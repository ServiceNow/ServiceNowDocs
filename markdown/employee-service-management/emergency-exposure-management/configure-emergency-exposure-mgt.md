---
title: Configure Microsoft Office 365 for Emergency Exposure Management
description: Configure Emergency Exposure Management by setting the application system properties. If you want to search by Microsoft Office 365 meeting information, you also must register the Microsoft application and configure it.
locale: en-US
release: xanadu
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Emergency Exposure Management, Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Office 365 for Emergency Exposure Management

Configure Emergency Exposure Management by setting the application system properties. If you want to search by Microsoft Office 365 meeting information, you also must register the Microsoft application and configure it.

## Before you begin

**Important:**

If you are an on-premise customer with Microsoft Office 365 and you need assistance in configuring Emergency Exposure Management, contact your sales representative or contact Customer Service and Support at [https://support.servicenow.com/now?draw=case](https://support.servicenow.com/now?draw=case).

Role required: admin

## Procedure

1.  Register the Microsoft application.

    1.  Sign in to your Azure portal.

    2.  In the left navigation pane, select **Azure Active Directory**.

    3.  Under **Create**, select **App registration**.

    4.  On the form, fill in these fields.

        |Field|Value|
        |-----|-----|
        |Name|The name for the application.|
        |Supported account types|Select the first option: Accounts in this organizational directory only|

        The app is created with unique credentials to use.

2.  Add permissions to the Microsoft application to read employee calendars.

    1.  In the left navigation pane, select **API permissions**.

    2.  Click **Add a Permission**.

    3.  In the Request API permissions pane, under **Commonly used Microsoft APIs**, select **Microsoft Graph**.

    4.  Click **Application Permissions**.

    5.  Under **Calendars**, select **Calendars.Calendars read**.

    6.  Click **Add permissions**.

    7.  Click **Delegated Permissions**.

    8.  Under **Calendars**, select **Calendars.Calendars read**.

    9.  Click **Add permissions**.

    10. On the Configured permissions screen, click **Grant admin consent**.

3.  Obtain a trusted SSL certificate following your company’s procedure.

    For information about adding a TLS/SSL certificate in Microsoft Azure App Service, refer to [Add SSL Cert](https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-certificate) in the Microsoft Azure App Service Documentation guide.

4.  In the Azure portal, upload the certificate.

    1.  Access your Azure portal.

    2.  In the left navigation pane, select **Certificates and Secrets**.

    3.  Select **Upload certificate** and upload the certificate created in step [3](configure-emergency-exposure-mgt.md#generate-cert).

5.  Create a Java Key Store certificate in your ServiceNow instance.

    1.  Navigate to **System Definition** &gt; **Certificates**.

    2.  Click **New** and create a new certificate with a **Type** value of **Java Key Store**.

    3.  Set the **Short Description** text to the alias used in [3](configure-emergency-exposure-mgt.md#generate-cert).

    4.  Set the **Keystore Password** to the password used in step [3](configure-emergency-exposure-mgt.md#generate-cert).

    5.  Attach the `keystore.jks` certificate exported in step [3](configure-emergency-exposure-mgt.md#generate-cert).

6.  In your ServiceNow instance, set system properties for Emergency Exposure Management.

    1.  Navigate to **Emergency Exposure Management** &gt; **Properties**.

    2.  Verify the values or modify them for your environment.

    3.  Add these required properties.

        -   Client ID
        -   Tenant ID
        -   Certificate – The sys\_id of the certificate created in Step [5](configure-emergency-exposure-mgt.md#keystore-cert).
        -   Private key – Use the password used to generate the keystore in Step [3](configure-emergency-exposure-mgt.md#generate-cert).
        -   \(Optional\) Location – Location accessible from tables, such as a floor or building.
    4.  Verify that the Microsoft URL for token generation is correct for your organization.

    5.  Click **Save**.


