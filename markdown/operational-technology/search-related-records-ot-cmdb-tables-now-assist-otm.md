---
title: Search for related records in an OT CMDB table
description: Search for Operational Technology \(OT\) configuration items \(CIs\) and OT device information available in an OT CMDB table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, OT Manager Foundation, Operational Technology]
---

# Search for related records in an OT CMDB table

Search for Operational Technology \(OT\) configuration items \(CIs\) and OT device information available in an OT CMDB table.

## Before you begin

-   The Now Assist panel must be activated. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/activate-now-assist-panel.md).
-   You must be assigned the now\_assist\_panel\_user role to have access to the Now Assist panel.
-   You must be assigned appropriate roles to search the relevant OT CMDB tables, such as cmdb\_ot\_viewer or cmdb\_ot\_isa\_viewer.

Role required: now\_assist\_panel\_user and cmdb\_ot\_viewer

## About this task

The OT CMDB search feature leverages the following:

-   Now Assist for CMDB's Search CMDB agentic workflow

    **Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

-   ServiceNow AI Platform's Analytics Query Generator skill

    **Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).


## Procedure

1.  Select the **Now Assist** \[Omitted image "now-assist-icon.png"\] Alt text: icon.

    The Now Assist is displayed.

2.  To initiate a search for OT CMDB tables, enter a prompt such as `Search CMDB` or `CMDB Search`.

    The command signals that you want to search the CMDB tables.

3.  Search for an OT device.

    To optimize search results, include OT-specific trigger words or device types in your query, such as `OT`, `Operational Technology`, `PLC`, or `HMI`. Using relevant OT trigger words helps the CMDB search agentic workflow identify the OT context and display results in the Industrial Workspace.

    For example, you can search for OT device information using prompts such as:

    -   `Search for OT PLCs`
    -   `Search for OT network gear with Purdue Level 3`
    -   `Search for critical OT control systems`

## Result

If there are less than five OT device records in the search results, then the agent lists the devices in the Now Assist panel. You can enter the OT device name for more information. The agent gives you the option to view the device in either a form view or a unified map.

Here are some examples of the form view.

\[Omitted image "search-ot-cmdb-initiate.png"\] Alt text: Initiating the conversation in the Now Assist panel to search for OT network gear with a Purdue Level of 3

\[Omitted image "less-than-five-cmdb-search-results-form.png"\] Alt text: Conversation in the Now Assist panel to view the specified network gear in either a form or unified map.

\[Omitted image "cmdb-search-form-result.png"\] Alt text: Form view of the specified network gear accessible through a link in the Now Assist panel.

Here are some examples of the unified map view.

\[Omitted image "less-than-5-cmdb-search-results-map.png"\] Alt text: Conversation in the Now Assist panel to view the specified OT control system in either a form or unified map.

\[Omitted image "cmdb-search-unified-map-result.png"\] Alt text: Unified map view of the specified OT control system accessible through a link in the Now Assist panel.

When more than five OT device records appear in the search results based on your search criteria, you can select the link in the Now Assist panel to view them. Here's an example of the OT PLC search results.

\[Omitted image "ot-cmdb-search.png"\] Alt text: Search results for OT PLCs are using the OT CMDB search function

**Parent Topic:**[Using the OT Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/using-now-assist-for-otm.md)

