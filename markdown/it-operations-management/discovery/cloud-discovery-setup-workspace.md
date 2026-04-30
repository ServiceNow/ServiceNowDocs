---
title: Cloud Discovery setup using Cloud Discovery Workspace
description: Perform the necessary procedures to prepare for discovering resource CIs on the cloud.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud Discovery setup using Cloud Discovery Workspace

Perform the necessary procedures to prepare for discovering resource CIs on the cloud.

Setting up Cloud Discovery is the first stage in performing cloud discovery and using Cloud Provisioning and Governance for managing discovered cloud resources.

Cloud Discovery is part of the ServiceNow AI Platform and deploys some of its platform-wide mechanisms and features. At the same time, there are some configurations that are specific to Cloud Discovery only.

Cloud Discovery Workspace present an enhanced way of creating discovery schedules. You can also check prerequisites required for discovering cloud resources, like credentials and service accounts.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

Perform the following tasks in the exact order they are listed below:

1.  Evaluate your cloud deployment and plan how you are going to discover it.
2.  [Request Discovery](../task/t_ActivateTheDiscoveryPlugin.md).
3.  [Install Cloud Discovery Workspace](../../cloud-operations-workspace/task/install-cloud-ops-wrksp.md).
4.  [Install and configure the MID Servers](../../it-operations-management/task/mid-server-configuration-cloud.md).
5.  \(For Amazon AWS Cloud and Microsoft Azure Cloud\) Configure notifications and alerts from the Amazon AWS Cloud and Microsoft Azure Cloud to make the necessary updates to your CMDB without additional scanning.

    -   [Configure the AWS Config service to send event notifications to the ServiceNow instance](../../it-operations-management/task/aws-config-service-cloud-mgt.md)
    -   [Configure the Microsoft Azure Alert service to auto-update the CMDB](../../it-operations-management/concept/microsoft-azure-alert-driven-discovery.md#)
    -   [Configure the Google Cloud Logging service to auto-update the CMDB](../../it-operations-management/task/gcp-stackdriver-service.md)
    -   [Configure the VMware Events service to auto-update the CMDB](../../it-operations-management/task/vmware-events-service-cloud-mgt.md)
    **Note:** Event-driven discovery does not require Cloud Provisioning and Governance.

6.  Ensure that your ServiceNow instance has the relevant patterns and CI classes \(types\) for cloud resources. You may need to deploy the latest version of the following applications from the ServiceNow Store.
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
7.  [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md).

**Related topics**  


[Cloud Discovery Workspace](../../cloud-operations-workspace/reference/cow-landing-page.md)

