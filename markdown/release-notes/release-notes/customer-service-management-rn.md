---
title: Case management for CSM release notes
description: The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Case management for CSM release notes

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.

## About Case management for CSM

-   Create cases for invoice-related services such as invoice disputes or requested corrections with the Case management for Invoice Operations application.
-   Use process mining to mine the configured base system project to investigate the causes of long resolution times.

See [Case management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-case-management.md) for more information.

## Activation and other requirements

-   **Activation information**

    Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_ActivateCustomerService.md).

-   **Browser requirements**

    ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/browser-support.md).


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/customer-service-mgmt-rn-landing.md)

## May 2025

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.

### What's changed

-   **[Case lines and workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/case-line-form.md)**

    The Case Line table \(sn\_case\_line\) includes the **Install base** and **Asset** reference fields. These fields display information based on the selected account and product.


## Yokohama Early Availability

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.

### What's new

-   **[Case Management for Invoice Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-invoice-operations.md)**

    Use the Case Management for Invoice Operations application \(com.sn\_csm\_invoice\) to create cases for multiple invoices or for specific invoice lines. Agents can use these cases to process invoice-related services such as invoice disputes or requested corrections.

-   **[Process mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/process-mining.md)**

    Use the following features to find process improvement opportunities:

    -   Use work notes analysis to learn the operational reasons behind activity transitions. This feature is Now LLM based.
    -   Mine the configured base system project to investigate the causes and get a clear view of the long resolution times and delays.

### What's changed

-   **[Process mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/process-config-builder.md)**

    Use the process mining enhancements to improve processes as needed:

    -   Removed the viewer role from all records in the Process Mining Content Pack for Customer Service Management \(CSM\).
    -   Set process configurations as read-only templates, deletable only by a process mining administrator. You can enable customers to copy the template or import specific parts into their custom configuration.

## Yokohama

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.

### What's new

-   **[Quick start tests for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/quick-start-tests-csm.md)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


### What's deprecated or removed

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

