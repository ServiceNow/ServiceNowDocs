---
title: Create offboarding requests for AI assets
description: Create an offboarding request to retire AI assets that are no longer needed.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating requests for AI assets, Use, AI Control Tower, Enable AI experiences]
---

# Create offboarding requests for AI assets

Create an offboarding request to retire AI assets that are no longer needed.

## Before you begin

Role required:

-   AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\)
-   AI steward \(sn\_ai\_governance\_ai\_steward\)

## About this task

To retire a deployed AI asset, a user with the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role can initiate the offboarding process by creating and submitting an offboarding request. After the request is submitted, a user with the AI steward \(sn\_ai\_governance\_ai\_steward\) role can review and approves the request. This approval triggers the offboarding workflow that assigns tasks to impacted asset owners and updates the Status of the AI asset record to Retired upon completion.

**Note:** We have automated the ServiceNow AI model to initiate the offboarding workflows when a deprecation date is present.

You can create offboarding requests for the following AI asset types:

-   AI systems \(classic, generative, and agentic\)
-   AI models
-   Datasets
-   MCP servers

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  If you have the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role, create an offboarding request.

    1.  Initiate the request by using one of the following navigation options.

<table id="table_tsq_c2x_g3c"><thead><tr><th>

Navigation option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

AI Control Tower Home view

</td><td>

1.  From the Home view of the AI Control Tower workspace, select the **Create request** drop-down menu.
2.  Select **Create an offboarding request**.


</td></tr><tr><td>

Offboarding requests list

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, navigate to **Requests** &gt; **Offboarding requests**.
3.  Select **Create offboarding request**.


</td></tr><tr><td>

AI asset record

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Managed** section and then select the subsection for the type of AI asset that you want to retire.

Alternatively, navigate to **Lifecycle** &gt; **Deploy**.

3.  Select an AI asset that meets the following criteria:
    -   The State is set to Deployed.
    -   The Lifecycle phase is set to Deploy.
    -   The Lifecycle status is set to Deployed.
4.  Select the **Create a request** drop-down menu.
5.  Select **Create an offboarding request**.


</td></tr></tbody>
</table>    2.  On the form, fill in the fields.

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
</table>    3.  Select **Save** and then select **Submit for review**.

    4.  In the Submit offboarding request dialog box, select **Submit request**.

        The offboarding workflow is initiated. The **Impacted assets** and the**Offboarding workflow** tabs also appear.


