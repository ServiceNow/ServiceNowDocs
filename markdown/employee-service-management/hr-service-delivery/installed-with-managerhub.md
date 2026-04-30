---
title: Components installed with Manager Hub
description: Several types of components are installed with activation of the Manager Hub \[sn\_mh\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference for Manager Hub, Manager Hub, HR Service Delivery, Employee Service Management]
---

# Components installed with Manager Hub

Several types of components are installed with activation of the Manager Hub \[sn\_mh\] plugin, including tables, user roles, and scheduled jobs.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Manager Hub Admin\[sn\_mh.admin\]

</td><td>

Grants write access to Manager Hub contents. A Manager Hub administrator can:-   Activate and run the Add Manager Hub user role scheduled job to assign the Manager Hub user role to new people managers.
-   Manually assign the Manager Hub user role to new people managers.
-   Configure team data, team request, important dates records, team column data, team filters, and daily stats records to display data on Manager Hub.

</td><td>

-   sn\_mh.manager\_hub\_user
-   sn\_mh.content\_manager

</td></tr><tr><td>

Manager Hub Content Manager\[sn\_mh.content\_manager\]

</td><td>

Grants read access to Manager Hub contents. A Manager Hub Content Manager can view team data, team requests, important dates, team column data, team filters, and daily stats configuration records.

</td><td>

 

</td></tr><tr><td>

Manager Hub User \[sn\_mh.manager\_hub\_user\]

</td><td>

Can view information about their reporting employees in Manager Hub.

</td><td>

Knowledge view role

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Important Dates Configuration\[sn\_mh\_important\_dates\_config\]

</td><td>

Stores configuration records of important dates.

</td></tr><tr><td>

Team Column Configuration\[sn\_mh\_team\_column\_config\]

</td><td>

Stores configuration records of team columns.

</td></tr><tr><td>

Team Daily Stat\[sn\_mh\_team\_daily\_stat\]

</td><td>

Stores configuration records of team daily stats.

</td></tr><tr><td>

Team Data Configuration\[sn\_mh\_team\_data\_config\]

</td><td>

Stores configuration records of team data.

</td></tr><tr><td>

Team Column Data Configuration\[sn\_mh\_team\_data\_m2m\_column\]

</td><td>

Stores mappings of columns and team data.

</td></tr><tr><td>

Team Filter Group Data\[sn\_mh\_team\_data\_m2m\_filter\_group\]

</td><td>

Stores configuration records of team filter group data.

</td></tr><tr><td>

Team Filter Group\[sn\_mh\_team\_filter\_group\]

</td><td>

Stores configuration records of team filter groups.

</td></tr><tr><td>

Filter sources\[sn\_mh\_team\_m2m\_filter\_sources\]

</td><td>

Stores configuration records of filter sources.

</td></tr><tr><td>

Team Requests Configuration\[sn\_mh\_team\_requests\_config\]

</td><td>

Stores configuration records of team requests.

</td></tr></tbody>
</table>**Parent Topic:**[Reference for Manager Hub](reference-manager-hub.md)

**Related topics**  


[Campaign configurations for Manager Hub](../concept/manager-hub-campaign.md)

[Default configurations for important dates](../concept/manager-hub-imp-dates.md)

[Default configurations for team requests](../concept/manager-hub-team-requests.md)

[Default configurations for team data](../concept/team-data-config.md)

[Default configurations for team column data](../concept/config-team-column.md)

[Default configurations for filter groups](../concept/config-filter-group.md)

[Default configurations for daily stats](../concept/config-daily-stats.md)

[Default configurations for To do's](../concept/manager-hub-todos.md)

[Default proactive prompts for Manager Hub](../concept/prompts-mh.md)

[Use the View menu icon in Manager Hub](view-menu.md)

[Assign learning form](assign-learning-form.md)

[Create a conversation form](create-conversation-form.md)

[Schedule a conversation form](schedule-conversation-form.md)

