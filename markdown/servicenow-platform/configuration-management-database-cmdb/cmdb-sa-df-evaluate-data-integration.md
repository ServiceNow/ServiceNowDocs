---
title: Evaluate Data Foundations data integration coverage
description: Identify supported principal classes and attributes from a Discovery pattern or Service Graph Connector to evaluate data coverage and upgrade requirements.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analyze data integrations, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Evaluate Data Foundations data integration coverage

Identify supported principal classes and attributes from a Discovery pattern or Service Graph Connector to evaluate data coverage and upgrade requirements.

## Before you begin

Role required: sn\_cmdb\_admin

## Procedure

1.  Navigate to the CMDB success advisor landing page.

2.  On the Data Foundations card, select **View insights**.

3.  Select the **Data integrations** tab.

4.  Find the Discovery pattern or Service Graph Connector by selecting the respective cards.

5.  Identify the status of your Discovery patterns and Service Graph Connectors to improve CMDB data coverage.

6.  Select the **Attribute coverage** link for a data integration source.

7.  In the Supported principal classes and attributes dialog box, review the attribute coverage details.

    The following details are available:

    -   Integration suggested vs. installed version
    -   Supported CI classes identified as principal classes
    -   List of attributes and whether each is supported by the selected data integration source
8.  When installed version is lower than the suggested version, select the **View available version** link to open the Application manager.

    **Note:** The **View available version** link is available only when applicable for a data integration source. Also, only users with the admin role can install or upgrade an application. See Application Manager.

9.  Determine which CI attributes are being populated by the integration and whether an upgrade is needed to improve the data coverage.

    Available options for improving the data coverage are:

    -   For Discovery patterns, you can perform the following actions based on the applicable criteria:
        -   If you have the pd\_user, you can select **View pattern** for a Discovery pattern to view the pattern. For more information, see Patterns and horizontal discovery.
        -   If you have the pd\_admin role, you can select **View pattern** for a Discovery pattern to understand its contribution and modify the pattern to maximize the attribute coverage. For more information, see Patterns and horizontal discovery.
    -   For Service Graph Connectors, if you have the cmdb\_inst\_admin role, you can perform the following actions based on the applicable criteria:
        -   Select **Install connector** to add a connector from the ServiceNow Store.
        -   Select **Create connection** to configure a Service Graph Connector from SGC Central. For more information, see [Create a connection for a Service Graph Connector in SGC Central](../../sgc-central/task/sgcc-create-connection.md).
        -   Select **View connections** to open and review details of existing installed connections importing hardware asset data within SGC Central. For more information, see [Viewing connections for a Service Graph Connector in SGC Central](../../sgc-central/concept/sgcc-viewing-installed-connection.md#).

