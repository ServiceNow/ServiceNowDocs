---
title: Configuring automation summary execution
description: Configure the execution summary of automation to specify how automation data is aggregated and presented on the Automation Center dashboard.
locale: en-US
release: yokohama
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Automation Center, Automation Center, Data and Automation]
---

# Configuring automation summary execution

Configure the execution summary of automation to specify how automation data is aggregated and presented on the Automation Center dashboard.

You can import and configure data from various sources, such as RPA, ServiceNow flows, Document Intelligence \(DocIntel\), and others to view in the Automation Center dashboard.

Earlier, for data of different data sources different types of summarization was required. It was time-consuming. However, now there’s a generic way to make updates to automation summary execution for data from different sources.

**Note:** The summary execution table displays data about executions of the automations for the domain where they are created and not where they are executed. For example, if an automation is created in the parent domain and executed in the child domain, it will display the data in the parent domain. You cannot see this execution data in the child domain.

-   **[Create automation source type](../task/create-source-type.md)**  
Define the kind of source type that you want to import and use in Automation Center.
-   **[Create automation source](../task/create-source.md)**  
Associate a data source for the selected source type.
-   **[Configure execution summary](../task/create-exe-sum-config.md)**  
Configure the execution summary with the appropriate conditions.
-   **[Create execution state mapping](../task/create-exe-state-mapping.md)**  
Define the mapping for the source and target tables for the configuration to work as expected.

**Parent Topic:**[Configuring Automation Center](automation-center-setup.md)

