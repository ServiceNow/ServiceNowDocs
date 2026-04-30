---
title: Register a new application at Azure portal for Microsoft Teams connections
description: Register a new application at Azure portal for Microsoft Teams integration and grant access to the Azure app.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate Major Security Incident Management with Microsoft Teams, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Register a new application at Azure portal for Microsoft Teams connections

Register a new application at Azure portal for Microsoft Teams integration and grant access to the Azure app.

## Before you begin

**Note:** If you want, you can use the same application that you created for SharePoint to establish the Microsoft Teams Graph connection.

Role required: admin, Azure admin

## Procedure

1.  Sign in to Azure portal using your Microsoft account.

2.  Navigate to **Azure Services** &gt; **Application Registration** &gt; **New Registration**.

3.  Enter name of the application.

    For example, Microsoft Teams Graph.

4.  Select **Supported account type: Accounts in this organizational directory only \(Service Now only - Single tenant\)**.

5.  Select **Web** type from drop down list under the Redirect URL.

6.  Enter ServiceNow AI Platform® instance redirect URL in the allowed redirect URL field.

    For example, `https://<<InstanceName>>.service-now.com/oauth_redirect.do`

7.  Click on **Register** and make sure the page is displayed with **Overview** section.

8.  Make a note of the Client ID and Tenant ID from the **Essentials** section in the **Overview** page.

9.  You can either follow Step 6.1 or Step 6.2 to complete the procedure of establishing a connection on your ServiceNow instance.


**Parent Topic:**[Integrate Major Security Incident Management with Microsoft Teams](../../secops-integration-major-security-incident-management/concept/integrate-teams-msim.md)

