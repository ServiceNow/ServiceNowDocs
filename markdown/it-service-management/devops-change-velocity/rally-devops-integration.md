---
title: Rally integration with DevOps Change Velocity
description: Connect to your Broadcom Rally instance to discover plans and configure real-time notifications to enable change traceability and automation.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Rally integration with DevOps Change Velocity

Connect to your Broadcom Rally instance to discover plans and configure real-time notifications to enable change traceability and automation.

## Rally integration overview

With this integration, you can configure and expose data like projects, user stories, and defects from Rally. You can then associate these planning objects to an application for end-to-end traceability.

**Install Rally plugin**

You must install the Rally application from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

**Note:**

-   The default object types configured for Rally are `"ObjectTypes"["HierarchicalRequirement","Defect","Feature"]`.
-   The file script include **Rally state mapping helper** is editable. You can override this file with your specific customization as required.
-   Scheduledstate in Rally is used when mapping object state to internal ServiceNow work item state.
-   For tool mappings, see [Tool mappings](dev-ops-tool-integration.md#section_rsp_z1v_xnb).

## Get started

Use one of the following options to onboard Rally. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard Rally to DevOps Change Velocity — Workspace](../task/rally-connect-workspace.md)**  
Connect to your Rally instance using the DevOps Change Workspace playbook to configure webhooks and discover plans.
-   **[Onboard Rally to DevOps Change Velocity — Service Catalog](../task/sc-rally.md)**  
Create, connect, discover, and configure your Rally instance using the ServiceNow Service Catalog.
-   **[Onboard Rally to DevOps Change Velocity — Classic](../task/rally-create-tool.md)**  
With this integration, you can configure and expose data like projects, user stories, and defects from the Rally. You can then associate these planning objects to application for end-to-end traceability.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

