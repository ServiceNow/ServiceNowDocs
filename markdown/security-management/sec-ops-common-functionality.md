---
title: Security Operations common functionality
description: Whenever any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated, the Security Support Common plugin is activated. This plugin loads various modules that provide functionality that is common across all Security Operations applications.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Security Operations]
---

# Security Operations common functionality

Whenever any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated, the Security Support Common plugin is activated. This plugin loads various modules that provide functionality that is common across all Security Operations applications.

**Note:** Only users with the \[sn\_sec\_cmn.admin\] can view and use the Security Operations module. This role is inherited when you are assigned an administrative role in any of the Security Operations applications.

## Security Operations Modules

<table id="table_td5_g1s_3z"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Security Operations Integration Reference](../../secops-integration-reference/concept/secops-integ-ref.md), [Threat Intelligence integrations](../../threat-intelligence/concept/threat-intelligence-integrations.md), [Vulnerability Response integrations](../../vulnerability-response/concept/vuln_integrations.md)

</td><td>

Several integrations are included with the Security Operations applications \(Security Incident Response, Threat Intelligence, and Vulnerability Response\). This section provides instructions for activating the plugins and configuring both ServiceNow and third-party integrations. Also included are some basic guidelines for developing your own integrations, as well as details on specific integrations included in the base system.

</td></tr><tr><td>

[Security Operations email processing](email-processing.md)

</td><td>

You can set up the integration of information from external detection systems, provide granularity in processing security operations records, handle unmatched emails, and prevent duplication of records using Email Processing.

</td></tr><tr><td>

Groups

</td><td>

-   Filter Groups

Create and use filter groups to locate records from any table on your instance. For example, you can create a group of all computers by the same manufacturer. You can also filter configuration items \(CIs\) that have similar vulnerabilities or that fall within a particular subnet IP address range.

-   Escalations

You can create an escalation path for security incidents for issues requiring more attention or expertise. Once an escalation group exists, a button appears on any security incident in that group.


</td></tr><tr><td>

Security Tags

</td><td>

Tags: Security tag rules provide filtering for security tag access.

</td></tr><tr><td>

Workflows

</td><td>

-   View Security Workflows

You can view the many workflows included with the Security Operations applications. You can create workflows from templates and in the Workflow Editor.

-   Workflow Triggers

Security Operations workflow triggers contain a condition on a table. All workflows attached to the workflow trigger record run when the condition is met.


</td></tr><tr><td>

Utilities

</td><td>

-   Enrichment Data Mapping

Enrichment Data Mapping transforms data from XML, JSON, or Properties files to ServiceNow records. Security Operations workflows use enrichment data maps and provide output data to security incidents.

-   Field Value Transforms

Transforms unique customer field values into field values recognized by Security Operations email parsing, data enrichment or tables using field maps. Supports choice fields, references, and aligns external data into the standard terminology and format for your new record.

-   Field Mapping

Security Operations tables can be mapped to and from other tables, linking a security incident to a customer service case or a problem to other parts of the Security Operations system. For example, you can integrate a plugin to a Security Incident Response task.

-   On-Demand Orchestration

During Security Incident Response analysis, a security analyst may want to perform a task that is driven by a security incident workflow. For example, run a process dump on a particular CI. This can be accomplished with on-demand orchestration.

-   Operating Systems Groups

NA.

-   SecOps Application Registry

NA.


</td></tr><tr><td>

CMDB

</td><td>

CI Identifier Rules: CI identifiers are rules used to lookup a configuration item \(CI\) in the CMDB that contains matching information from a third-party integration. These rules define the fields that contain matching data and the order of precedence by which they are evaluated. The lowest **Order** value is evaluated first.

</td></tr></tbody>
</table>-   **[Create and define filter groups in Security Operations](../task/create-filter-group.md)**  
Create and use filter groups to locate records from any table on your instance. For example, you can create a group of all computers by the same manufacturer. You can also filter configuration items \(CIs\) that have similar vulnerabilities or that fall within a particular subnet IP address range.
-   **[Shared data transformation](shared-data-transformation.md)**  
The Security Incident Response, Vulnerability Response, and Threat Intelligence plugins share common features, for relationship data and duplication rules, used to import external and internal information into Security Operations.
-   **[Security Operations email processing](email-processing.md)**  
You can set up the integration of information from external detection systems, provide granularity in processing security operations records, handle unmatched emails, and prevent duplication of records using Email Processing.
-   **[Security Operations field mapping](field-mapping.md)**  
Security Operations tables can be mapped to and from other tables, linking a security incident to a customer service case or a problem to other parts of the Security Operations system.
-   **[Security Operations field value transforms](field-value-transforms.md)**  
Transforms unique customer field values into field values recognized by Security Operations email parsing, data enrichment or tables using field maps. Supports choice fields, references, and aligns external data into the standard terminology and format for your new record.
-   **[Security Operations enrichment data mapping](enrichment-data-mapping.md)**  
Enrichment Data Mapping transforms data from XML, JSON, or Properties files to ServiceNow records. Security Operations workflows use enrichment data maps and provide output data to security incidents.
-   **[Security Operations user-defined escalation](user-defined-escalation.md)**  
You can create an escalation path for security incidents for issues requiring more attention or expertise. Once an escalation group exists, a button appears on any security incident in that group.
-   **[Create domain-separated property overrides](../task/create-dom-sep-prop-overrides.md)**  
When you use domain separation, you can create overrides to existing Security Operations properties that allow you to customize the functions of the applications in each of your domains.
-   **[Create an operating system group](../task/create-new-os-group.md)**  
Operating system groups are used to map an operating system to specific process types and scripts in Security Incident Response workflows. The scripts define how running processes for the defined operating system groups are retrieved. New operating systems can be added as needed.
-   **[Set up security tag groups and tags](../task/create-class-group-and-tags.md)**  
You can assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to create metadata on the responding record and define who should have access to specific types of security content. The tags can be added to security groups to organize them.
-   **[Security annotations](security-annotations.md)**  
A security annotation is a note of explanation or comments added to a configuration item, observable, or use on a security incident.
-   **[Components installed with Security Support Common](../reference/install-with-sec-sup-common.md)**  
Several types of components are installed with Security Support Common. They provide common functionality for use across the various security applications, such as Security Incident Response.
-   **[Search Security Operations](../task/t_SearchSecOps.md)**  
You can find information quickly in any Security Operations application using the search icon in the screen header. Zing is the text indexing and search engine that performs all text searches in your instance.
-   **[Security Operations Integration Reference](../../secops-integration-reference/concept/secops-integ-ref.md)**  
Developers and ServiceNow partners can use the information in this section to gain understanding of the under-the-hood functionality of third-party integrations, including development guidelines, integration capabilities, and workflows.
-   **[Security Operations workflow triggers](workflow-triggers.md)**  
Security Operations workflow triggers contain a condition on a table. All workflows attached to the workflow trigger record run when the condition is met.
-   **[Security Operations Orchestration](../../security-operations-orchestration/concept/security-operations-orchestration.md)**  
Users can interact with and retrieve data from Windows or UNIX-based systems and environments using activity packs and workflows in Security Operations Orchestration.

