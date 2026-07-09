---
title: Create a shared parameter in RPA Hub
description: Create a shared parameter so that you can store the global variables or configurable items in one place. These variables are used across bot processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-shared-parameter.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Shared parameters, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create a shared parameter in RPA Hub

Create a shared parameter so that you can store the global variables or configurable items in one place. These variables are used across bot processes.

## Before you begin

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Shared Parameters**.

4.  Select **New**.

5.  On the form, fill in the fields.

6.  Select **Submit**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.

8.  To delete a shared parameter, select the three-dot icon next to the **Save** button and select **Delete**.

    **Note:** Verify that the shared parameter is not associated to any bot process. You can delete a shared parameter which is associated to a retired bot process.


**Parent Topic:**[Shared parameters in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/shared-paramaters-rpa-hub.md)

**Related topics**  


[Process parameter form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-process-parameter-botprocess.md)

[Assign a bot process to a shared parameter in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/assign-botprocess-shared-parameter.md)

[Unassign a bot process from a shared parameter in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/unassign-botprocess-shared-parameter.md)

[View Audit History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_HistorySets.md)

