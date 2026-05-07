---
title: Playbooks
description: Playbooks are structured workflows that guide users, agents, and technicians step-by-step through the activities required to complete a business process. They are available as discrete applications for Sales CRM, Customer Service Management \(CSM\), Field Service Management \(FSM\), and individual industry solutions, and are installed separately from the core CRM products.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 5
---

# Playbooks

Playbooks are structured workflows that guide users, agents, and technicians step-by-step through the activities required to complete a business process. They are available as discrete applications for Sales CRM, Customer Service Management \(CSM\), Field Service Management \(FSM\), and individual industry solutions, and are installed separately from the core CRM products.

## Playbooks overview

A playbook is a structured process attached to a record, typically a case or a work order, that guides the user working on it through a defined sequence of stages and activities. Because playbooks are associated with specific record types, the correct process is applied automatically based on the nature of the work. A complaint case opens with the complaint handling playbook; a work order task opens with the corresponding field service playbook.

![Playbook with a horizontal stage picker that displays stages across the top of the record and activities in the currently selected stage along the side of the record.](../image/case-playbook-horizontal-stages.png "Playbook with horizontal stages")

A playbook is organized into stages and activities that progress sequentially based on conditions set by an administrator. Each stage contains a group of activities to complete before the process moves forward. Activities can be manual tasks or form entries, automated system actions that run without agent input, or guided decisions that present structured questions and branch to a recommended next action based on the response.

**Note:** This topic covers playbooks at a conceptual level. Configuration details, including how to create stages, define activities, build decision trees, and associate playbooks with record types, are covered in the product-specific configuration documentation for each CRM product.

## Playbooks benefits

Playbooks ensure that the correct process is applied consistently across every record, regardless of which agent or technician is handling it.

-   **For agents, fulfillers, and technicians:** Playbooks eliminate the need to know a process from memory or consult separate documentation. Stage-by-stage guidance, activity checklists, and status indicators keep users focused on the right task at the right time. When a decision needs to be made, a guided decision activity surfaces the relevant questions and presents a recommended action directly within the playbook.
-   **For administrators and implementation partners:** Playbooks provide a controlled way to encode process knowledge into the platform, moving compliance requirements, escalation criteria, and documentation obligations into the system where they are applied automatically. Administrators can update a process by modifying the playbook configuration, and the change takes effect immediately for all subsequent records. Predefined playbooks can be deployed as-is or extended to match organizational workflows without modifying underlying case or work order configurations.

## Use cases

-   **Sales CRM: lead engagement**

    A sales organization configures playbooks to guide representatives through structured, multi-step outreach plans for leads and prospects. Automated activities handle routine steps like sending follow-up emails, while configured activities define when sales representatives should call, message, or engage through other channels. Each record that meets a trigger condition automatically starts a sequence and generates a task for the assigned representative, so outreach progresses consistently without manual tracking.

    Sales CRM includes predefined playbooks for customer engagement sequences and return merchandise authorizations. Sales CRM also incorporates case management applications within its playbooks.

-   **Customer Service Management: case management**

    A customer service organization configures playbooks for different case types, each reflecting the specific stages and activities agents need to complete for that type of request. Automated activities handle routine steps like sending acknowledgement emails, while configured activities can be customized to guide agents through the work of investigation and resolution. The corresponding playbook appears automatically in the workspace when an agent opens a case of that type.

    Playbooks for Portals extends this further by enabling a customer-facing version of the guided experience. Instead of an agent being walked through a case, the customer is guided through a self-service intake process on the portal, with their case held in Draft state until they complete and submit it. CSM includes several predefined playbooks, such as onboarding, complaints, and product support cases.

-   **Field Service Management: work order fulfillment**

    A utilities company configures playbooks to guide technicians through the activities required to complete work order tasks, from troubleshooting and parts retrieval through work verification and closure. Each stage includes activity checklists and status indicators so technicians can track progress without losing context.

    Technicians working in the field can access playbooks directly from the Now Mobile Agent application under a selected work order task. FSM includes predefined playbooks for work order task management, covering workflows such as appointment booking, parts and asset usage, service order tasks, and questionnaires, available on both desktop and the Now Mobile Agent.

-   **Financial Services Operations: loan processing**

    A lending institution configures playbooks for loan deferment and forgiveness cases covering acknowledgement, investigation, resolution, and closure, with automated notifications on case creation and configured activities guiding agents through eligibility assessment and approval. A guided decision in the investigation stage recommends the appropriate resolution path based on the applicant's loan status, and can be maintained separately so eligibility criteria can be updated as policy changes.

    FSO includes a broad set of predefined playbooks covering card operations, complaint management, onboarding, loan and deposit operations, and insurance servicing.

-   **Healthcare and Life Sciences: medical device management**

    A healthcare organization configures playbooks to guide clinical engineers through the review and processing of AEM requests for medical devices, from initial request capture through assessment, regulatory review, and final approval. At each stage, configured activities ensure the required documentation and sign-offs are completed before the process can advance. Healthcare and Life Sciences includes predefined playbooks for enrollment cases and medical device workflows in the Patient Support Services and Healthcare CMMS applications.

-   **Public Sector Digital Services: government service delivery**

    A government agency configures playbooks for benefit applications, license renewals, and non-emergency service requests, each reflecting the stages and activities agents need to complete for that case type. Guided decision activities branch based on constituent responses to recommend the correct next action.

    Administrators can also configure optional activities that agents can insert during a playbook run when a case requires it. For example, scheduling a follow-up appointment or requesting additional documentation from a constituent. The corresponding playbook appears automatically in the workspace when an agent creates a case, or when a constituent submits a request through the Government Service Portal. Public Sector Digital Services includes predefined playbooks for social benefits, license and permit, information request, and service request cases.


**Note:** Playbook applications must be installed separately from the core CSM and FSM products. They are available from the ServiceNow Store. Some applications have dependencies on additional plugins. For example, Case Playbooks for Onboarding and Complaints require the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) and the Customer Service Case Action Status plugin \(com.snc.csm\_action\_status\). Review the application listing in the Store for full dependency and licensing information before installation.

**Related topics**  


[Playbooks for Field Service Management](https://www.servicenow.com/docs/access?context=playbooks&version=australia&pubname=australia-field-service-management&ft:locale=en-US)

[Playbooks for Financial Services Operations applications](https://www.servicenow.com/docs/access?context=playbooks-fso-apps&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)

[Playbooks for Public Sector Digital Services](https://www.servicenow.com/docs/access?context=playbooks-psds-exploring&version=australia&pubname=australia-government-industry&ft:locale=en-US)

[Configuring playbooks for Patient Support Services](https://www.servicenow.com/docs/access?context=pss-config-playbook&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)

[Customer Engagement Sequences](https://www.servicenow.com/docs/access?context=explore-customer-engagement-sequences&version=australia&pubname=australia-order-management&ft:locale=en-US)

