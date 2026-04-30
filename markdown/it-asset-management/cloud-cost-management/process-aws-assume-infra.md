---
title: Processing AWS billing jobs with Assume role authentication
description: Use the Cloud Cost Management Infra Stack application to process and download the AWS billing files with Assume role authentication at a better speed.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up access to AWS billing and usage data, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Processing AWS billing jobs with Assume role authentication

Use the Cloud Cost Management Infra Stack application to process and download the AWS billing files with Assume role authentication at a better speed.

When you have installed the Cloud Cost Management Infra Stack application, the processing of all billing download jobs happens completely on the Kubernetes cluster. However, for AWS billing jobs with Assume role authentication the processing of billing data is partially done via Cloud Cost Management MID Server.

## AWS billing download job \(with Assume role\) workflow

1.  The Cloud Cost Management MID Server connects to AWS and downloads the billing data files.
2.  The billing data files are sent to Cloud Cost Management Glide as an attachment.

    **Note:** If the default configuration for maximum attachment size is changed and it’s less than the billing data file, it might have an impact on billing. To keep the default configuration or a value higher than the billing file size, see the knowledge base article [KB0718101](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0718101).

3.  The attachments are stored temporarily in the Attachment table in the Glide database.
4.  After all the attachments are stored in the Glide database, the Kubernetes job fetches details of the billing download jobs that are in the Requested state.

    **Note:** The temporary attachments are deleted from the Glide database after the billing job is completed.

5.  Kubernetes job fetches the attachment files from the Glide database via an API and processes the files on the Kubernetes cluster.
6.  The processed billing data is sent to Glide and finally stored in the Glide database.

For AWS Assume Role Billing Download, the Flow Launcher Job Configuration settings determine the parallel processing of multiple download threads. These settings are stored in the AWS Assume Role Billing Download record in the Flow Launcher Job Configuration \[sn\_cld\_intg\_core\_flow\_launcher\_job\_config\] table. The value in the Concurrency field of the AWS Assume Role Billing Download record is the number of billing files downloaded in parallel. Performance is optimal when the Concurrency field is set to the default value 2. However, if you experience any slowness, you can set the **Concurrency** field to **1** with the admin role.

