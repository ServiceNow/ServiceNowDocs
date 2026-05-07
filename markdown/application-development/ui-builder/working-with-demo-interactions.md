---
title: Working with UI interaction demo data
description: Demo UI interactions give you simple, ready‑made examples that demonstrate common UI interaction patterns. You can duplicate these samples to explore how interactions work, experiment safely, and use them as starting points when building your own experiences.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [UI interactions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Working with UI interaction demo data

Demo UI interactions give you simple, ready‑made examples that demonstrate common UI interaction patterns. You can duplicate these samples to explore how interactions work, experiment safely, and use them as starting points when building your own experiences.

## Key considerations for working with demo interactions

-   Duplicate before customizing. Demo interactions are reference examples; create a copy before modifying.
-   Backward compatibility isn’t guaranteed. Demo content may change between releases.
-   Custom components must be duplicated separately.
-   Corresponding declarative actions are inactive by default and must be manually set to true before testing.
-   Demo interactions don’t cover long‑running processes, usage tracking, automatic refresh behavior, multi-step journeys, or complex branching logic.

<table id="table_zjs_kyc_23c"><thead><tr><th>

Demo Interaction

</th><th>

What it does

</th><th>

Why It’s Useful

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

DEMO Cascade delete

</td><td>

Prompts you with a confirmation message before deleting records, including information about related child records that will also be deleted.**Note:** Unlike other demo interactions, Cascade delete must be duplicated into Global scope before it executes correctly.

</td><td>

Helps you understand how to design safe delete flows that clearly communicate downstream impacts before continuing.

</td><td>

Safe record deletion

</td></tr><tr><td>

DEMO Close incident

</td><td>

Simplifies closing an incident by updating the record and showing a confirmation.

</td><td>

Shows how to build quick, common life-cycle update actions for record forms such as closing, resolving, and advancing status.

</td><td>

Record life-cycle transition

</td></tr><tr><td>

DEMO Report knowledge gap

</td><td>

Opens a short form enabling you to report missing or incomplete knowledge content.

</td><td>

Demonstrates how to gather user input in a lightweight modal and submit it as a record.

</td><td>

User‑submitted feedback

</td></tr><tr><td>

DEMO Create new record

</td><td>

Opens a modeless dialog with a form for creating a new record without leaving the current page.

</td><td>

Teaches you how to invoke record creation in-context using UI interactions.

</td><td>

In‑context record creation

</td></tr><tr><td>

DEMO Reassign records

</td><td>

Opens a modal that lets you select an Assignment Group and Assigned To value, then updates the selected records.

</td><td>

Useful for showing guided update flows, including dependent fields and multi-record reassignment.

</td><td>

Bulk reassignment

</td></tr><tr><td>

DEMO Open modal with record info

</td><td>

Opens a modal that dynamically displays the table, sys\_id, and form view of the record the user is viewing. This data is pulled from the form controller, not passed in as inputs.

</td><td>

Illustrates how to surface additional record details in a modal instead of navigating away.

</td><td>

Contextual record inspection

</td></tr><tr><td>

DEMO Save form and close tab

</td><td>

Saves the current Workspace form and closes the tab \(or shows an alert if closing isn’t possible\).

</td><td>

Demonstrates Workspace‑aware actions, helping you automate save and finish patterns commonly needed by agents.

</td><td>

Save‑and‑finish workflow

</td></tr></tbody>
</table>## Load demo data

Demo data should be loaded only in a development or test instance to prevent conflict with production data.

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Enter `sn-interaction-builder` into the search bar.
3.  Select **Load demo data**.

    ![Application Manager page for devsnc/sn‑interaction‑builder with Load demo data.](../image/uib-uii-demo-data-plugin.png "Load demo data")


## Viewing demo data in UI Builder

1.  From the UI Builder home page, select the **UI interactions** tab to view the list of available interactions.
2.  Use either the list filter from the Label column to search for interactions that begin with DEMO or enter `DEMO` in the search field.
3.  Select any DEMO interaction to view how it works or [duplicate it for your own use](../task/duplicate-demo-data.md).

-   **[Duplicate a demo UI interaction](../task/duplicate-demo-data.md)**  
Create a duplicate of a demo UI interaction example to work with a separate, editable copy.

**Parent Topic:**[UI interactions](uib-ui-interactions.md)

