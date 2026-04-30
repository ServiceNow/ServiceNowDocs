---
title: Working with quick filters
description: Quick filters are easily accessible filters that are available on, security incidents and response tasks lists.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [List view in SIR Workspace, Explore, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Working with quick filters

Quick filters are easily accessible filters that are available on, security incidents and response tasks lists.

## Before you begin

Role required: sn\_si.admin

The SIR Workspace provides quick filters feature that allows you to filter the list of security incidents or response tasks with ease.

You can use quick filters to configure new filters or modify existing filters that appear against these lists. The base system provides the following quick filters for each security incident:

-   **Incidents Opened Today**
-   **Incidents open &gt; 24hrs**
-   **Open incidents with Priority= Critical**
-   **Risk &gt;= 80**
-   **Open Phishing Incidents**

The base system provides the following quick filters for each response task:

-   **Tasks open &gt; 24h**
-   **Open Tasks with Priority = Critical**

**Note:** An admin can configure the required list of quick filters according to the organization need.

## Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  Search for **Quick Filters** \(sn\_si\_aw\_quick\_filters\).

3.  Go to **Related Links** &gt; **Show List** section.

    The **Quick Filters** list page is displayed. OOTB, following is the list of quick filters shipped with the application.

    |Name|Table|Value|
    |----|-----|-----|
    |Tasks opened Today|Security Incident Task \[sn\_si\_task\]|True|
    |Incidents opened Today|Security Incident \[sn\_si\_incident\]|True|
    |Tasks open &gt; 24h|Security Incident Response Task \[sn\_si\_task\]|True|
    |Incidents open &gt; 24h|Security Incident \[sn\_si\_incident\]|True|
    |Open Tasks with Priority = Critical|Security Incident Response Task \[sn\_si\_incident\]|True|
    |Open Incidents with Priority = Critical|Security Incident \[sn\_si\_incident\]|True|
    |Risk score &gt;= 80|Security Incident \[sn\_si\_incident\]|True|
    |Open Phishing Incidents|Security Incident \[sn\_si\_incident\]|True|

    **Note:** The security admin can go ahead and configure these quick filters. As per the business need, admin can modify the existing value to false and create a quick filter.

    ![Quick filters list view](../image/quick-filters-list-view.png "Quick Filters")

4.  Click **New** to create a new filter.

5.  Enter a name for the filter, select the Table, specify the filter condition.

6.  Click **Submit** to return to the previous list page.

    You will see the newly added filter listed on the page.

    ![new filter](../image/new-filter.png)

    **Note:**

    -   The quick filter will be applicable only if the **Active** check box is selected.
    -   Within the workspace, any logged in user can personalize the active quick filters which are available in the application. Users can hide or unhide the newly created quick filters. This feature is based on their user preference.
    -   If a user has modified the preferences for quick filters and a new quick filter is created after that, then if the quick filter is set to active, it will not apply to the user's preference. The user has to manually change the preferences in the personalized view.
7.  Select any existing filter record to modify the existing quick filters.

8.  Modify the name and filter condition.

9.  Click **Update**.


-   **[Add or modify quick filters](add_quick_filters.md)**  
Add or modify quick filters for security incidents or response tasks within the list view.

**Parent Topic:**[List view in SIR Workspace](setting-up-list-view-in-analyst-workspace.md)

**Related topics**  


[Personalize a list](personalize-a-list.md)

[Apply quick filters on Security Incidents and Response Tasks lists](use-quick-filters-for-security-incidents.md)

[Assign Security Incidents](assign-security-incident.md)

[Close multiple security incidents](../task/close-multiple-incidents-sir.md)

[Assign Response Tasks](../task/assign_response_tasks.md)

[Report Phish Email](../task/report-phish-email.md)

[Export Security Incidents or Response Tasks](export-security-incidents-or-response-tasks.md)

[Manage Shift Handover records](manage-shift-handover-records.md)

