---
title: Search for related records in an OT CMDB table
description: Search for Operational Technology \(OT\) configuration items \(CIs\) and OT device information available in an OT CMDB table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/search-related-records-ot-cmdb-tables-now-assist-otm.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
breadcrumb: [Use the OT Manager Foundation, Use, Operational Technology Manager, Operational Technology]
---

# Search for related records in an OT CMDB table

Search for Operational Technology \(OT\) configuration items \(CIs\) and OT device information available in an OT CMDB table.

## Before you begin

-   The ServiceNowOtto panel must be activated. For more information, see [Activate the panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).
-   You must be assigned the now\_assist\_panel\_user role to have access to the ServiceNowOtto panel.
-   You must be assigned appropriate roles to search the relevant OT CMDB tables, such as cmdb\_ot\_viewer or cmdb\_ot\_isa\_viewer.

Role required: now\_assist\_panel\_user and cmdb\_ot\_viewer

## About this task

The OT CMDB search feature uses the following:

-   ServiceNow Otto for CMDB's Search CMDB agentic workflow

    **Important:** This agentic workflow is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

-   ServiceNow AI Platform's Analytics Query Generator skill

    **Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).


## Procedure

1.  Select the **ServiceNow Otto** \[Omitted image "now-assist-icon.png"\] Alt text: icon.

    The ServiceNowOtto panel is displayed.

2.  Enter a prompt such as `Search CMDB` or `CMDB Search` to search for OT CMDB tables.

    The command initiates a search of the CMDB tables.

3.  Search for an OT device.

    To optimize search results, include OT-specific trigger words or device types in your query, such as `OT`, `Operational Technology`, `PLC`, or `HMI`. Using relevant OT trigger words helps the CMDB search agentic workflow identify the OT context and display results in the Industrial Workspace.

    For example, you can search for OT device information using prompts such as:

    -   `Search for OT PLCs`
    -   `Search for OT network gear with Purdue Level 3`
    -   `Search for critical OT control systems`

## Result

If fewer than five device records appear in the search results, the panel displays the devices. You can enter the OT device name for more information. The agent then gives you the option to view the device in either a form view or a unified map.

When more than five OT device records appear in the search results based on your search criteria, you can select the link in the panel to view them.

**Parent Topic:**[Use the OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/using-now-assist-for-otm.md)

