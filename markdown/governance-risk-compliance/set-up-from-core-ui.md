---
title: Set up pillars and entity types from Core UI
description: Set up the pillars and entity types using Admin setup from the Core UI in the Operational Resilience application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/set-up-from-core-ui.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up pillars, entity types, entity filters, and entities, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up pillars and entity types from Core UI

Set up the pillars and entity types using Admin setup from the Core UI in the Operational Resilience application.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Pillars**.

    The list of pillars available with the application are shown in the example. All pillars are in the inactive state.

    \[Omitted image "pillars-core-ui-view.png"\] Alt text: Pillars in the Core UI view.

2.  Activate the pillars first.

    1.  Select the pillar that you want to activate.

    2.  Verify that the "Set" field is set to "Operational Resilience" and the "Choice category" field is set to "Pillar" in the GRC Choice record form.

    3.  To activate the pillar, select the Active check box.

        The example shows that the Active check box is selected.

        \[Omitted image "pillar-record-active-option.png"\] Alt text: Active check box is selected.

    4.  To save the settings, select **Update**.

        The example shows that the Business Services entity type is set to active.

        \[Omitted image "pillar-record-marked-active.png"\] Alt text: The entity type is set to active.

    5.  Repeat these steps for all required pillars.

3.  Open the Entity types list from the **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Pillars** menu.

4.  Activate the entity types.

    1.  Select and open an entity type record from the Name column.

        The example shows the entity types that are set up in the instance.

        \[Omitted image "ent-types-list-from-core-ui.png"\] Alt text: Entity types that are set up in the instance.

    2.  Select the Active check box, select **Pillar** \(must be active pillar\), and add **Description** \(optional\).

        Adding the description is an optional step.

        The example shows that the Active check box is selected.

        \[Omitted image "ent-types-active-option.png"\] Alt text: The Active check box is selected.

    3.  To save the entity type, select **Update**.

        The entity type is displayed in the Setup - Entity types list in the UI.

        \[Omitted image "ent-types-marked-active.png"\] Alt text: Entity type is displayed in the Setup - Entity types list.

    4.  Repeat these steps for all required entity types.

        The entity types are displayed in the Setup - Entity types list.


## What to do next

Once pillars and entity types are set up, configure the entity filters. For more information, see [Configure the entity filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-ent-filter.md).

