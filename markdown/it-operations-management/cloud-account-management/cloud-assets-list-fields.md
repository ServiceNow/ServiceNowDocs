---
title: Cloud assets list fields
description: Field descriptions for the All compute assets list in Cloud Asset Explorer, which displays cloud resources discovered across connected cloud providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/cloud-assets-list-fields.html
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: reference
last_updated: "2026-06-12"
reading_time_minutes: 1
breadcrumb: [Viewing cloud assets, Viewing Cloud Account Management dashboards, Using Cloud Account Management in Cloud Workspace, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud assets list fields

Field descriptions for the All compute assets list in Cloud Asset Explorer, which displays cloud resources discovered across connected cloud providers.

|Field|Description|
|-----|-----------|
|**Name**|Unique identifier or name of the compute asset as registered with the cloud provider.|
|**Provider**|Cloud provider hosting the asset, such as AWS, Azure, GCP, or OCI.|
|**Region**|Geographic region where the cloud provider hosts the asset.|
|**Cloud account**|Cloud provider account associated with the asset.|
|**Install status**|Current installation state of the asset, such as **Installed**.|
|**Owner**|User or team responsible for the asset.|
|**Security Findings**|Number of security findings detected for the asset.|
|**First discovered**|Date and timestamp when the system first discovered the asset.|
|**Last discovered**|Date and timestamp of the most recent discovery scan that detected the asset.|
|**Last ownership attestation**|Date and timestamp of the most recent ownership attestation completed for the asset.|
|**Cost center**|Cost center assigned to the asset for financial tracking and chargeback purposes.|

**Note:** Duplicate LDC entries no longer appear in the **Region** filter. After upgrading your instance to the latest version, the **Region** filter may be empty until the background job completes its initial run. Depending on data volume, this can take several hours. The job runs approximately every 30 minutes automatically.

