---
title: Set up entities for the targets
description: Set up an entity record in the instance and map it to an incident or security incident. You can map one or multiple entities to the selected incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/set-up-entities-for-targets.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up entities for the targets

Set up an entity record in the instance and map it to an incident or security incident. You can map one or multiple entities to the selected incident.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## About this task

When an entity is mapped to an incident or security incident, the 'DRI case creation on incident entity insert' or 'DRI case creation on SIR entity insert' flow runs and a Digital Resilience Incident Reporting case is created automatically in the Digital Resilience Incident Reporting module with the prebuilt flow. For information on the flows, see [Configure Digital resilience incident reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/workflow-confi-auto-trigger-inci-repo-cases.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and open an incident from the list view.

2.  To add one or multiple entities to the selected incident, select **Add** in the Entities related list.

    Adding the entity triggers the DRI case creation flow, which generates a Digital Resilience Incident Reporting case record automatically in the sn\_grc\_inc\_rptg\_case\_task table. The DRI manager can then assign the case and proceed with the regulatory reporting assessment.

    The Entities related list is shown in the example.

    \[Omitted image "inci-new-ent.png"\] Alt text: Entity related list in an incident record.

    1.  Choose the entity from the list view.

    2.  Select **Add**.

        The selected entities are added to the incident. The example shows that the "Account Opening Workflow" entity is added to the Entities related list of the "Facility issue" incident.

        \[Omitted image "inci-create-sec-inci.png"\] Alt text: Example showing an entity added to an incident.

3.  To create a security incident from the incident record, select **Create Security Incident**.

    **Note:** Verify that the Security Incident Response application is installed in your instance.

    The security incident is created as shown in the example.

    \[Omitted image "inci-sec-new.png"\] Alt text: Security incident created from an incident record.

4.  To map an entity to the security incident, navigate to Entities related list, select **New**, and follow the substeps.

    1.  Select the entity from the drop-down list to associate with the security incident.

        An entity is added to the security incident; for example, the 'Core Banking Portal' entity is added to SIR0010001.

        \[Omitted image "inci-sec-inci-ent-added.png"\] Alt text: Entity added to a security incident.

    2.  To save the changes, select **Save**.

        The entity is displayed in the related record of the security incident.

        \[Omitted image "inci-sec-inci-ent.png"\] Alt text: Example showing how an entity is displayed in the related record.

    The entities are now set up for the target incidents.


