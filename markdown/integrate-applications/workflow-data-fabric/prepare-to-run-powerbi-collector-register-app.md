---
title: Register Power BI application
description: Register an application in Azure and create client credentials for Power BI collector authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector-register-app.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prepare to run the PowerBI collector, PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Register Power BI application

Register an application in Azure and create client credentials for Power BI collector authentication.

## Before you begin

Role required: admin

You must have permissions to register applications in Azure Active Directory.

## About this task

Register an application in Azure to obtain the client ID and client secret needed for Power BI collector authentication.

## Procedure

1.  Register a new application in Azure.

    1.  Navigate to the [Azure Portal](https://portal.azure.com).

    2.  Select **App Registrations** from Azure services.

    3.  Select **New Registration**.

    4.  Enter the registration information.

        -   Application Name: DataDotWorldPowerBIApplication
        -   Supported account types: Accounts in this organizational directory only
    5.  Select **Register** to complete the registration.

2.  Create a client secret.

    1.  On the application page, select **Certificates and Secrets**.

    2.  Select **New client secret**.

    3.  Add a description for the secret.

    4.  Select the desired expiration date.

    5.  Select **Add**.

    6.  Copy the secret value.

        Save this value securely. You will use it when configuring the Power BI collector.

3.  Get the client ID.

    1.  Select the **Overview** tab in the left sidebar of the application page.

    2.  Copy the Client ID from the Essentials section.

        Save this value. You will use it when configuring the Power BI collector.


**Parent Topic:**[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)

