---
title: Enable and configure AI Search in Legal Service Portal
description: The ServiceNow AI Search application provides a modern consumer-grade search engine for the Legal Service Portal.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Enable and configure AI Search in Legal Service Portal

The ServiceNow® AI Search application provides a modern consumer-grade search engine for the Legal Service Portal.

## Before you begin

Role required: admin

## Procedure

1.  Add the sys\_id of the Legal Service Portal record to the system property that includes the supported portals.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

    2.  Open the Legal Service Portal record and copy its sys\_id.

    3.  Open the System Properties table \[sys\_properties\], search, and open **glide.service\_portal.enable\_ais\_portal.allow\_list**.

    4.  In the **Value** field, append the sys\_id of Legal Service Portal record.

    5.  Click **Update**.

2.  Update the Legal Service Portal record.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

    2.  Open the Legal Service Portal record.

    3.  Select the **Enable AI Search** check box.

    4.  In the **Search Application** field, select **Legal Service Portal Default Search Application**.

        A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can change it as needed. For more information on defining a search application configuration, see [Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-search-app-cfgs-ais.md).

    5.  In the **Search Results Configuration** field, select **Legal Portal Search**.

        A search results configuration defines how search results are displayed. A search results configuration is selected by default, but you can change it as needed. For more information on defining a search results configuration, see [Create an EVAM definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/entity-view-action-mapper-evam/define-composite-dataset.md).

    6.  Click **Update**.


**Parent Topic:**[Configuring Legal Request Management](../concept/legal-ops-administration.md)

