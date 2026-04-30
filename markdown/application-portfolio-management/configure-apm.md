---
title: Configuring Enterprise Architecture \(formerly Application Portfolio Management\)
description: Learn about the process required to set up Enterprise Architecture to gain a comprehensive understanding of the applications used in your organization.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Configuring Enterprise Architecture \(formerly Application Portfolio Management\)

Learn about the process required to set up Enterprise Architecture to gain a comprehensive understanding of the applications used in your organization.

-   **[Exploring Enterprise Architecture Workspace](explore-eaw.md)**  
The Enterprise Architecture Workspace is part of the Enterprise Architecture application. The workspace is a unified interface with multiple views that help you manage your portfolio efficiently. You can use these views to stay up to date with your tasks, insights, tasks that need attention, portfolio health, and dashboards.
-   **[Activate Enterprise Architecture](../task/activate-apm.md)**  
An administrator can activate the Enterprise Architecture plugin \(com.snc.apm\).
-   **[Enterprise Architecture administration](application-portfolio-management-admin.md)**  
With the sn\_apm.apm\_admin role, you can classify the applications used in the business enterprise. You can also provide privileges to users to do specific tasks, set up indicators to assess application usability, and create bubble charts to help define strategies to maintain applications.
-   **[Enterprise Architecture \(EA\) \(formerlyApplication Portfolio Management\) and the CSDM framework](apm-use-case-product-view.md)**  
Use Enterprise Architecture \(formerly APM\) to gain a comprehensive understanding of your organization's applications so you can identify redundancies and decrease budgetary costs. The goal of this product view is to help you to understand how Enterprise Architecture key entities work with the core CSDM framework.
-   **[Application classification](setup-appln-class-attrib.md)**  
Classifying applications into groups and categories helps your organization track and compare the applications. You can identify relationships and redundancies between the applications more easily. You can also build a complete applications inventory and map the applications to the business functions.
-   **[Manage the life cycle of a business application](../task/create-app-model-lifecycle.md)**  
Create or edit the life cycle of a business application to better manage the business application.
-   **[Run a scheduled job to generate an application model for business applications](../task/run-job-gen-model-id-ba.md)**  
Execute a script to generate the application model for existing business applications. An application model is a structured representation of a business application's components and their relationships and interactions within your application landscape.
-   **[Add a data classification group](../task/add-data-class-group.md)**  
Create a data classification group to categorize data classifications.
-   **[Add a data classification](../task/add-data-classification.md)**  
Create a data classification to apply it to an information object. Effectively control the data used by the business applications.
-   **[Apply classification tags to an information object](../task/apply-classif-tag-info-obj.md)**  
Apply data classification tags to an information object to get better visibility and control over the information objects data.
-   **[Schedule a data certification task](../task/schedule-data-in-business-applications.md)**  
Keep your business applications inventory up to date by certifying the data in the business applications table periodically. Keeping your business application data current helps you to assess your business applications precisely as there are indicators that are dependent on these business applications.
-   **[Run audits to determine invalid and missing configuration data](../task/run-desired-and-scripted-audits.md)**  
Run the scripted audits and desired state audit to determine invalid and missing information in the configuration data. These audits help you find the gaps in business capability, business application, software models, and the life-cycle information.
-   **[Train the similarity solution for Enterprise Architecture to categorize applications while registering](../task/similarity-solution-apm.md)**  
Train the business application similarity definition included within the Predictive Intelligence for Enterprise Architecture to suggest a category for a business application when it is being registered or on-boarded.
-   **[Suggest an application category based on similar business applications](../task/apm-piwb-usecase-ba.md)**  
Use a guided template that walks you through training the Similar Business Applications solution definition for finding similar business applications and suggesting an application category.
-   **[Configure script to customize risk calculation](../task/configure-risk-bubble.md)**  
Configure the risk calculation script at the extension points where the risks bubble up to the next level. With such configuration, the risk engine ignores the default logic of risk calculation and looks for the custom logic.
-   **[Run scheduled job to generate risk values](../task/run-scheduled-job-to-calculate-risks.md)**  
The risks on the product model and business application is time dependent. Based on the external and internal lifecycles the risk changes every day, hence the risk must be calculated daily. A scheduled job is created that runs daily and calculates the risks of the software model and the business application.
-   **[Install Application Portfolio Management \(APM\) Cloud Assessment Application](../task/install-cloud-readiness-sore-prof.md)**  
Install the APM Cloud Assessment application \(app-apm-cloud-readiness\) from  the  ServiceNow Store.
-   **[Schedule a job to compute application scores](../task/schedule-job-for-indicator-sourcing-score-cal.md)**  
Enable the **Load Application Indicators and compute Application Scores** scheduled job to regularly compute the application and indicator scores.
-   **[Set up domain separation for Enterprise Architecture users](../task/set-up-domain-separation-for-apm-users.md)**  
Enterprise Architecture supports domain separation for managed service providers \(MSPs\) to protect the sensitive data of each customer. The protection also ensures inability to view business application data of one customer by another customer and also secures the data within the domain.
-   **[Run scheduled jobs for CMDB Query Builder reports](../task/scheduled-job-cmdb-query-builder.md)**  
Schedule a job to run at a scheduled time or on a recurring schedule for CMDB query. Ensure to do this action in global scope.
-   **[Schedule a job to generate TPM lifecycle data](../task/schedule-job-generate-tpm-data.md)**  
Enable the  **Populate TPM Discovered Technologies and Lifecycles** scheduled job to regularly compute the technology lifecycle risks.
-   **[Run a scheduled job to generate TPM lifecycle data](../task/run-scheduled-job-update-tpm-data.md)**  
Run a scheduled job to fetch the technology lifecycle data for your technology portfolio.
-   **[Schedule a job to generate TPM technology risk](../task/schedule-job-generate-tpm-risk.md)**  
Execute the  **Populate Technology Lifecycle Risks** scheduled job to generate the TPM technology lifecycle risks and populate the result in the TPM Technology Lifecycle Risks \[sn\_apm\_tpm\_technology\_risk\] table.

**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\)](application-portfolio-management.md)

