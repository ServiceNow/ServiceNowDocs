---
title: Configuring Workflow Data Fabric Home
description: Install Workflow Data Fabric Home and supporting applications to integrate data from multiple sources, unify it into a consistent structure, and make it available across UI, workflows, GenAI, agents, and processes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Workflow Data Fabric Home, Workflow Data Fabric]
---

# Configuring Workflow Data Fabric Home

Install Workflow Data Fabric Home and supporting applications to integrate data from multiple sources, unify it into a consistent structure, and make it available across UI, workflows, GenAI, agents, and processes.

## Configuration overview

1.  Install other required Workflow Data Fabric applications that aren’t already installed.

    |Application|App ID|Link|
    |-----------|------|----|
    |Zero Copy Connectors|\(sn\_data\_fabric\_zcc\) and \(sn\_data\_fabric\)|[Configuring Zero Copy Connectors](../../zero-copy-connectors/concept/configuring-zcc.md)|
    |Workflow Data Fabric Credits|\(sn\_wdf\_token\)|[Workflow Data Fabric Credits](../../create-integrations-apps/concept/credits.md#)|

2.  Install the Connect Hub \(sn\_wdf\_connect\_hub\) store application. The applications listed in the table are installed automatically with Connect Hub and enable the Workflow Data Fabric experience.

    |Name|App ID|
    |----|------|
    |WDF Unified Hub \(WDF Home\)|sn\_wdf\_unified\_hub|
    |Connect Hub|sn\_wdf\_connect\_hub|
    |Now Assist for Workflow Data Fabric \(WDF\)|sn\_nowassist\_wdf|
    |Data Products|sn\_data\_product|
    |ServiceNow Data Catalog Graph Explorer|sn\_hexplorer|
    |ServiceNow Data Catalog \(UI\)|sn\_dcg\_ui|
    |ServiceNow Data Catalog \(Core\)|sn\_dcg\_core|
    |ServiceNow Data Catalog - Metadata Collectors \(UI\)|sn\_meta\_collectors|
    |ServiceNow Data Catalog - Metadata Collectors \(Core\)|sn\_dcg\_cc|

    For more information, see [Install Workflow Data Fabric Home store applications](../task/install-workflow-data-fabric.md).

    **Note:** You can start the installation with any of the following applications: Connect Hub \(sn\_wdf\_connect\_hub\), Data Products \(sn\_data\_product\), or ServiceNow Data Catalog \(Core\) \(sn\_dcg\_core\). Installing other apps separately causes errors.

3.  Configure the Now Assist for Workflow Data Fabric \(WDF\) \(sn\_nowassist\_wdf\) plugin. Create a ServiceNow Product Documentation connector and activate the flow generation skill to enable full AI agent capabilities.

    For more information, see [Configure Now Assist for Workflow Data Fabric \(WDF\)](../task/configure-now-assist-for-workflow-data-fabric.md).

4.  Assign Workflow Data Fabric roles to users to control access to features, capabilities, and data in Workflow Data Fabric Home.

    For more information, see [Assign roles to Workflow Data Fabric Home users](../task/assign-roles-to-wdf-users.md).


