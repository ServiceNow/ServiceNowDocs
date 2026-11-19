---
title: Edit a bot process in RPA Hub
description: Edit an existing bot process in RPA Hub to modify a few details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/integrate-applications/rpa-hub/edit-botprocess.html
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Edit a bot process in RPA Hub

Edit an existing bot process in RPA Hub to modify a few details.

## Before you begin

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/create-botprocess.md).

Verify that the life cycle stage of the bot process is **In-maintenance** on the bot process form.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to modify.

5.  On the **Details** tab, update the following fields as appropriate:

    -   Name
    -   Order
    -   Package
    -   Package Version
    -   Run Time Threshold \(mins\)
    -   Job Purging \(days\)
    -   Description
    -   Keep Monitor Active
    -   Force Start
    -   Auto Session Restore
    -   Track Execution Logs
    -   Managed By Group
    -   Enable Desktop In Desktop
    -   End Desktop In Desktop on Complete
    -   Screen Resolution
6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/managing-rpa-hub.md)

**Related topics**  


[Bot Process form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/bot-process-form.md)

