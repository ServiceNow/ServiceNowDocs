---
title: Configure a persona
description: Create a persona to bind the API token that is used by the Service Graph Connector for Tanium Endpoints. If a persona for the integration already exists, edit it. Use a persona only if a service account isn't permitted by your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-configure-persona.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Configure the Tanium environment, Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure a persona

Create a persona to bind the API token that is used by the Service Graph Connector for Tanium Endpoints. If a persona for the integration already exists, edit it. Use a persona only if a service account isn't permitted by your organization.

## Before you begin

Role required: Tanium administrator

For more information, see [Creating API tokens for ServiceNow](https://help.tanium.com/bundle/Security-Operation-Integration/page/ServiceNow_Integrations/Create_API_key.htm).

## Procedure

1.  Log in to the **Tanium Endpoint Console**.

2.  Navigate to **Administration** &gt; **Permissions** &gt; **Personas**.

3.  Add a new persona or edit an existing persona:

    -   Select **New Persona** to add a new persona.
    -   If a persona already exists, select the **Name** of the persona, and then select **Edit Mode**.
4.  Assign the required roles:

    -   Interact Basic User
    -   Asset User
    -   Gateway User
    Manual permission configuration isn't required because these roles automatically assign all the necessary permissions \(such as Gateway API access and Sensor read access\).

5.  If the integration uses additional sensors, assign read permission for the additional sensors, and then enable access to their content sets.

6.  Assign the required Computer Group access to import data.

    If Computer Group access isn't assigned, data won't be returned after an API call.

7.  Assign users to the persona.

8.  Select **Save** to complete the configuration.


