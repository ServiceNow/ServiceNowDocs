---
title: Quick start tests for Cloud Provisioning and Governance
description: Validate that Cloud Provisioning and Governance still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Quick start tests for Cloud Provisioning and Governance

Validate that Cloud Provisioning and Governance still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

## Cloud Provisioning and Governance

Cloud Provisioning and Governance quick start tests require activating the following Cloud Provisioning and Governance plugins:

-   Cloud Provisioning and Governance \(com.snc.cloud.mgmt\)
-   Domain Support- Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\)
-   Service Catalog- Domain Separation plugin \(glideapp.servicecatalog.domain\_separation\)

|Test|Description|Release version|
|----|-----------|---------------|
|CMP: Add Azure Credentials|Add Azure credentials by inserting the fields into the Credentials table.|Orlando|
|CMP: Azure Service Account|Add Azure service account by inserting the fields into the service account table.|Orlando|
|CMP: Update datacenter type|Update the Cloud Service account with the datacenter type.|Orlando|
|CMP: Creating Resource Group|Creating Resource Group to provision Azure stack via ARM Template.|Orlando|
|CMP: Create Azure Logical datacenter.|Create Azure Logical datacenter for provisioning resources.|Orlando|
|CMP: Create "Contains: Contained by" relationship.|Create "Contains: Contained by" relationship between Resource Group and Azure datacenter.|Orlando|
|CMP: Create 'Hosted on' relationship.|Create hosted on relationship between logical datacenter and Cloud Service account.|Orlando|
|CMP: Create Cloud Account|Create cloud account by inserting the fields into the cloud account table.|Orlando|
|CMP: Cloud account and Logical datacenter association|Create an association between CMP cloud account and Logical datacenter.|Orlando|
|CMP: Create Catalog Item|Create Cloud Catalog Item with ARM Template.|Orlando|
|CMP: Create template version.|Create Cloud Template Version for Cloud Catalog Item.|Orlando|
|CMP: ARM template body|Update Cloud Template Version with ARM template body.|Orlando|
|CMP: Open the 'ServiceNow Cloud Template Versions'|Open the 'ServiceNow Cloud Template Versions' GUI page.|Orlando|
|CMP: Activate Cloud Template Version|Activate Cloud Template Version to create resource block, blueprint, and catalog.|Orlando|
|CMP: Verify the Cloud Template Version.|Validate whether status is Success and state is active in the Cloud Template Version after Activation operation.|Orlando|
|CMP: Activate Cloud Catalog Item|Activate Cloud Catalog Item to display catalog order form to the cloud user.|Orlando|
|CMP: Add stack and resource group name in Catalog item|Set the default value for stack name and resource group in the catalog item.|Orlando|
|CMP: Verify whether stack is present|Validate whether stack is available with name "ATFARMStack".|Orlando|
|CMP: Open Cloud Catalog Item page|Open Cloud Catalog Item page in the Service Portal.|Orlando|
|CMP: Submit Catalog form|Submit the Catalog Form to start provisioning ARM stack.|Orlando|
|CMP: Verify whether stack status is active|Validate the status of a stack after provisioning the stack.|Orlando|
|CMP: Verify stack status after Day2 - Stop operation|Validate the status of the stack status changed from 'On' to 'Off' after the Stop operation.|Orlando|
|CMP: Verify stack status after Day2 - Start operation|Validate the status of the stack status changed from 'Off' to 'On' after the Start operation.|Orlando|
|CMP: Verify stack status after Day2 - Deprovision operation|Validate the status of the stack status changed from 'On' to 'Terminate' after the de-provisioning operation.|Orlando|

|Test|Description|Release version|
|----|-----------|---------------|
|CMP: Add AWS Credentials|Add AWS credentials by inserting the fields into the credential table.|Orlando|
|CMP: AWS Service Account|Add AWS service account by inserting the fields into the service account table.|Orlando|
|CMP: Update datacenter type|Update the cloud service account with the datacenter type.|Orlando|
|CMP: Create logical datacenter|Create Logical datacenter for provisioning the resources.|Orlando|
|CMP: Create hosted on relationship|Create hosted on relationship between logical datacenter and Cloud Service account.|Orlando|
|CMP: Create Cloud Account|Create cloud account by inserting the fields into the cloud account table.|Orlando|
|CMP: Cloud account and Logical datacenter association|Create an association between CMP cloud account and logical datacenter.|Orlando|
|CMP: Create Catalog Item|Create Cloud Catalog Item with the CFT Template.|Orlando|
|CMP: Create template version|Created Cloud Template Version for a Cloud Catalog Item.|Orlando|
|CMP: CFT template body|Update Cloud Template Version with the CFT template body.|Orlando|
|CMP: Open the ' ServiceNow Cloud Template Versions'|Open the ' ServiceNow Cloud Template Versions' GUI page.|Orlando|
|CMP: Activate Cloud Template Version|Activate Cloud Template Version to create resource block, blueprint, and catalog.|Orlando|
|CMP: Verify the Cloud Template Version|Validate the Cloud Template Version whether status is Success and state is active after Activation operation.|Orlando|
|CMP: Activate Cloud Catalog Item|Activate Cloud Catalog Item to display the catalog order form to the cloud user.|Orlando|
|CMP: Add stack name in Catalog item|Set the default value for stack name in the catalog item.|Orlando|
|CMP: Verify whether stack is present|Validate whether stack is available with name "ATFCFTStack".|Orlando|
|CMP: Open Cloud Catalog Item page|Open the Cloud Catalog Item page in the Service Portal.|Orlando|
|CMP: Submit Catalog form|Submit the Catalog Form to start provisioning CFT Stack.|Orlando|
|CMP: Verify whether stack status is active|Validate the status of the stack after provisioning the stack.|Orlando|
|CMP: Verify stack status after Day2 - Stop operation|Validate the status of the stack status changed from 'On' to 'Off' after the Stop operation.|Orlando|
|CMP: Verify stack status after Day2 - Start operation|Validate the status of the stack status changed from 'Off' to 'On' after the Start operation.|Orlando|
|CMP: Verify stack status after Day2 - De-provision operation|Validate the status of the stack status changed from 'On' to 'terminate' after the de-provisioning operation.|Orlando|

To learn more about Cloud Provisioning and Governance, see [Cloud Provisioning and Governance](../../../product/cloud-management-v2/concept/cloud-management-v2-landing-page.md).

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

