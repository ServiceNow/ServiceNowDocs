---
title: Integrating ESG Management \(formerly ESG\) with Urjanet
description: Urjanet is a cloud-based platform that extracts different utility bills directly from the source, and delivers it into the business systems and applications that rely on it. As an ESG program manager or a metrics manager you can get your utilities data automatically from Urjanet and avoid manual data entry from your various facilities or office owners.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Integrating ESG Management \(formerly ESG\) with Urjanet

Urjanet is a cloud-based platform that extracts different utility bills directly from the source, and delivers it into the business systems and applications that rely on it. As an ESG program manager or a metrics manager you can get your utilities data automatically from Urjanet and avoid manual data entry from your various facilities or office owners.

A utility bill is a detailed invoice, issued and paid once a month from utilities, including electricity, natural gas, water, and waste. With the Operational Sustainability Integration with Urjanet, organizations can obtain historical or real-time utility data from Urjanet into the ServiceNow AI Platform in the form of metrics. These metrics can then be tracked using the Operational Sustainability Workspace and are associated with other operational sustainability components such as goals and targets thus enabling organizations to take the necessary actions for sustainability.

Using this integration, you can automatically bring the following types of data from Urjanet into the ESG Management application.

-   Water and electricity consumption
-   Waste generated and so on.

The workflow of the Operational Sustainability Integration with Urjanet is as follows:

1.  Create entities: Each utility data for all your locations is tracked as an entity in the ESG Management application. For example, your electricity consumption in your Atlanta office is considered to be an entity. Therefore, you must create entities for all the utility data that you want to track. If you've already created the entities, then you must map the utility data that is imported from Urjanet with the entities created. Certain fields such as **Entity class** and **Entity owner** in the entity forms must be manually filled in by the users of the integration.
2.  Activate the metric definitions: For the Operational Sustainability Integration with Urjanet, ServiceNow® provides a few metric definitions by default. You must activate the ones that you require for your metric collection. Only those metric definitions that are active are considered and their data is loaded into the system. Certain fields such as **Unit**, **Frequency** and **Enterprise owner** in the default metric definitions must be manually filled in by the users of the integration. If you don’t want to use the metric definitions provided by default, you can create your own metric definitions.
3.  Import the data for the metrics: After the user activates the required metric definitions, the data for those metric definitions and their entities will be imported into the ESG Management as metrics and metric data.

-   **[Install Operational Sustainability Integration with Urjanet](../task/install-urjanet.md)**  
You can install the Operational Sustainability Integration with Urjanet application \(sn\_esg\_urjanet\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Create an Urjanet connection](../task/create-an-urjanet-connection.md)**  
Create an Urjanet account connection with valid credentials to establish a connection between Urjanet and ServiceNow®. Only one connection can be active for each domain for the integration. You can separate the imported data into logically defined domains. Data access is restricted among the domains.
-   **[Create an entity mapping for Urjanet](../task/configure-entities-for-urjanet.md)**  
Create entity mappings for Urjanet because the Operational Sustainability Integration with Urjanet considers each Urjanet account meter as an entity.
-   **[Create a metric definition mapping](../task/create-metric-definition-mapping.md)**  
Create a metric definition mapping to map the imported data from Urjanet with the correct metric definitions.
-   **[Generate Webhook URL](../task/configure-webhook.md)**  
Define a Webhook registry for generating the Webhook URL. Urjanet uses the Webhook URL to send real time data to the ESG Management application when an Urjanet statement data is either generated or modified.
-   **[Import meter details from Urjanet](../task/import-data-from-urjanet.md)**  
Using scheduled jobs, import meter details such as meter number, meter ID, and so on from Urjanet into the ESG Management application for reporting purposes. The details are imported in the form of entities.
-   **[Load historical Urjanet data](../task/load-historical-urjanet-data.md)**  
Load historical Urjanet account statement data as metric data by creating new metrics that can be managed as part of Operational Sustainability Management. Data is retrieved from the date that you specify while configuring the Urjanet connection.

**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with other applications](integrate-esg.md)

