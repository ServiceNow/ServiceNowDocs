---
title: Create a campaign
description: Create a recall campaign and also view the list of campaigns claims assigned to the person who has logged in to the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/manufacturing/mco-rc-my-campaigns.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Recall management, Agent management, Use, Manufacturing Commercial Operations]
---

# Create a campaign

Create a recall campaign and also view the list of campaigns claims assigned to the person who has logged in to the workspace.

## Before you begin

Role required: sn\_rcl\_claim\_mgmt.recall\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Recall Management** &gt; **My Campaigns**.

2.  Select **New**.

3.  On the Recall campaign form, fill in the fields.

    For a description of the field values, see [Recall campaign form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/manufacturing/mco-recall-campaign-form.md).

4.  Select **Save**.

    The recall campaign record is created.

    The following actions are displayed:

    -   Import Impacted Assets: To import impacted assets, refer [Importing impacted assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/manufacturing/mco_importing_impacted_assets.md)
    -   Initiate Recall Campaign: To change the recall campaign state from draft to in-progress, you must have atleast one corrective action marked as In use. Only then can the campaign progress beyond the draft stage.
    -   Cancel Campaign: To cancel the recall campaign.
    .


## What to do next

1.  Create [Corrective actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/manufacturing/mco-corrective-actions.md).
2.  Create [Corrective action charges](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/manufacturing/mco_corrective_action_charges.md).
3.  Select **Initiate Recall Campaign** to enable Recall Campaign Phases and Phase &amp; Sub-phases.

