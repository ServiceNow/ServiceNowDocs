---
title: View automated phishing response playbook flow action designer
description: You can drill down to the Action Designer to view detailed information about the actions being performed for a specific step in the automated phishing response playbook flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/action-phishing-playbook.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Run the automated phishing response playbook flow, Playbook for Automated Phishing, Flow-based Playbooks, Security Incident Response playbooks, Playbook Resources, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View automated phishing response playbook flow action designer

You can drill down to the Action Designer to view detailed information about the actions being performed for a specific step in the automated phishing response playbook flow.

This page describes the Action Designer page for the Get Observables from Task step. Select a task in the Action Outline panel to view the details.

## Action Input

This section shows details on how the action was created including the incident id, the type of observable \(hash or IP\) and observable finding \(malicious emails only\).

\[Omitted image "cj-sir-flow-phishing-action5-1.png"\] Alt text: Automated phishing playbook flow: action designer inputs

## Get M2M Records

This section shows the conditions that have been defined to search for observables in a specified table.

\[Omitted image "cj-sir-flow-phishing-action5-2.png"\] Alt text: Automated phishing playbook flow: action designer get records

## Get Observables

This section shows the script used to retrieve observables based on the specified filter conditions. Finally, the observables meeting this criteria and the count is displayed.

\[Omitted image "cj-sir-flow-phishing-action5-3.png"\] Alt text: Automated phishing playbook flow: action designer get observables

**Note:** All actions defined in this flow are reusable and can be modified according to your requirements.

**Parent Topic:**[Run the automated phishing response playbook flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/run-phishing-playbook.md)

