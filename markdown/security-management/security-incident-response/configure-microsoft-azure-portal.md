---
title: Register and configure the Microsoft Azure portal
description: Register your application in the Microsoft Azure portal and grant your users with read and write access to the application.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Register and configure the Microsoft Azure portal

Register your application in the Microsoft Azure portal and grant your users with read and write access to the application.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration \(store link of the defender integration\) as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see XX.

Role required: Microsoft Azure application developer, Microsoft Azure tenant administrator

## Procedure

1.  Sign in to the Microsoft Azure portal.

2.  Search for and select **App registrations**.

3.  Click **New registration**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|User-facing display name for the application. For example, LogAnalyticsAPI.|
    |Supported account types|Account type that can use this application or access the API.|
    |Redirect URI|Redirect URI. The authentication response is directed to this URI after successfully authenticating a user.|

5.  Click **Register**.

    After you successfully register the application, you see the Overview page.

    ![Application overview page on Azure.](../image/sentinel_app_overview.png)

6.  Navigate to **Manage** &gt; **Certificates &amp; secrets**.

7.  In the Client secrets section, click **New client secret**.

    You can't view the client secret later, so make sure that you copy and save the client secret now at this step. If you forget the client secret, you can generate a new one by following the instructions in steps 4 and 5.

8.  Navigate to **Manage** &gt; **API permissions**.

9.  Click **Add a permission**.

10. In the Request API permissions window, click the **APIs my organization uses** tab.

11. Search and select **Log Analytics API** app name.

12. In the Log Analytics API permissions, select **Application permissions**.

    Enabling this permission ensures that the application runs as a background service or daemon without a signed-in user.

13. Under the Data section, select **Data.Read**

14. Click **Add Permissions**.

    The permissions are updated.

15. Enable the **Grant admin consent for Default Directory** option for the Data.Read API permission that you enabled in step 13.

16. Search for and select **Log Analytics workspaces**.

17. Select your Sentinel Log Analytics workspace.

    You now see the Sentinel Log Analytics workspace Overview page.

18. Navigate to **Access control \(IAM\)** &gt; **Role assignments**.

19. Click **Add**, and select **Add role assignment**.

20. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Role|Account type that can use this application. Select **Azure Sentinel Responder**.|
    |Assign access to|Permissions scope that you define. Select **User**, **group**, or **service principal**.|
    |Select|Application that you created earlier in step 4. For example, LogAnalyticsAPI.|

21. Click **Save**.


