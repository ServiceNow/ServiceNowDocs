---
title: Create GCP service accounts
description: Create Google Cloud Platform \(GCP\) service accounts on the ServiceNow AI Platform to access your GCP account during GCP discovery.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-06-29"
reading_time_minutes: 1
breadcrumb: [Set up Google Cloud Platform service accounts, Setting up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Create GCP service accounts

Create Google Cloud Platform \(GCP\) service accounts on the ServiceNow AI Platform to access your GCP account during GCP discovery.

## Before you begin

Verify that Google API credentials have been created. For more information, see [Configure the Google API credentials for Cloud Discovery](../../discovery/task/itom-create-google-api-credentials.md).

Retrieve the **project\_id** value from the JSON key file that is associated with the service account.

Role required: discovery\_admin

## Procedure

1.  In the navigation filter, enter `cmdb_ci_cloud_service_account.list`.

2.  Select **New**.

3.  In the **Discovery Credentials field**, begin to enter the credential name and select it from the list.

4.  On the form, fill in the remaining fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for the GCP service account.|
    |Account Id|GCP project ID.|
    |Datacenter URL|URL of the datacenter, which should remain empty.|
    |Datacenter Type|Type of the datacenter where the account is hosted, which should be Google Datacenter \[cmdb\_ci\_google\_datacenter\].|

5.  Select **Submit**.


## What to do next

Schedule a GCP cloud discovery. For more information, see [Create a discovery schedule in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md).

**Parent Topic:**[Set up Google Cloud Platform service accounts](../concept/set-up-gcp-service-accounts.md)

