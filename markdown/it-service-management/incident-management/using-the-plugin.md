---
title: Incident and problem workflow
description: Incident and problem workflow enables you create a problem from an incident, attach Known Error \(KE\) articles, and communicate problem workarounds and fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/using-the-plugin.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Incident and problem workflow

Incident and problem workflow enables you create a problem from an incident, attach Known Error \(KE\) articles, and communicate problem workarounds and fixes.

The incident and problem workflow supports the following activities:

-   **Create a problem**

    When you create a problem from an existing incident, the incident **State** is set to **On Hold** and the **Reason** is set to **Awaiting Problem** until the linked problem is resolved.

-   **Attach a Known Error \(KE\) article**
    -   When you associate a Known Error \(KE\) article with the incident and the KE article has a problem associated with it, the problem gets associated with the incident.
    -   When you select **Known error** as **Resolution code** to resolve an incident but the incident contains no associated KE articles, then the system prompts you to select a KE article.
-   **Communicate Workaround**

    If a workaround is added to the problem, and if you select the **Communicate Workaround** related link, then the following occurs:

    -   The workaround is copied to the **Work notes** field. A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields. The notification is sent only when the incident state is New, On Hold, or In Progress.
    -   The workaround is copied to the **Additional Comments** field. If **Known error** is selected from the **Resolution code** field of the incident, then a notification is sent to the caller and to the users listed in the **Assigned to** and **Watch list** fields.
-   **Communicate Fix**

    If a fix is added to a problem and if you select the **Communicate Fix** related link, then the following occurs:

    -   The fix is copied to the **Work notes** field.
    -   A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields of the problem record. The notification is sent only when the incident state is New, On Hold, or In Progress.

