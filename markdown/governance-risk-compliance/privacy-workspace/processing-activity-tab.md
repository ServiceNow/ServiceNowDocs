---
title: Processing activity tab
description: The Processing activity tab on the Privacy management dashboard provides a comprehensive and real-time overview of all data processing activities across the organization.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Privacy Workspace for the privacy manager, Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Processing activity tab

The Processing activity tab on the Privacy management dashboard provides a comprehensive and real-time overview of all data processing activities across the organization.

The Processing activity tab on the Privacy management dashboard supports privacy teams, compliance officers, and data protection professionals. This dashboard consolidates key metrics and visualizations to track the status, criticality, compliance levels, and categorization of processing activities.

By offering intuitive insights through charts, graphs, and filters, the dashboard enables proactive management of data privacy obligations and facilitates informed decision-making in line with regulatory requirements. You can use filters and drop-down lists in the widgets to customize the views based on your preferences.

This dashboard displays the following widgets.

-   **Processing activities by state**

    This section displays a summary of processing activities categorized by their current workflow states: New, Discover, Review, Monitor, and Retire. Each state block provides a quick overview of volume and enables direct navigation to filtered activity lists.

-   **Processing activities by criticality score**

    The gauge chart displays the total number of active processing activities segmented by criticality score: High and Low. This chart enables stakeholders to prioritize efforts based on regulatory risk classification levels.

    If any criticality factor under Regulatory details is marked Yes and criticality is assessed, the processing activity’s criticality score is set to High. If all factors are answered as No, then the score is Low. The score is determined using the Automated criticality factors RAM and can be configured according to requirements.

-   **Processing activities by department**

    The bar chart displays a breakdown of processing activities across different departments. It enables departmental accountability and visibility into privacy management's distribution. You can also filter by the criticality score to view the criticality score of processing activities across different departments.

-   **Least compliant processing activities**

    This widget highlights activities with the lowest compliance scores in a list view. Each entry shows criticality score and aggregated residual risk. With the filter, the analysts can focus on processing activities having low compliance and high criticality score or low compliance and high aggregated residual risk.

-   **Processing activities by data subject type**

    The bar chart illustrates activities grouped by data subject types such as Employees, Candidates, Customers, Internal Staff, Job Applicants, and so on. It helps in assessing which categories of data subjects are most involved in processing activities and take appropriate measures to safeguard the data of these data subjects. You can apply a filter to focus specifically on vulnerable data subjects.

-   **Processing activities by information object category**

    The bar chart presents classification based on the types of data processed. The categorization supports the identification of data types most involved in processing. It also enables filtering by sensitive Information Object \(IO category\), helping the privacy team identify data types and implement appropriate measures to safeguard the data.

-   **Processing activities by type**

    The pie chart depicts the underlying record \(entity type\) based on which the processing activity is created. This categorization helps in determining the scope of privacy initiatives across business functions and technology platforms.

-   **Processing activities by data processing role**

    The pie chart shows the roles undertaken in data processing like Controller and Processor. Clarity about the role played in processing activities is vital for assigning responsibilities and meeting legal requirements.


The following image shows the Processing activity dashboard.

![Processing activity tab on the privacy management home page.](../image/processing-activity-tab.png "Processing activity tab")

**Parent Topic:**[Privacy Workspace for the privacy manager](privacy-mgmt-ws-privacy-compliance-manager.md)

