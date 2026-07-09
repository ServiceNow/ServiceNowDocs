---
title: Configuring Workflow Data Fabric Home
description: Install Workflow Data Fabric Home and supporting applications to integrate data from multiple sources, unify it into a consistent structure, and make it available across UI, workflows, GenAI, agents, and processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/configuring-workflow-data-fabric.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [configure]
breadcrumb: [Workflow Data Fabric Home, Workflow Data Fabric]
---

# Configuring Workflow Data Fabric Home

Install Workflow Data Fabric Home and supporting applications to integrate data from multiple sources, unify it into a consistent structure, and make it available across UI, workflows, GenAI, agents, and processes.

## Choose your setup

Workflow Data Fabric supports three setup options. Each option adds capabilities on top of the previous one, so choose the option that matches the outcomes you need. You can extend a smaller setup later by installing the next application in the sequence.

|Setup option|Best for|Capabilities enabled|
|------------|--------|--------------------|
|Option 1: Connect Hub|When you want to centrally manage connections to external systems for use in Flow Designer, spokes, and other integration contexts — without cataloging metadata or publishing governed data contracts.|Create and manage connections, manage credentials, grant steward access, and use Now Assist for Workflow Data Fabric \(WDF\) for guided discovery.|
|Option 2: ServiceNow Data Catalog and Connect Hub|When you want a full discovery and metadata experience — browse cataloged assets, view lineage, and evaluate trust — without packaging data into reusable Data Products.|Everything in Option 1, plus configure metadata collectors, populate the Data Catalog with discovered assets, view lineage and impact, and browse the catalog.|
|Option 3: Data Products, ServiceNow Data Catalog, and Connect Hub|When you want the full end-to-end Workflow Data Fabric lifecycle — connect, understand, govern, and act on data through stable contracts.|Everything in Option 2, plus author Data Interfaces and Data Products, publish governed contracts, and enable workflows, analytics, and AI to consume data through Data Products.|

**Note:** Begin every setup by installing one of the three top-level applications: Connect Hub \(sn\_wdf\_connect\_hub\), ServiceNow Data Catalog, or Data Products \(sn\_data\_product\). Each top-level application pulls in its required dependencies automatically. Installing individual sub-applications directly \(for example, sn\_dcg\_ui on its own\) causes errors.

## Configuration overview

1.  Install other required Workflow Data Fabric applications that aren’t already installed.

    |Application|App ID|Link|
    |-----------|------|----|
    |Zero Copy Connectors|\(sn\_data\_fabric\_zcc\) and \(sn\_data\_fabric\)|[Configuring Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configuring-zcc.md)|
    |Workflow Data Fabric Credits|\(sn\_wdf\_token\)|[Workflow Data Fabric Credits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/credits.md)|

2.  Install the Connect Hub \(sn\_wdf\_connect\_hub\), or ServiceNow Data Catalog \(sn\_dcg\_core\), or Data Products \(sn\_data\_product\) store application according to the setup you chose. The applications listed in the table are installed automatically with the specified starting installation.

    |Name|App ID|Installed with|
    |----|------|--------------|
    |WDF Unified Hub \(WDF Home\)|sn\_wdf\_unified\_hub|Connect Hub, ServiceNow Data Catalog, and Data Product|
    |Connect Hub|sn\_wdf\_connect\_hub|Connect Hub, ServiceNow Data Catalog, and Data Product|
    |Now Assist for Workflow Data Fabric \(WDF\)|sn\_nowassist\_wdf|Connect Hub, ServiceNow Data Catalog, and Data Product|
    |ServiceNow Data Catalog|sn\_dcg\_ui|ServiceNow Data Catalog and Data Product|
    |ServiceNow Data Catalog \(Core\)|sn\_dcg\_core|ServiceNow Data Catalog and Data Product|
    |ServiceNow Data Catalog Graph Explorer|sn\_hexplorer|ServiceNow Data Catalog and Data Product|
    |ServiceNow Data Catalog - Metadata Collectors \(UI\)|sn\_meta\_collectors|ServiceNow Data Catalog and Data Product|
    |ServiceNow Data Catalog - Metadata Collectors \(Core\)|sn\_dcg\_cc|ServiceNow Data Catalog and Data Product|
    |Data Product|sn\_data\_product|Data Product only|

    For more information, see [Install Workflow Data Fabric Home store applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/install-workflow-data-fabric.md).

    **Note:** You can start the installation with any of the following applications: Connect Hub \(sn\_wdf\_connect\_hub\), Data Products \(sn\_data\_product\), or ServiceNow Data Catalog \(sn\_dcg\_core\). Installing other apps separately causes errors.

3.  Configure the Now Assist for Workflow Data Fabric \(WDF\) \(sn\_nowassist\_wdf\) plugin. Create a ServiceNow Product Documentation connector and activate the flow generation skill to enable full AI agent capabilities.

    For more information, see [Configure Now Assist for Workflow Data Fabric \(WDF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-now-assist-for-workflow-data-fabric.md).

4.  Assign Workflow Data Fabric roles to users to control access to features, capabilities, and data in Workflow Data Fabric Home.

    For more information, see [Assign roles to Workflow Data Fabric Home users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/assign-roles-to-wdf-users.md).


**Related topics**  


[Install Data Catalog store applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/install-data-catalog-store-applications.md)

[Install data products store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/install-data-products-store-application.md)

