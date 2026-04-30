---
title: Create a record of Microsoft Azure credentials in Cloud Cost Management
description: Securely store your Microsoft Azure credentials in the ServiceNow AI Platform credentials store. You must create a service account that accepts billing data for Cloud Cost Management.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configure, Cloud Cost Management, IT Asset Management]
---

# Create a record of Microsoft Azure credentials in Cloud Cost Management

Securely store your Microsoft Azure credentials in the ServiceNow AI Platform credentials store. You must create a service account that accepts billing data for Cloud Cost Management.

## Before you begin

Role required: sn\_clin\_core.insights\_admin or admin

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Credentials**.

2.  On the Cloud API credentials page, select **Azure service principal**.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_xbf_4ky_szb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the service principal to register with the instance. For example, `CloudInsights-SP`.

</td></tr><tr><td>

Tenant ID

</td><td>

An unique identifier or alias for the tenant.Copy and paste the Tenant ID value from the `Azure-Credentials.txt` file.

</td></tr><tr><td>

Client ID

</td><td>

Unique identifier of an application created in Active Directory.Copy and paste the Tenant ID value from the `Azure-Credentials.txt` file.

</td></tr><tr><td>

Authentication Method

</td><td>

Select **Client Secret**.The Secret key field appears when you select Client Secret.

**Note:** Client Assertion isn’t supported.

</td></tr><tr><td>

Secret key

</td><td>

Azure client secret key.Copy and paste the Tenant ID value from the `Azure-Credentials.txt` file.

</td></tr><tr><td>

Active

</td><td>

Option to enable the credentials for use.

</td></tr></tbody>
</table>5.  Select **Save**.


## What to do next

[Schedule and manage the jobs that download Azure billing data](schedule-azure-billing-job.md)

