---
title: Set up primary and secondary filters for Security Analyst Workspace
description: The Security Analyst Workspace base system includes a set of primary filters for narrowing down the list of security incidents for analysis \(for security incidents assigned to you, all open incidents, and so forth\) and a set of quick \(or secondary\) filters for narrowing down the list even further \(by new incidents, open incidents, only critical incidents, and so forth\).
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up primary and secondary filters for Security Analyst Workspace

The Security Analyst Workspace base system includes a set of primary filters for narrowing down the list of security incidents for analysis \(for security incidents assigned to you, all open incidents, and so forth\) and a set of quick \(or secondary\) filters for narrowing down the list even further \(by new incidents, open incidents, only critical incidents, and so forth\).

## Before you begin

You can use the Classic environment to define additional primary and secondary filters.

As you define filters to be used in the Security Analyst Workspace, you can assign tags to indicate whether they can be used as primary or secondary filters. Primary filters are shown at the top of the security incident list.

![Primary filter](../image/primary-filter.png)

Click **Edit** next to the Quick Filters option to select secondary \(or quick\) filters.

![Secondary or quick filter selection](../image/secondary-filters.png)

Role required: admin or sn\_sec\_cmn.write

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Filters**.

2.  Click **New** and complete the following steps.

    1.  Enter a **Title**.

    2.  Select **Security Incident \[sn\_si\_incident\]** from the **Table** choice list.

    3.  Add your filter conditions.

        For example, the **Open Incidents with Priority = Critical** filter, uses these conditions.

        ![Filter conditions](../image/filter-conditions.png)

    4.  Click **Submit**.

3.  If the **Tags** column is not visible on the filter list, click the gear icon and personalize the view to add it.

4.  Locate the filter you created and add one of the following tags to indicate how the filter should appear in the Security Analyst Workspace.

    -   **SN\_SI\_Primary**: If this tag is selected, the filter can be selected from the primary filter slushbucket in the Security Analyst Workspace.
    -   **SN\_SI\_Primary\_OOB**: If this tag is selected, the filter appears in the **Selected** side of the primary filter slushbucket by default.
    -   **SN\_SI\_Secondary**: If this tag is selected, the filter can be selected from the secondary \(quick\) filter slushbucket.
    -   **SN\_SI\_Secondary\_OOB**: If this tag is selected, the filter appears in the **Selected** side of the primary filter slushbucket by default.

**Related topics**  


[Create and edit filters](https://www.servicenow.com/docs/access?context=t_EditingSavedFilters&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

