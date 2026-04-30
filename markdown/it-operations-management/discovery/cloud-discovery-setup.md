---
title: Cloud discovery setup using Discovery Home
description: Get started with Cloud Discovery by configuring credentials, service accounts, schedules, and MID Servers.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud discovery setup using Discovery Home

Get started with Cloud Discovery by configuring credentials, service accounts, schedules, and MID Servers.

Setting up Cloud Discovery is the first stage in performing cloud discovery and using Cloud Provisioning and Governance for managing discovered cloud resources.

Cloud Discovery is part of the ServiceNow AI Platform and deploys some of its platform-wide mechanisms and features. At the same time, there are some configurations that are specific to Cloud Discovery only.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

Perform the following tasks in the exact order they are listed below:

1.  Evaluate your cloud deployment and plan how you are going to discover it.
2.  [Request Discovery](../task/t_ActivateTheDiscoveryPlugin.md).
3.  [Install and configure the MID Servers](../../it-operations-management/task/mid-server-configuration-cloud.md).
4.  Set up service accounts and configure access to them.
    -   [Setting up AWS service accounts](../../it-operations-management/concept/setup-aws-service-accounts.md)
    -   [Create Azure service accounts](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md)
    -   [Create GCP service accounts](../../cloud-management-v2-setup/task/gcp-first-cld-and-srvc-accts.md)
    -   [Create VMware service accounts](../../cloud-management-v2-setup/task/vmware-create-creds-cloud-mgt.md)
    -   [Set up Alibaba Cloud service accounts](../task/set-up-alibaba-cloud-service-account.md)
5.  For Amazon AWS Cloud and Microsoft Azure Cloud, configure notifications and alerts from the Amazon AWS Cloud and Microsoft Azure Cloud to make the necessary updates to your CMDB without additional scanning.

    -   [Configure the AWS Config service to send event notifications to the ServiceNow instance](../../it-operations-management/task/aws-config-service-cloud-mgt.md)
    -   [Configure the Microsoft Azure Alert service to auto-update the CMDB](../../it-operations-management/concept/microsoft-azure-alert-driven-discovery.md#)
    -   [Configure the Google Cloud Logging service to auto-update the CMDB](../../it-operations-management/task/gcp-stackdriver-service.md)
    -   [Configure the VMware Events service to auto-update the CMDB](../../it-operations-management/task/vmware-events-service-cloud-mgt.md)
    **Note:** Event-driven discovery does not require Cloud Provisioning and Governance.

6.  Ensure that your ServiceNow instance has the relevant patterns and CI classes \(types\) for cloud resources. You may need to deploy the latest version of the following applications from the ServiceNow Store.
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
7.  [Create Discovery schedules for cloud resources](discovery-manager.md#).

