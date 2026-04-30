---
title: DevOps Accelerator plugin
description: GRC: DevOps Accelerator is an application that enables your customers to evaluate the compliance for DevOps policies and GRC control objectives integrating with Policy as a Code Engine \(PaCE\).
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# DevOps Accelerator plugin

GRC: DevOps Accelerator is an application that enables your customers to evaluate the compliance for DevOps policies and GRC control objectives integrating with Policy as a Code Engine \(PaCE\).

**Important:** GRC DevOps Accelerator is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

GRC: DevOps Accelerator \(com.sn\_grc\_devops\) plugin maps the control objectives drawn from regulations, standards, and frameworks, such as CIS controls, NIST 800-53, ISO 27002, PCI DSS, and others with DevOps Policy as a Code Engine \(PaCE\). The DevOps policies are provided by the DevOps Config Policy Content Pack.

With this integration you can evaluate the compliance status. The integration also enables the DevOps managers to monitor control compliance, visualize evidence of PaCE execution, and manage exceptions.

## Pre-requisites for DevOps Accelerator

1.  Hierarchy of PaCE-related plugins and CDM-related plugins.
2.  DevOps Config Policy Content Pack provided by PaCE.
3.  GRC plugins: GRC: Cybersecurity Controls Accelerator, GRC: Compliance UCF, and GRC: Continuous Authorization and Monitoring.

**Note:** GRC: DevOps Accelerator \(com.sn\_grc\_devops\) is dependent on DevOps Config Policy Content Pack and GRC: Policy and Compliance Management. However, if GRC: Cybersecurity Controls Accelerator \(CIS\), GRC: Unified Compliance Framework \(UCF\), and GRC: Continuous Authorization and Monitoring \(CAM\) plugins are not installed on the instance, then the staging data relevant to the control objectives from these plugins would not be available on installing GRC: DevOps Accelerator.

GRC: DevOps Accelerator plugin maps the relationship between PaCE policies and control objectives.

**Note:** Not all GRC control objectives may have a relationship with every PaCE policy.

## Populating control objective and PaCE mapping data from the instances to staging table

-   **Control objective to items mapping table**

    As part of DevOps accelerator, the mapping relationships between control objectives and PaCE policies are shipped to the customers. The relationship is captured in Control objective to items \[sn\_compliance\_control\_objective\_item\] table, where the **Control objective** column and **Item record** column, which is the PaCE policy, list the data.

    ![Control objective to item table.](../image/DevOpsMappingPC.png "Control objective to item table")

-   **DevOps policy to control objective staging table**

    ![DevOps accelerator staging table.](../image/DevOpsStagingPC.png "DevOps accelerator staging table")

    There is a staging table as a part of DevOps accelerator, which is DevOps policy to control objective staging \[sn\_grc\_devops\_policy\_control\_objective\_staging\] table. A user with Compliance admin role can view the table.


For CAM and CIS, the sys IDs of the control objectives map with the DevOps policy sys IDs. However, for UCF the source ID of the control objective imported from the Shared List is mapped with the DevOps policy sys ID.

The data in the DevOps policy to control objective staging \[sn\_grc\_devops\_policy\_control\_objective\_staging\] table is shipped in Pending status. The data is populated in the staging table based on the applications that are installed in the instance. The data is not processed if the control objective and the PaCE policy do not exist in the instance.

## Scheduled job to move data from the staging to the main table

A daily job \(Import DevOps policy to Control Objective mapping from staging\) runs after the applications and the DevOps accelerator are installed to add the records to the Control objective to items \(sn\_compliance\_control\_objective\_item\) table. If the record is successfully added to the mapping table, then the status of the record in the staging table moves to Processed. If a control objective is not populated or present in the application, then the record is not processed but is in Pending status.

