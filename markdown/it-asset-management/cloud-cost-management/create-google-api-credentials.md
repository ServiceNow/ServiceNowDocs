---
title: Create Google API credentials
description: To access data securely on your provider account, the Discovery process must be present with appropriate credentials.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up access to Google Cloud billing and usage data, Configure Cloud Cost Management for Google Cloud, Configure, Cloud Cost Management, IT Asset Management]
---

# Create Google API credentials

To access data securely on your provider account, the Discovery process must be present with appropriate credentials.

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or admin

## About this task

**Important:** This information applies to both the Cloud Cost Management and Cloud Insights Billing apps. All references to Cloud Cost Management also apply to Cloud Insights Billing.

## Procedure

1.  In Cloud Cost Management, navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Credentials**.

2.  Select **Google API credentials**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique and descriptive name for the Google Cloud credentials.|
    |Active|Option to use the credential.|
    |Type|Provider name, GCP.|
    |Applies to|Indicates the MID Servers. If all, type All MID Servers.|
    |EMail|Billing service account email.|
    |Secret Key|Secret key that you generated on the Google Cloud Console.|

5.  Select **Save**.


**Related topics**  


[Cloud credentials](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

