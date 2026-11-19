---
title: Add entities to an incident or security incident
description: Add one or more existing entities to an incident or security incident. Adding an entity starts the Digital Resilience Incident Reporting case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/set-up-entities-for-targets.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Add entities to an incident or security incident

Add one or more existing entities to an incident or security incident. Adding an entity starts the Digital Resilience Incident Reporting case.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_user

## About this task

The entities that you add to an incident identify what the incident affects. The case lists these entities as impacted areas. The incident is linked to an existing entity so that the regulations mapped to that entity decide which regulation records and reports apply to the case. For information on mapping regulations to entities, see [Map regulations to the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/configure-case-types-map-regu.md).

When you add an entity to an incident or security incident, a flow runs. The flow is either 'DRI case creation on incident entity insert' or 'DRI case creation on SIR entity insert'. The flow automatically creates a Digital Resilience Incident Reporting case in the Digital Resilience Incident Reporting module. It also adds the entity as an impacted area and creates the regulation records that are mapped to the entity. The regulation records then create the action tasks for the regulatory reports. For information on the flows, see [Configure Digital resilience incident reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/workflow-confi-auto-trigger-inci-repo-cases.md).

The entities must already exist and be active. Entities are generated from entity types and entity filters. The entity types that are delivered with Operational Resilience are inactive by default. A user with the sn\_oper\_res.admin role sets up and activates the entity types and filters. Incident users do not create entities. They only select entities that are already active.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and open an incident from the list view.

2.  To add one or multiple entities to the selected incident, open the **Related records** tab, select **Entities**, and select **Add**.

    The case is created automatically in the sn\_grc\_inc\_rptg\_case\_task table in the Draft state. The DRI manager accepts the work on the case and proceeds with the regulatory reporting assessment.

    You can add an entity to an incident only once. If the entity is already added, the error message "Entity with given incident already exists" is displayed and the entity isn't added again.

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

4.  To map an entity to the security incident, navigate to the Entities related list, select **New**, and follow the substeps.

    You can add an entity to a security incident only once. If the entity is already added, the error message "Entity with given security incident already exists" is displayed and the entity isn't added again.

    1.  Select the entity from the drop-down list to associate with the security incident.

        An entity is added to the security incident; for example, the 'Core Banking Portal' entity is added to SIR0010001.

        \[Omitted image "inci-sec-inci-ent-added.png"\] Alt text: Entity added to a security incident.

    2.  To save the changes, select **Save**.

        The entity is displayed in the related record of the security incident.

        \[Omitted image "inci-sec-inci-ent.png"\] Alt text: Example showing how an entity is displayed in the related record.

    The entities are added to the incident or security incident, and a Digital Resilience Incident Reporting case is created automatically.


