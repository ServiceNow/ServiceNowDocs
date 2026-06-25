---
title: Add the Threat Hunting Playbook to a Case
description: If a Case does not meet the auto-trigger conditions for the Threat Hunting playbook, you can attach the playbook to the Case manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-add-playbook-manually.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 1
keywords: [tisc, threat hunting, playbook, manual add]
breadcrumb: [Threat Hunting Playbook, Using playbooks, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Add the Threat Hunting Playbook to a Case

If a Case does not meet the auto-trigger conditions for the Threat Hunting playbook, you can attach the playbook to the Case manually.

## Before you begin

Role required: sn\_sec\_tisc.analyst

The Case must be open. You can't add the Threat Hunting playbook to a closed Case.

## About this task

Use this procedure when the Threat Hunting playbook doesn't auto-trigger but you still want to run a threat hunt. For example, you want to run it when the Case Type is not **Threat Hunting**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Open a Case record and select **\[Omitted image "more-action-menu.png"\] Alt text: More actions** &gt; **Add Playbook**.

5.  Select **Threat Hunting** from the list of available playbooks.

6.  Review the confirmation dialog and confirm the addition.

    **Important:** Adding a playbook can result in repetition of the activities completed on the Case, for example, MITRE techniques associated or scenarios entered.


## Result

The Threat Hunt Playbook is attached to the Case and initiates the **Intake** stage. For details on each stage, see [Use the Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-use-threat-hunt-playbook.md).

**Parent Topic:**[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)

**Related topics**  


[Threat Hunting Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-hunt-playbook.md)

