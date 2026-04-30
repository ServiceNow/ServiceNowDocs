---
title: Exploring Cloud Configuration Governance
description: Understand the typical Cloud Configuration Governance workflow and high-level tasks.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Exploring Cloud Configuration Governance

Understand the typical Cloud Configuration Governance workflow and high-level tasks.

To use Cloud Configuration Governance for managing the configuration of the cloud resources, perform the following tasks:

1.  Install Cloud Configuration Governance. For more information, see [Install Cloud Configuration Governance](../task/install-cloud-config-governance.md).
2.  Install the CCG Content Pack to access the base system Cloud Configuration Governance contents. For more information, see [Install the CCG Content Pack](../task/install-ccg-content-pack.md).
3.  Assign Cloud Configuration Governance roles to users. For more information on the Cloud Configuration Governance roles, see [Cloud Configuration Governance roles and system properties](ccg-roles-and-system-properties.md).
4.  To manage the configuration of the Amazon Web Services \(AWS\) resources through Cloud Configuration Governance, see [Set up Cloud Configuration Governance for AWS](../task/set-up-ccg-for-aws.md).
5.  To manage the configuration of the Microsoft Azure resources through Cloud Configuration Governance, see [Set up Cloud Configuration Governance for Microsoft Azure](../task/set-up-ccg-for-azure.md).
6.  Create a scan configuration to scan the cloud resources against one or more policy sets and identify the policy violations. For more information, see [Create a scan configuration](../task/create-ccg-scan-configuration.md).
7.  Run the appropriate remediation action to fix the non-compliant cloud configuration identified during the scan run. For more information, see [Run remediation](../task/ccg-run-remediation.md).

## What to do next

See [Plugins or applications installed with ITOM Cloud Accelerate](../reference/plugin-app-cloud-accelerate.md) to find the list of plugins you activate with Cloud Configuration Governance.

-   **[Install Cloud Configuration Governance](../task/install-cloud-config-governance.md)**  
You can install the Cloud Configuration Governance application \(com.sn.itom.ccg\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they aren’t already installed.
-   **[Install the CCG Content Pack](../task/install-ccg-content-pack.md)**  
You can install the CCG Content Pack application \(sn\_itom\_ccg\_cp\) if you have the admin role.
-   **[Set up Cloud Configuration Governance for AWS](../task/set-up-ccg-for-aws.md)**  
Set up access to the Amazon Web Services \(AWS\) cloud accounts in Cloud Configuration Governance to enable interaction between the application and the cloud. The application requires access to the cloud accounts to scan the cloud resources for non-compliant configurations and remediate them.
-   **[Set up Cloud Configuration Governance for Microsoft Azure](../task/set-up-ccg-for-azure.md)**  
Set up access to the Microsoft Azure cloud accounts in Cloud Configuration Governance to enable interaction between the application and the cloud. The application requires access to the cloud accounts of your organization to scan the cloud resources for non-compliant configurations and remediate them.
-   **[Domain separation and Cloud Configuration Governance](domain-separation-and-cloud-configuration-governance.md)**  
Domain separation is not supported in Cloud Configuration Governance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Cloud Configuration Governance](../reference/cloud-configuration-governance.md)

