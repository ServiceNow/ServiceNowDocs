---
title: Configuring the Playbook tab on contract repository records
description: Configure the visibility of the Playbook tab on contract repository records so contract managers can review and act on AI‑extracted metadata and obligations.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Playbook tab, data broker, Script Include, tab visibility, contract repository, AI extracted metadata, AI extracted obligations]
breadcrumb: [Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configuring the Playbook tab on contract repository records

Configure the visibility of the Playbook tab on contract repository records so contract managers can review and act on AI‑extracted metadata and obligations.

The playbook appears on the contract repository record when the Now Assist in Contract Management plugin is installed for your workspace. If the playbook tab is not configured in the base system for your workspace, you must configure the playbook tab to control its visibility.

The visibility of the Playbook tab is controlled by a data broker. The conditional logic is provided as a script method, `sn_cm_gen_ai.ContractsMetadataExtractionHelper()` in a Script include file. To invoke this action, create a method in one of your Script include files for your workspace, which can be accessed by the data broker linked to your workspace on the UI Builder.

1.  [Add a script include method for the Playbook tab](cmpro-config-script-playbook.md)
2.  [Add a data broker server script for the Playbook tab](cmpro-data-broker-playbook.md)
3.  [Add the data broker to your workspace page](cmpro-add-databroker-workspace.md)
4.  [Configure the Playbook tab component for your workspace](cmpro-confg-playbook-comp.md)
5.  [Configure obligation review for the playbook](cmpro-add-obligation-playbook.md)

-   **[Add a script include method for the Playbook tab](cmpro-config-script-playbook.md)**  
Add a script include method that controls the **Playbook** tab visibility on the contract repository record by verifying plugin availability and applying conditional logic.
-   **[Add a data broker server script for the Playbook tab](cmpro-data-broker-playbook.md)**  
Configure a data broker server script that connects the UI Builder component to the script include method controlling the **Playbook** tab visibility.
-   **[Add the data broker to your workspace page](cmpro-add-databroker-workspace.md)**  
Add the data resources to your page in the UI Builder to dynamically expose data from tables, records, or other elements on your page.
-   **[Configure the Playbook tab component for your workspace](cmpro-confg-playbook-comp.md)**  
Use the Tabs component in UI Builder to configure the **Playbook** tab on the contract repository record page for your workspace.
-   **[Configure obligation review for the playbook](cmpro-add-obligation-playbook.md)**  
Create a page in UI Builder that uses a viewport component to dynamically load obligation review content in the playbook.

**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to the contract request record](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Add Contract documents tab to the contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Group contract documents by contract type in a contract request](cncore-config-srp-grouping.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Assign a role for configuring template mappings](cncore-tbl-access-config-role.md)

[Enable contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

