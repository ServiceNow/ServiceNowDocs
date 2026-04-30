---
title: Configuring Standard Record Page in Service Operations Workspace
description: Configure individual record pages to display information and help them to update the customization easily.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring record pages in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring Standard Record Page in Service Operations Workspace

Configure individual record pages to display information and help them to update the customization easily.

A Standard Record Page \(SRP\) is the basic format in which records appear in the Service Operations Workspace. These record pages have containers, components, modals, and other layouts that display the record information.

Service Operations Workspace contains incidents, cases, and tasks that an agent requires for daily work. SRP provides a basic structure that displays record information, such as a communication interface and suggestions for resolution. It provides the following constructs that help in customization:

-   Presets: Presets are the pre-configured mappings inside the record pages. When you add a new component to the record page, the presets associated with the component are also added to the record page. You can configure presets to components by selecting the ![lock icon.](../../incident-management/image/lock-icon.png) lock icon of a configuration. A copy or duplicate of the component contains these preset values.
-   Controllers: Controllers are the base scripts that help implement a record page's functionality. When you create a copy or duplicate of the record page, SRP establishes a reference to the original controller. You can’t modify the base functionality of the record page. However, you can modify the record page using the scripts and states according to your requirements.

**Note:**

-   If you are on a version prior to 4.0, you can change the Incident record page using **Record SNC** in the UI Builder.
-   ServiceNow doesn’t recommend customizing the Incident record page using methods such as **Record SNC** or **SRP Record**. So, no support is provided for record page customizations.

-   **[Adding Declarative Actions on the Standard Record Page](../task/customize-srp-sow.md)**  
Adding declarative actions on the Incident page and the tabs inside the incident record page using the Standard Record Page \(SRP\) in the Service Operations Workspace.
-   **[Custom Modal Migration in Standard Record Page](../task/custom-modal-migration-srp.md)**  
Modify the modal containers inside a record page in the Service Operations Workspace.
-   **[Modify the Record Page in the Service Operations Workspace using the Standard Record Page](../task/configure-record-page-order-sow.md)**  
Configure the order number and screen conditions of a record page using the Standard Record Page \(SRP\) in the Service Operations Workspace.
-   **[Configure the Agent Assist tab in Service Operations Workspace using the Standard Record Page](../task/configure-agent-assist-tab-sow-srp.md)**  
Enable or disable the Agent Assist tab in the contextual side panel for the required record type using the Standard Record Page \(SRP\) in Service Operations Workspace.

**Parent Topic:**[Configuring record pages in Service Operations Workspace for ITSM](configuring-record-pages-sow-itsm.md)

