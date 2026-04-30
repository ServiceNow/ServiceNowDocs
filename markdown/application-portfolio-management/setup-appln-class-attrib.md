---
title: Application classification - Legacy
description: Classifying applications into groups and categories helps your organization track and compare the applications. You can identify relationships and redundancies between the applications more easily. You can also build a complete applications inventory and map the applications to the business functions.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Application classification - Legacy

Classifying applications into groups and categories helps your organization track and compare the applications. You can identify relationships and redundancies between the applications more easily. You can also build a complete applications inventory and map the applications to the business functions.

Set up these attributes for classifying and grouping applications:

-   **Application category**

    This attribute is mandatory. It is a grouping attribute which you can use to make application rationalization decisions. Typically you can use this attribute to group applications used in a business process or department. The applications can have overlapping or complementary capabilities, but they are a part of the same business function and must be reviewed together during an application rationalization exercise. The summarized information at the application category level enables you to compare applications within a category using various metrics.

-   **Category group**

    This attribute is optional. It is a grouping attribute for filtering and reporting of application categories.

-   **Application family**

    You can use this optional attribute to group the applications by the manufacturers classification of their products into various product suites.

-   **Business Process**

    This attribute is an optional attribute that is primarily used for filtering and reporting. Level one \(L1\) of a business process is a high-level representation that outlines the business operations of an organization. Ideally L1 business process can be tagged. For example, Oracle Order Management can be tagged to the business process ‘Quote to Cash’. The detailed mapping between the application and the business processes can be created using the CI relationship.

-   **Software Model**

    This attribute is available with the base instance and contains the specifications of the software such as the manufacturer, version, release date, and end of life date. Business application references the corresponding software model record to automatically pull in the software specifications.


To check out an application classification example, see [Application Classification Example](../reference/application-classification-example.md).

-   **[Add or edit an application category group - Legacy](../task/application-category-groups.md)**  
An application category group is a collection of application categories. Category groups help with the filtering and reporting of the application categories. You can create an application category group or edit an existing one to align it with your business requirements.
-   **[Add or edit an application category - Legacy](../task/add-application-categories.md)**  
An application category is a grouping of applications by their purpose and function, fields, or areas. Such a categorization helps you to consolidate applications and rationalize decisions. You can create an application category or edit an existing one to align it with your business requirements.
-   **[Add or edit an application family - Legacy](../task/add-application-families.md)**  
An application family is an attribute to group a set of related applications based on manufacturer classification of their products into product suites. You can create an application family or modify an existing one to align it with your business requirements.
-   **[Add or edit an application business process - Legacy](../task/add-business-process-or-capabilities.md)**  
Business processes are a structured sequence of tasks that are grouped, helping to accomplish specific outcomes. You can create business processes or modify an existing one to align it with your business requirements.
-   **[Create an application portfolio - Legacy](../task/add-portfolios.md)**  
A portfolio is a collection of related projects and demands. You can create a project and execute it to rationalize and modernize the application portfolio. Create a portfolio of applications, and set demands and goals to measure the effort and progress of several projects and also create reports on these projects for analysis.
-   **[Add a strategy for managing applications - Legacy](../task/add-idea-actions.md)**  
Demand actions are strategic decisions that you want to execute for an application. Enterprise Architecture provides preconfigured actions that help you enhance the capability of the applications. You can add new demand actions as per your requirements.

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](configure-apm.md)

