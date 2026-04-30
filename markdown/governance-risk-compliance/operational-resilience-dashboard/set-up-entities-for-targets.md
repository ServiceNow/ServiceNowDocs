---
title: Set up entities for the targets
description: Set up an entity record in the instance and map it to an incident or security incident. You can map one or multiple entities to the selected incident.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 1
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up entities for the targets

Set up an entity record in the instance and map it to an incident or security incident. You can map one or multiple entities to the selected incident.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and open an incident from the list view.

2.  To add one or multiple entities to the selected incident, select **Add** in the Entities related list.

    The Entities related list is shown in the example.

    ![Entity related list in an incident record.](../image/inci-new-ent.png)

    1.  Choose the entity from the list view.

    2.  Select **Add**.

        The selected entities are added to the incident. The example shows that the "Account Opening Workflow" entity is added to the Entities related list of the "Facility issue" incident.

        ![Example showing an entity added to an incident.](../image/inci-create-sec-inci.png)

3.  To create a security incident from the incident record, select **Create Security Incident**.

    **Note:** Verify that the Security Incident Response application is installed in your instance.

    The security incident is created as shown in the example.

    ![Security incident created from an incident record.](../image/inci-sec-new.png)

4.  To map an entity to the security incident, navigate to Entities related list, select **New**, and follow the substeps.

    1.  Select the entity from the drop-down list to associate with the security incident.

        An entity is added to the security incident; for example, the 'Core Banking Portal' entity is added to SIR0010001.

        ![Entity added to a security incident.](../image/inci-sec-inci-ent-added.png)

    2.  To save the changes, select **Save**.

        The entity is displayed in the related record of the security incident.

        ![Example showing how an entity is displayed in the related record.](../image/inci-sec-inci-ent.png)

    The entities are now set up for the target incidents.


