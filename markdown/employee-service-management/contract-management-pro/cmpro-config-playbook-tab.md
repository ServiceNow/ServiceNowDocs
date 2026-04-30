---
title: Configuring the Playbook tab on contract repository records
description: Configure the visibility of the Playbook tab on contract repository records so contract managers can review and act on AI‑extracted metadata and obligations.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-11-25"
reading_time_minutes: 1
keywords: [Playbook tab, data broker, Script Include, tab visibility, contract repository, AI extracted metadata, AI extracted obligations]
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
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

