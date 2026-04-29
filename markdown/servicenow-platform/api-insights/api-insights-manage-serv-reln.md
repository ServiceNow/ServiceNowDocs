---
title: Managing application service relationships for APIs
description: You can associate APIs with relevant configuration items \(CIs\) to ensure accurate mappings between APIs and the configuration items they support.View existing relationships between an API and application services.Create relationships between an API and application services.Remove relationships between an API and application services.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage API data, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Managing application service relationships for APIs

You can associate APIs with relevant configuration items \(CIs\) to ensure accurate mappings between APIs and the configuration items they support.

Application service relationships link APIs to business context and the CIs they depend on, providing clarity on dependencies and improving performance visibility. They enable you to monitor, track changes, and resolve issues more efficiently.

For APIs, application service relationships map how they interact with other CIs, enabling you to manage dependencies, ensure business continuity, and respond quickly to incidents. By understanding these relationships, you gain better control over API performance and the availability of connected CIs.

By using application service relationships, you can:

-   Identify which APIs are tied to specific application services and their related CIs.
-   Understand the dependencies between APIs and the CIs they support.
-   Manage and monitor API performance and its impact on critical business services and CIs.

For more information, see [Service instances \(Application services\)](../../configuration-management/concept/application-services.md).

The available actions for handling application service relationships for APIs include:

-   [View application service relationships](api-insights-manage-serv-reln.md#).
-   [Create application service relationships](api-insights-manage-serv-reln.md#).
-   [Remove application service relationships](api-insights-manage-serv-reln.md#).

**Note:** When managing multiple API relationships for application services, you can automate the mapping. For more information, see [Automate tag-based relationship mapping](../../../Chunk1716298283.md#).

## View application service relationships

View existing relationships between an API and application services.

### Before you begin

Role required: sn\_cmdb\_admin, sn\_api\_insights\_ws.api\_mgmt\_architect\_admin, or sn\_api\_insights\_ws.api\_mgmt\_architect

### Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the **APIs** tab.

3.  Select an API from the **Name** column on the API data table.

4.  In the Relationship map section, select **Manage service relationships**.

5.  View existing relationships between application services and the selected API on the Related application services table.


## Create application service relationships

Create relationships between an API and application services.

### Before you begin

Role required: sn\_cmdb\_admin or sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

### Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the **APIs** tab.

3.  Select an API from the **Name** column on the API data table.

4.  In the Relationship map section, select **Manage service relationships**.

5.  Select **Create relationships**.

6.  Select application services to create relationships with the selected API.

7.  Select **Create**.


## Remove application service relationships

Remove relationships between an API and application services.

### Before you begin

Role required: sn\_cmdb\_admin or sn\_api\_insights\_ws.api\_mgmt\_architect\_admin

### Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the **APIs** tab.

3.  Select an API from the **Name** column on the API data table.

4.  In the Relationship map section, select **Manage service relationships**.

5.  On the Related application services table, select the check box for an existing relationship.

6.  Select **Remove relationships**.


