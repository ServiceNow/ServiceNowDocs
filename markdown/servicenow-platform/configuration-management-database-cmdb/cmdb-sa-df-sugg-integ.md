---
title: View suggested integrations for the Data Foundations advisor
description: View integrations recommended for your Data Foundations advisor scope that are not yet installed, to identify opportunities to improve CI data coverage for your principal classes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-sugg-integ.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Analyze data integrations, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View suggested integrations for the Data Foundations advisor

View integrations recommended for your Data Foundations advisor scope that are not yet installed, to identify opportunities to improve CI data coverage for your principal classes.

## Before you begin

Role required: sn\_cmdb\_admin

The Data Foundations advisor dashboard must be configured before you can access the **Data integrations** tab. For more information, see [CMDB success advisor for Data Foundations setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-config-settings.md).

## Procedure

1.  Navigate to the CMDB success advisor landing page.

2.  On the Data Foundations card, select **View insights**.

3.  Select the **Data integrations** tab.

4.  In the **Suggested integrations** section, review the recommended Service Graph Connectors and Discovery patterns to identify potential data sources for improving CI coverage for your principal classes.

    Suggested integrations are recommended based on your selected advisor scope. Installing them can expand data coverage by populating additional CI attributes for your principal classes. All suggested integration sources are accessible for setup from the dashboard.

5.  Select the **Attribute coverage** link next to a suggested integration to view which CI attributes it supports for your principal classes.

    **Note:** If an upgraded version of the integration is suggested, select **View available versions** to open the Application Manager, where users with the admin role can install or upgrade the integration to improve attribute coverage. For more information, see [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md).


## Result

You have identified the integrations recommended for your Data Foundations scope. To evaluate attribute coverage for integrations that are already installed, see [Evaluate Data Foundations data integration coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-evaluate-data-integration.md).

