---
title: Integrating Operational Sustainability Management \(formerly ESG\) with Workday
description: The Operational Sustainability Integration with Workday plugin enables users to import HR data that is required for operational sustainability reporting from Workday into the ESG Management application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Integrating Operational Sustainability Management \(formerly ESG\) with Workday

The Operational Sustainability Integration with Workday plugin enables users to import HR data that is required for operational sustainability reporting from Workday into the ESG Management application.

Using this integration, an ESG administrator can import monthly and yearly metric data from a wide range of categories such as benefits, demographics, compensation, and so on. This integration saves time for HR, Operational Sustainability Management, and IT teams by making the data transfer process secure and automatic. The integration is also configurable according to an organization's requirements. By default, 150 metric definitions in **Inactive** state and 15 corresponding reports are provided to the users. To configure the reports on Workday, see the [Workday ESG Integration Workday Reports' Configuration \[KB1220842\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1220842) article in the Now Support Knowledge Base. The article also provides mappings between the metric definitions and the Workday reports. ESG administrators must activate those metric definitions from which they want data. The data that is obtained is then used for disclosure reporting.

The following are the different types of reports that can be obtained using the integration:

-   **Point in time**: In this type of report, the metric data is obtained until a given point in time. For example, you may want to obtain data for the number of hires in an organization on a specific date such as Jan 25, 2023. In this case, if the metric definition has the frequency set to **Annual**, the data until Dec 31, 2022 will be available for reporting.
-   **Cumulative**: In this type of report, the metric data is obtained for a given period. For example, you may want to obtain the data for the number of hires for a particular quarter in the year 2023.

