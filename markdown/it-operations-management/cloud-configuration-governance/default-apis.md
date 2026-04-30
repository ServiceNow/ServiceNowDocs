---
title: Default CAPI APIs
description: Several CAPI APIs are provided by default with the Cloud Provisioning and Governance application.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Default CAPI APIs

Several CAPI APIs are provided by default with the Cloud Provisioning and Governance application.

CAPI APIs refer to the API records that link a CAPI product and a CAPI interface. They do not refer to the CAPI classes that you can call from MID Server script includes in CAPI APIs. For an overview of CAPI classes, see [CAPI classes in MID Server script includes](../concept/mid-server-script-includes.md).

View Cloud APIs by navigating to **Cloud API** &gt; **Library** in the base system instance interface, or by navigating to **Design** &gt; **Cloud API** in the Cloud Admin Portal.

![CAPI APIs](../image/capi-apis-nav.png "CAPI APIs")

**Note:** You can customize scripted connectors using MID Server script includes.

|API|Interface|Product|Scripted|
|---|---------|-------|--------|
|Ansible Tower Configuration API|Configuration Management Interface|Ansible-Tower|YES\*|
|AWS Auto Scaling API|Auto Scaling Interface|AWS Elastic Compute Cloud|YES\*|
|AWS Blob Storage API|Blob Storage Interface|AWS Simple Storage Service|NO|
|AWS Block Storage API|Block Storage Interface|AWS Elastic Block Storage|NO|
|AWS Compute API|Compute Interface|AWS Elastic Compute Cloud|NO|
|AWS Compute API|Compute Interface|AWS Elastic Compute Cloud|YES\*|
|AWS Load Balancer API|Load Balancer Interface|AWS Elastic Load Balancing|NO|
|AWS Network API|Network Interface|AWS Virtual Private Cloud|NO|
|AWS Stack Orchestration API|Stack Orchestration Interface|AWS CloudFormation|YES\*|
|Azure Alert API|Event Interface|Azure Alert|YES\*|
|Azure Blob Storage API|Blob Storage Interface|Microsoft.Storage|YES\*|
|Azure Block Storage API|Block Storage Interface|Microsoft.BlockStorage|YES\*|
|Azure Compute API|Compute Interface|Microsoft.Compute|YES\*|
|Azure Extensions API|Azure Extensions Interface|Microsoft.Compute|YES\*|
|Azure Load Balancer API|Load Balancer Interface|Microsoft.LoadBalancer|YES\*|
|Azure Network API|Network Interface|Microsoft.Network|YES\*|
|Azure Stack Orchestration API|Stack Orchestration Interface|Azure ARM|YES\*|
|Infoblox IPAM API|IPAM Interface|Infoblox|NO|
|ServiceNow Store IPAM API|IPAM Interface|ServiceNow|YES\*|
|SSH API|SSH Interface|SSH|NO|
|vSphere Block Storage API|Block Storage Interface|VMware VDisk|NO|
|vSphere Compute API|Compute Interface|VMware vSphere|NO|

\*You can customize how scripted APIs make REST calls to the cloud provider.

**Parent Topic:**[Cloud Provisioning and Governance](../concept/cloud-management-v2-landing-page.md)

