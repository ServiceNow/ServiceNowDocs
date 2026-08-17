---
title: Create offboarding requests for AI assets
description: Create an offboarding request to retire AI assets that are no longer needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/create-ai-asset-offboarding-request-newexperience.html
release: zurich
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 1
breadcrumb: [Managing your AI asset lifecycle, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Create offboarding requests for AI assets

Create an offboarding request to retire AI assets that are no longer needed.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can create offboarding requests only for the AI assets that they are assigned to manage. In addition, they can only create offboarding requests and submit them for review. They can't approve or reject requests or complete any corresponding offboarding tasks.

## About this task

To retire a deployed AI asset, you can initiate the offboarding process by creating and submitting an offboarding request. This triggers the offboarding workflow that assigns tasks to impacted asset owners and updates the status of the AI asset record to **Retired** on completion.

You can create offboarding requests for the following AI asset types:

-   AI systems \(classic, generative, and agentic\)
-   AI models
-   Datasets
-   MCP servers

## Procedure

1.  Navigate to **All** &gt; **Al Control Tower** &gt; **Home** &gt; **Inventory**.

2.  From the list of available assets, open an asset record with a state of **Deployed** and a status of **Approved**.

3.  Initiate the offboarding request by using one of the following navigation options.

    -   Open the asset record, select the **Actions** menu and select **Create offboarding request**.
    -   In the Lifecycle tab, go to the Retire stage and select **Create offboarding request**
4.  On the Offboarding form, fill in the fields.

<table id="table_cj4_x5x_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset in review

</td><td>

**Note:** If you initiated the offboarding request from an AI asset record, this field populates automatically.

</td></tr><tr><td>

Due date

</td><td>

Date and time at which the request must be completed.

</td></tr><tr><td>

Justification

</td><td>

Justification for creating the request.

</td></tr></tbody>
</table>5.  Select **Save**, the **Actions** menu and, then select **Submit for review**.

6.  In the Submit offboarding request dialog box, select **Submit request**.

    The offboarding workflow is initiated. The **Impacted assets** and the**Offboarding workflow** tabs also appear.


**Parent Topic:**[Managing your AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/manage-lifecycle-newexperience.md)

