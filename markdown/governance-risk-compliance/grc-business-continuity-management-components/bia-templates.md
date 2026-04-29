---
title: Business impact analysis \(BIA\) templates
description: The Business Continuity Management application provides pre-configured business impact analysis \(BIA\) templates for creating a business impact analysis. If you are the BCM or BIA administrator, you can use the BIA Templates module in the Business Continuity Management application. You can then select the type of the template, elements, impact categories, and so on, for the business impact analysis.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Business impact analysis, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Business impact analysis \(BIA\) templates

The Business Continuity Management application provides pre-configured business impact analysis \(BIA\) templates for creating a business impact analysis. If you are the BCM or BIA administrator, you can use the **BIA Templates** module in the Business Continuity Management application. You can then select the type of the template, elements, impact categories, and so on, for the business impact analysis.

## Advantages of using a BIA template

The BIA templates store information such as the impact categories and dependency groups that a business process depends on. Using a BIA template offers these advantages:

-   Simplifies the process of creating a business impact analysis.
-   Saves time and resources by pre-populating the templates.
-   Helps you to define the primary object type that you can use the BIA template for. For example, you can use the Application technical impact analysis template to perform a technical impact analysis of an IT application.
-   Populates the dependency groups automatically in the BIA.
-   Helps you to select the impact categories that are relevant to your organization.

## BIA templates in BCM

If you have the sn\_bcm.admin role, you can view the BIA templates that are installed with demo data when you install the application or configure a BIA template in the **BIA Templates** module. The example shows the BIA templates that are installed with demo data in the Business Continuity Management application.

![BIA templates that are installed with demo data.](../image/bia-templates.png)

## BIA template configuration

With the sn\_bcm.admin role, you can configure these details in the BIA template:

-   **Name and Description**

    Use the **Name** and **Description** fields to search for the name and select an appropriate template for your business impact analysis.

-   **Primary Element Assessed**

    Select the type of the elements that you plan to assess such as Business processes or CI service.

-   **Impact Categories**

    Assess specific impact categories during the business impact analysis. For example, you plan to assess the financial impact and legal impact of a downtime.

-   **Dependency Assessments**

    Identify the dependencies for your business impact analysis.

-   **Include CIA**

    Include CIA \(Confidentiality, Integrity, Availability\) information in your business impact analysis if the primary element being analyzed has critical data.


The example shows the sample configuration of a BIA template in an instance.

![Configuration of a BIA template.](../image/bia-template.png)

## Configuring a BIA template

For more information on how to configure a BIA template with the sn\_bcm.admin role, see [Configure BIA templates with legacy assessment](../task/configure-bia-template-uib-ws.md).

## Impact dependency groups

The BIA template used for creating a business impact analysis has dependency groups associated with it. When conducting an assessment, the dependency groups are automatically populated in the BIA. You can view them as Applications, Hardware, Software, Vendors, Workplaces, and others, each in its own container depending on how many of these groups are associated to the template.

![Dependency groups.](../image/impact-dep-groups.png)

Each of them is a dependency group and you can add or remove items that belong to each group within its container.

