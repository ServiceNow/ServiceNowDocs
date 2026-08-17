---
title: Edit an attended configuration record in RPA Hub
description: Edit an existing attended configuration record in RPA Hub to modify a few details of the record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/integrate-applications/rpa-hub/edit-attended-config-rpa.html
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Edit an attended configuration record in RPA Hub

Edit an existing attended configuration record in RPA Hub to modify a few details of the record.

## Before you begin

Ensure you are familiar with Embedded Task Automation concepts. For more information, see [Embedded Task Automation in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/embedded-task-auto-rpa.md).

Create an attended configuration record. For more information, see [Create an attended configuration record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/create-attended-config-rpa.md).

Ensure that the attended configuration record is in **Active** state.

Ensure that the RPA developer \(sn\_rpa\_fdn.rpa\_developer\) is in the Managed by Group list of the associated bot process that is assigned to an Attended Configuration record.

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_developer, or sn\_rpa\_fdn.rpa\_admin

## About this task

Editing an attended configuration record moves the state from **Active** to **Inactive**, opens the form for editing, and the configuration disconnects from the associated ServiceNow form.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  Navigate to the Attended Configuration record either from the Attended Configuration menu list or from an attended bot process record's related list.

<table id="choicetable_uqv_q52_vzb"><thead><tr><th align="left" id="d194062e140">

Option

</th><th align="left" id="d194062e143">

Action

</th></tr></thead><tbody><tr><td id="d194062e149">

**From an Attended Configuration menu list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Attended Configurations**.
2.  Open the attended configuration record that you want to modify.


</td></tr><tr><td id="d194062e176">

**From an attended bot process record's related list**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Open an attended bot process.
3.  On the Attended Configurations tab, select the attended configuration record that you want to modify.


</td></tr></tbody>
</table>4.  In the form header, select **Edit**.

5.  In the confirmation dialog box, select **Edit**.

6.  Update the following fields as appropriate.

    **Table**, **Bot Process Configuration**, **Action Label** fields cannot be edited.

7.  Select **Save**.


**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/managing-rpa-hub.md)

**Related topics**  


[Activate an attended configuration record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/activate-attend-config-rpa.md)

[Deactivate an attended configuration record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/deactivate-attend-config-rpa.md)

[Delete an attended configuration record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/delete-attended-config-rpa.md)

[Invoke Embedded Task Automation via API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/create-button-att-config-rpa.md)

[Visibility conditions of the UI action \(button\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/visibility-cond-button-rpa.md)

