---
title: Playbook for Automated Phishing
description: The Automated Phishing playbook helps you resolve certain types of security threats in a step-by-step manner. With the flow designer templates, you can automate the steps in the phishing response playbook and resolve incidents quickly and efficiently.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Playbook for Automated Phishing

The Automated Phishing playbook helps you resolve certain types of security threats in a step-by-step manner. With the flow designer templates, you can automate the steps in the phishing response playbook and resolve incidents quickly and efficiently.

You can use templates authored with flow designer to automate the tasks in the [Phishing Response Playbook](../task/use-the-playbook.md#) to analyze and resolve phishing attacks in your organization.

The phishing response playbook includes the following flows and subflows:

-   Security Incident - Automated Phishing Response Template: This template is designed to automate the phishing response tasks and contains a sequence of actions including a trigger.
-   Security Incident - Phishing Manual Template: This template is the existing manual phishing response workflow. Set the category to Phishing to activate the flow.

These templates contain a sequence of reusable actions designed to respond to phishing attacks. Each flow has a trigger \(condition\), a sequence of actions and subflows that you can annotate for readability. To access these flows, you must install the Security Operations spoke.

**Note:** Activate these templates before you can use them. See [Activate a Security Incident Response flow](../task/getting-started-phishing-playbook.md) for details.

-   Run Threat Lookups for Observables: Performs threat lookups of selected observables.
-   Enrich Observables: Allows you to enrich observables with additional information from various sources.
-   Assess Phishing Email Impact: Allows you to assess the impact of the phishing email. When you receive an email at the phishing email address, this subflow parses the .EML attachment and compares the information to the email matching rules.
-   Eradicate Phishing Emails: Allows you to delete or eradicate phishing emails to help reduce exposure to a specific attack.
-   Run Sighting Search on Observables: Determines the prevalence of a threat over time or test remediation or eradication efforts.
-   Create Block Requests: Blocks communication with observables associated with the incident.

These subflows represent a set of reusable operations that you can use in multiple playbooks. You can use these subflows to define custom templates \(flows\) according to your requirements.

To create custom templates \(flows\), follow the instructions in Flows.

-   **[Run the automated phishing response playbook flow](../task/run-phishing-playbook.md)**  
Using the flow designer, you can define and automate tasks in the playbook to analyze and resolve phishing attacks against your organization.

**Parent Topic:**[Flow-based Playbooks](playbook-flow-based.md)

