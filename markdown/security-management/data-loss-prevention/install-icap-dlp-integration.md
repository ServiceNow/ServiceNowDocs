---
title: Install and configure the ICAP DLP integration
description: Install and configure the  provider ICAP DLP integration from the  ServiceNow Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  provider ICAP DLP incident data.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Install and configure the ICAP DLP integration

Install and configure the  provider ICAP DLP integration from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  provider ICAP DLP incident data.

## Before you begin

Role required: sn\_dlir.admin

## Procedure

1.  Download the  provider ICAP DLP integration from the  ServiceNow® Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations ** &gt; **Integration Configurations**.

3.  Search for the  DLP Incident Response Integration with ICAP tile and click  **Configure**.

    ![Click configure button for ICAP.](../image/install-config-tile.png)

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Region Name|Region name of the Amazon S3 bucket name.|
    |Transaction Data Bucket Name|Transaction data bucket name is the bucket where a DLP violation transaction has occurred.|
    |Evidence File Bucket Name|Evidence file bucket name is the bucket where you can find the DLP file that caused the violation.|
    |Access Key|AWS IAM access key for the ICAP configuration.|
    |Secret Key|AWS IAM secret key for the ICAP configuration.|

    ![Configure the DLP Incident Response integration with ICAP.](../image/dlp-icap-config.png)

5.  Click **Submit**.


## Result

**Note:** Please connect ICAP sub prod to the ServiceNow sub prod. Keep all the username and passwords in sync across the instances to avoid accounts getting logged out.

After you successfully validate and submit the configuration, the ICAP DLP Integration configurations is saved.

**Parent Topic:**[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](icap-dlp-integration.md)

