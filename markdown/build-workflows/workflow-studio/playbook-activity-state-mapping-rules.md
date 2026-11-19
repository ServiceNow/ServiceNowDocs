---
title: Playbook activity state-mapping rules
description: Use activity state-mapping rules to control which activity state is shown in a card for a given experience status record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/playbook-activity-state-mapping-rules.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook activity state mapping, Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Playbook activity state-mapping rules

Use activity state-mapping rules to control which activity state is shown in a card for a given experience status record.

Activity state-mapping rules are required for each Experience Status Table. These rules determine how to update the experience status record when a playbook user updates an activity state, such as completing an activity.

Out-of-the-box Global Playbook Experience includes a default rule set for the **sys\_flow\_data** table. This rule set is enough for most playbook activities, but additional rules can be created for custom tables if needed.

Activity state-mapping rules for a given Experience Status Table are unique for each Playbook Experience and can be accessed in the related tabs by clicking **Status Mapping**.

\[Omitted image "playbook-status-mapping-tab.png"\] Alt text: Playbook experience status mapping tab

## Experience status mapping records

Each Experience Status Mapping record specifies which field on the **Experience Status Tables** contains the **Experience Status value**. Experience Status Mapping records also have the following related lists.

-   **Experience Status to Activity State** rules
-   **Activity State to Experience Status** rules

\[Omitted image "playbook-experience-status-related.png"\] Alt text: Experience Status Table related lists

The **Experience Status to Activity State** form controls which activity state is shown in a card for a given experience status record value. The form populates the **Experience Status Record Value** list with the choice values of the **Experience Status Field**.

\[Omitted image "playbook-experience-status.png"\] Alt text: Playbook experience status record value list

**Activity State to Experience Status** form controls how the experience status record is updated when a playbook user updates an activity state, such as skipping an activity. The form populates **Experience Status Record Value** list with the choice value of the **Experience Status Field**.

\[Omitted image "playbook-experience-activity-state.png"\] Alt text:

**Parent Topic:**[Playbook activity state mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/playbook-activity-state-mapping.md)

