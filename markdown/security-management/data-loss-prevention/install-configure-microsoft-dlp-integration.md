---
title: Install and configure the Microsoft DLP integration
description: Install and configure the  DLP Incident Response integration with Microsoft DLP from the  ServiceNow Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Microsoft DLP event data.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Install and configure the Microsoft DLP integration

Install and configure the  DLP Incident Response integration with Microsoft DLP from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Microsoft DLP event data.

## Before you begin

Role required: sn\_dlir.admin

## Procedure

1.  Download the  Microsoft DLP integration from the  ServiceNow® Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations ** &gt; **Integration Configurations**.

3.  Configure the Microsoft DLP integration.

    1.  Search for **DLP Incident Response Integration with Microsoft** tile and click  **Configure**.

        ![Click Configure for Microsoft.](../../data-loss-prevention/image/dlp-microsoft.png "DLP Incident Response Integration with Microsoft")

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the Microsoft DLP integration configuration.|
        |Client ID|Client ID of the app created on Microsoft Azure portal.|
        |Client Secret|Client Secret of the app created on Microsoft Azure portal.|
        |Tenant ID|Tenant ID of the user.|

    3.  Click **Submit**.

    After you successfully validate and submit the configuration, the Microsoft DLP Integration is saved on the Security Integrations page as a tile.

4.  Update the Azure Storage Configuration.

    1.  In the Security Integrations page, search for **Azure Storage Configuration** tile.

    2.  In the Azure Storage Configuration tile, click **Update**.

        ![Click Update for Azure Storage Configuration.](../../data-loss-prevention/image/dlp-microsoft-azure-storage.png)

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the Azure Storage configuration.|
        |Storage Account Name|Storage account name created on Azure portal|
        |Container Name|Container name created in storage account on Azure portal.|
        |Shared Access Key|Shared access key for the Storage account.|

    4.  Click **Submit**.

    After you successfully validate and submit the configuration, the Azure Storage Configuration is saved on the Security Integrations page as a tile.

5.  Update the AWS Storage Configuration.

    1.  In the Security Integrations page, search for **AWS Storage Configuration** tile.

    2.  In the AWS Storage Configuration tile, click **Update**.

        ![Click Update for AWS Storage Configuration.](../../data-loss-prevention/image/dlp-microsoft-aws-storage.png)

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the AWS Storage configuration.|
        |Region Name|Region name of the AWS Storage account.|
        |Bucket Name|Bucket name created on the AWS portal.|
        |Access Key|Access key with read, write, and delete access.|
        |Secret Key|Shared key with read, write, and delete access|

    4.  Click **Submit**.


## Result

After you successfully validate and submit the configuration, the AWS S3 Configuration is saved on the Security Integrations page as a tile.

**Parent Topic:**[Data Loss Prevention Incident Response with Microsoft](../concept/dlp-integration-microsoft.md)

