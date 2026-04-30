---
title: Scope 3 dashboard
description: The Scope 3 dashboard helps you to calculate and track scope 3 emissions to gain a complete understanding of your organization's operational sustainability impact and ensure compliance with evolving regulations. Scope 3 emissions refer to indirect emissions in your value chain, for example, the emissions generated from procurement of equipment.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Scope 3 dashboard

The Scope 3 dashboard helps you to calculate and track scope 3 emissions to gain a complete understanding of your organization's operational sustainability impact and ensure compliance with evolving regulations. Scope 3 emissions refer to indirect emissions in your value chain, for example, the emissions generated from procurement of equipment.

Integrated with the Operational Sustainability Workspace, the Scope 3 dashboard is useful for ESG program managers and ESG administrators to get an overview of the trends of the organization's scope 3 emissions. To view the scope 3 dashboard, you must activate the Scope 3 emissions management \(sn\_esg\_scope3\) plugin. This application starts collecting data only after the plugin is activated and the necessary categories and models tables are configured. If you want to view historical data on the dashboard, then the data must be imported into the system.

**Note:** A total of 10 metric definitions are provided to collect data for this dashboard. By default, these metric definitions are in the inactive state and must be activated. These metric definitions are grouped under **Scope 3 emissions** for you to easily find them.

You can access the Scope 3 dashboard by selecting the ![Scope 3 dashboard icon](../images/scope-3-icon.jpg) icon on the Operational Sustainability Workspace.

There are 15 categories of greenhouse gases \(GHGs\) for which you can report your Scope 3 emissions. Organizations can choose which categories to report, and with the Scope 3 emissions management application, you can report on the following two categories.

-   Category 1 Purchased goods and services: This category refers to the extraction, production, and transportation of goods and services purchased or acquired by the reporting company in the reporting year.
-   Category 2 Capital goods: This category refers to the extraction, production, and transportation of capital goods purchased or acquired by the reporting company in the reporting year. Capital goods are physical assets like buildings, machinery, and equipment that are used to produce consumer goods or services.

The dashboard displays the scope 3 data for GHG category, spend category, and supplier category. The following sections explain these categories. Understanding these types of data helps you to understand the data that is displayed on the Scope 3 dashboard.

## Spend category data

Spend-based emission factors assign typical levels of greenhouse gas \(GHG\) emissions to different spending categories. For instance, the emissions generated from spending $1 on office equipment may differ from those generated from spending $1 on transportation services. By multiplying the amount spent in each category by the relevant emission factor, you can estimate your indirect emissions. For example, if you categorize all your laptops as assets spend category, you can aggregate the expenditure on all those assets and then multiply the figure by the emission factor value provided by the Environmentally extended input-output \(EEIO\).

## Supplier category data

The supplier category data uses the following calculation methodologies.

-   Environmentally extended input-output \(EEIO\) data: EEIO data integrates environmental data with economic input-output models to assess the environmental impacts associated with economic activities. This type of data is crucial for understanding how economic activities contribute to environmental pressures and can be used to evaluate the environmental impacts of different sectors and products throughout their supply chains. This data can either be entered manually in the ServiceNow instance or can be uploaded in bulk if the data is available in a spreadsheet. EEIO data is derived from the emission tables that are filled by activating from the ESG content accelerator application.
-   Life cycle assessment \(LCA\) data: LCA data is used for evaluating the environmental impacts associated with all stages of a product's life from raw material extraction through materials processing, manufacture, distribution, use, repair and maintenance, and disposal or recycling. LCA data is crucial for conducting these assessments and includes detailed information about the environmental impacts of materials, processes, energy use, and waste management throughout the product life cycle.
-   Supplier category data: Each organization has several suppliers for a variety of goods and services. Some examples of suppliers are laptop suppliers, monitor suppliers, desktop suppliers, and so on. You can categorize each of the suppliers into different categories. The scope 3 dashboard displays the emissions generated by these suppliers using the metric definitions that are provided by default. This information helps you to identify the scope for reduction of emissions. This data can either be entered manually in the ServiceNow instance or can be uploaded in bulk if the data is available in a spreadsheet.

**Note:** For more information on the data calculation, see the [Overview of Calculation Methodologies for Metric Definitions in the Scope 3 Dashboard \[KB1648880\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648880) article in the Now Support Knowledge Base.

## GHG category

Emissions from purchased goods and services, classified under Scope 3 category 1 of the Greenhouse Gas \(GHG\) Protocol and capital goods classified under category 2, refer to the indirect emissions generated from a company's procurement of goods and services. The GHG category also uses the EEIO, LCA, and supplier calculation methodologies.

-   **[Reports on the scope 3 dashboard](reports-on-the-scope-3-dashboard.md)**  
The Scope 3 dashboard displays a variety of reports to easily gauge the sustainability impact of the scope 3 emissions of an organization. All the reports on this dashboard can be drilled down for detailed metric definitions and the entities that provide the data for each report.

**Parent Topic:**[Exploring Operational Sustainability Management \(formerly ESG Management\)](esg-new-explore.md)

**Related topics**  


[Configuring the Scope 3 dashboard](configuring-the-scope-3-dashboard.md)

