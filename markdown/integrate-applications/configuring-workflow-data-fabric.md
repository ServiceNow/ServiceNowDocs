---
title: Configuring Workflow Data Fabric Home
description: Install Workflow Data Fabric Home and supporting applications to integrate data from multiple sources, unify it into a consistent structure, and make it available across UI, workflows, GenAI, agents, and processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/configuring-workflow-data-fabric.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Workflow Data Fabric Home, Workflow Data Fabric]
---

# Configuring Workflow Data Fabric Home

Install Workflow Data Fabric Home and supporting applications to integrate data from multiple sources, unify it into a consistent structure, and make it available across UI, workflows, GenAI, agents, and processes.

## Configuration overview

1.  Install other required Workflow Data Fabric applications if they aren’t already installed.

    |Application|App ID|Link|
    |-----------|------|----|
    |Zero Copy Connectors|\(sn\_data\_fabric\_zcc\) and \(sn\_data\_fabric\)|[Configuring Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/configuring-zcc.md)|
    |Workflow Data Fabric Credits|\(sn\_wdf\_token\)|[Workflow Data Fabric Credits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/credits.md)|

2.  Install the Connect Hub \(sn\_wdf\_connect\_hub\) store application. WDF Unified Hub \(sn\_wdf\_unified\_hub\) and ServiceNow Otto for Workflow Data Fabric \(WDF\) \(sn\_nowassist\_wdf\) are automatically installed with Connect Hub \(sn\_wdf\_connect\_hub\).

    For more information, see [Install Workflow Data Fabric Home store applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/install-workflow-data-fabric.md).

3.  Configure the ServiceNow Otto for Workflow Data Fabric \(WDF\) \(sn\_nowassist\_wdf\) plugin. Create a ServiceNow Product Documentation connector, and activate the flow generation skill to enable full AI agent capabilities

    For more information, see [Configure ServiceNow Otto for Workflow Data Fabric \(WDF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/configure-now-assist-for-workflow-data-fabric.md).

4.  Assign Workflow Data Fabric roles to control access to features, capabilities, and data in Workflow Data Fabric Home.

    For more information, see [Assign roles to Workflow Data Fabric Home users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/assign-roles-to-wdf-users.md).


