---
title: Getting started with ICAP DLP integration for Data Loss Prevention
description: Before you can use the integration, you must download it from the ServiceNow Store
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Getting started with ICAP DLP integration for Data Loss Prevention

Before you can use the integration, you must download it from the ServiceNow® Store

## Checklist

Review the following information before you start setting up your provider ICAP DLP integration for data loss prevention.

<table id="table_iz3_5mh_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify you have assigned the required ServiceNow AI Platform, Data Loss Prevention Application application roles.

</td><td>

Following roles are used across the ICAP DLP integration on the ServiceNow AI Platform: -   The Administrator \(admin\) install the applications from the ServiceNow® Store and assigns the Data Loss Prevention admin \(sn\_dlir.admin\).
-   The user with sn\_dlir.admin role can configure the integration and setup the incident profiles.
-   The users with sn\_dlir.analyst role will have read roles across the integration configurations.

</td></tr><tr><td>

Verify you have assigned the required Amazon S3 bucket policies.

</td><td>

You can follow the official AWS documentation for creating and managing IAM users, policies, and permissions through the following links:-   [Creating an IAM User](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html)
-   [Creating IAM Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_create-console.html)
-   [Amazon S3 Permissions](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security-iam.html)

**Note:** Using the above links, you can learn more on the detailed instructions and further options for managing IAM users and S3 permissions in AWS, also how to create an IAM user in your AWS account - AWS Identity and Access Management, and the basic overview of the process used to create an IAM user and credentials in AWS Identity and Access Management.

</td></tr><tr><td>

Verify that ServiceNow® core application that is required to support the ICAP DLP integration are installed and activated.

</td><td>

Verify that the following DLP applications and security support common applications are installed and activated from ServiceNow Store. If not installed, install, and activate on application.-   Security Support Common
-   Security Case Management common workspace components.
-   Data Loss Prevention Incident Response

</td></tr></tbody>
</table>**Parent Topic:**[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](icap-dlp-integration.md)

