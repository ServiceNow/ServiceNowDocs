---
title: Artifacts that Creator Studio generates when users create an app
description: When a user creates an app in Creator Studio, the ServiceNow AI Platform creates several metadata artifacts, such as tables.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Artifacts that Creator Studio generates when users create an app

When a user creates an app in Creator Studio, the ServiceNow AI Platform creates several metadata artifacts, such as tables.

For each app users add in Creator Studio, the following artifacts are added to the ServiceNow AI Platform.

<table id="table_ixk_trh_2bc"><thead><tr><th>

Artifact

</th><th>

Details

</th></tr></thead><tbody><tr><td>

New table that extends from the base Request Task table

</td><td>

-   Name: \[scope\]\_request \(for example, x\_snc\_marketing\_request\)
-   Label: \[App name\] + Requests \(for example, Marketing Request\)

 **Note:** All of the form questions are stored as catalog variables in the app's Request Task table.

</td></tr><tr><td>

Fulfiller role

</td><td>

-   Name: \[scope\].agent
-   Provides access to the table created by the app

</td></tr><tr><td>

Access Control Lists \(ACLs\)

</td><td>

Provides CRUD access to the new table for the fulfiller and requester roles.

</td></tr><tr><td>

Category for the new app's workspace

</td><td>

Name: \[App Name\] + Requests

</td></tr><tr><td>

Default lists for the new workspace category

</td><td>

-   Open \(active=true\)
-   Open – Unassigned \(active=true^assigned\_toISEMPTY\)
-   Closed \(active=false\)
-   All \(no conditions\)

</td></tr><tr><td>

Dashboard in the new workspace category

</td><td>

Dashboard name: \[App Name\] + RequestsContents:

-   A row of single scores:
    -   Open requests \(active=true\)
    -   Unassigned requests \(active=true and assigned to is empty\)
    -   Closed last 30 days \(closed &gt;= 30 days ago\)
-   A simple list showing all open requests

</td></tr></tbody>
</table>**Parent Topic:**[Administering Creator Studio](../concept/administering-creator-studio.md)

