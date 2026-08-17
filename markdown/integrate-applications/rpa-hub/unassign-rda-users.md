---
title: Unassign an attended user or group from an attended bot process in RPA Hub
description: Unassign an attended user or a group from an attended bot process if the user is moving out of the business process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/integrate-applications/rpa-hub/unassign-rda-users.html
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Unassign an attended user or group from an attended bot process in RPA Hub

Unassign an attended user or a group from an attended bot process if the user is moving out of the business process.

## Before you begin

Do this task only when you select the **Process Type** field as **Attended** on the Bot process configuration form, while creating a bot process. You can't perform this task unless you select that field. For more information, see [Configuring a bot process record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/create-botprocess.md), [Bot process configuration form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/bot-process-config-form.md), and [Bot Process form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/bot-process-form.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open an attended bot process that you want to unassign an attended user or a group from.

5.  On the **Attended Users/Groups** tab, do one of the following actions.

<table id="choicetable_wh5_mgl_frb"><thead><tr><th align="left" id="d167668e141">

Option

</th><th align="left" id="d167668e144">

Action

</th></tr></thead><tbody><tr><td id="d167668e150">

**To delete a user**

</td><td>

1.  Select a user record that you want to unassign.
2.  Select **Delete**.


</td></tr><tr><td id="d167668e171">

**To delete a group**

</td><td>

1.  Select a group record that you want to unassign.
2.  Select **Delete**.


</td></tr></tbody>
</table>
**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/managing-rpa-hub.md)

**Related topics**  


[License distribution in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/license-rpa-hub.md)

