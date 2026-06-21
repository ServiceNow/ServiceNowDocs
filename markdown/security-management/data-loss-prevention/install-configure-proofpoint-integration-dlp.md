---
title: Install and configure the Proofpoint integration for Data Loss Prevention
description: Install and configure the  Proofpoint DLP integration from the  ServiceNow Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Proofpoint DLP incident data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/data-loss-prevention/install-configure-proofpoint-integration-dlp.html
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Install and configure the Proofpoint integration for Data Loss Prevention

Install and configure the  Proofpoint DLP integration from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Proofpoint DLP incident data.

## Before you begin

Role required: sn\_dlir.admin

## Procedure

1.  Download the  Proofpoint DLP integration from the  ServiceNow® Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations ** &gt; **Integration Configurations**.

3.  Search for the  `DLP Incident Response Integration with Proofpoint` tile, and click  **Configure**.

    \[Omitted image "dlp-proofpoint-tile.png"\] Alt text: Click Configure button for Proofpoint.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Proofpoint DLP integration configuration.|
    |Base URL|URL for the Proofpoint that serves as the REST endpoint.|
    |Tenant ID|The ID of Proofpoint tenant.|
    |Client ID|The ID of Proofpoint client to be used.|
    |Client Secret|The secret configured for your user account on Proofpoint.|

    \[Omitted image "dlp-proofpoint-config.png"\] Alt text: Configure the DLP Incident Response integration with Proofpoint.

    **Note:** For the existing customers, we continue to support Basic Authentication to ensure that the existing child tiles which have basic authentication function as expected. However, if a customer wishes to add OAuth to a child tile, they must not remove the existing Basic Authentication credentials \(username and password\). While they can replace these values with dummy entries, leaving the fields empty will prevent the tile from being submitted successfully.

5.  Update the Azure Storage Configuration.

    1.  In the Security Integrations page, search for **Azure Storage Configuration** tile.

    2.  In the Azure Storage Configuration tile, click **Update**.

        \[Omitted image "dlp-microsoft-azure-storage.png"\] Alt text: Click Update for Azure Storage Configuration.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the Azure Storage configuration.|
        |Storage Account Name|Storage account name created on Azure portal|
        |Container Name|Container name created in storage account on Azure portal.|
        |Shared Access Key|Shared access key for the Storage account.|

    4.  Click **Submit**.

    After you successfully validate and submit the configuration, the Azure Storage Configuration is saved on the Security Integrations page as a tile.

6.  Update the AWS Storage Configuration.

    1.  In the Security Integrations page, search for **AWS Storage Configuration** tile.

    2.  In the AWS Storage Configuration tile, click **Update**.

        \[Omitted image "dlp-microsoft-aws-storage.png"\] Alt text: Click Update for AWS Storage Configuration.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the AWS Storage configuration.|
        |Region Name|Region name of the AWS Storage account.|
        |Bucket Name|Bucket name created on the AWS portal.|
        |Access Key|Access key with read and write access.|
        |Secret Key|Secret key with read and write access.|

7.  Click **Submit**.


## Result

After you successfully validate and submit the configuration, the Proofpoint DLP Integration is saved on the Security Integrations page as a tile.

-   **[Create an Application in Proofpoint and Obtain Client Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/data-loss-prevention/create-application-proofpoint-dlp.md)**  
Create an Application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to Proofpoint's API for seamless integration and automation.
-   **[Configure the Webhook on the Proofpoint DLP tenant for alert notifications to ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/data-loss-prevention/configure-webhook-proofpoint-tenant-alert-notifications.md)**  
Configure a webhook on Proofpoint using the REST API endpoint to start getting the alerts from the Proofpoint DLP tenant. Your ServiceNow instance creates DLP incidents from these alerts. The Proofpoint DLP integration provides a REST API endpoint for end users to configure the webhook.

**Parent Topic:**[Data Loss Prevention Incident Response Integration with Proofpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/data-loss-prevention/dlp-incident-response-integration-proofpoint.md)

