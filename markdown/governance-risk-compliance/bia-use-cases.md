---
title: Use cases for business impact analysis
description: You can use the Business Continuity Management application to assess the impact of a downtime on your business services or processes and technical entities such as datacenters or applications. For creating a business impact analysis for your organization, you can refer to the common use cases that are used for managing the business continuity tasks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Business impact analysis, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Use cases for business impact analysis

You can use the Business Continuity Management application to assess the impact of a downtime on your business services or processes and technical entities such as datacenters or applications. For creating a business impact analysis for your organization, you can refer to the common use cases that are used for managing the business continuity tasks.

**Note:** Every customer's environment is different. These use case scenarios only show generic implementations for the stated use cases. Your actual implementation may be different.

## Importance of performing the impact analysis

Performing the impact analysis is an important step in managing your business continuity tasks. It offers these benefits:

-   Prevents and minimizes unintended disruptions to your normal business functions.
-   Helps you identify the critical business processes for your organization and develop strategies to prevent future issues.
-   Assists in planning for the protection of your financial and technical assets.
-   Offers guidance and support about the areas of improvement in future.

## Categories of impact analysis

You can broadly classify the impact analysis in the categories:

-   **Business impact analysis**

    If you are a business user who mainly manages the business services or processes, you want to determine the impact of a downtime on your services and processes. Performing a process-related business impact analysis can help your business to achieve the objectives:

    -   Prepare for the changes to a process or procedure.
    -   Identify the issues that are associated with a process.
    -   Mitigate for the risks that you may face due to an unexpected event.
-   **Technical impact analysis**

    If you are an application user or the IT manager who mainly manages a datacenter or IT systems, you want to determine the impact of a downtime on your data and applications. Performing a technical impact analysis can help you to analyze the impact of technical changes in the deployed product or application. It gives the information about the areas of the information system that may be affected due to a change in the particular section or features of an application.


## Goal and method for creating the business impact analysis

Business impact analysis is performed by the business users to analyze a business service or business process. For example, if you are a financial analyst, you can perform the business impact analysis to estimate the impact of the downtime of a business process or service.

-   **Goal**

    The goals of performing a business impact analysis are to determine the details:

    -   Determine the criticality of the process.
    -   Determine the time that a business can survive without the business service or process.
-   **Method to perform the business impact analysis**

    As a business user, you want to analyze the business service or process by estimating responses to few of the assessment questions:

    -   What are the Impact categories or factors that affect the business service or process?
    -   What is the impact of the downtime of the business process or service?
    -   How many customers are affected?
    -   What is the revenue impact of the downtime for the organization?
    -   Are there additional penalties that the organization may incur?
    -   Is there a reputational damage for the organization?
    -   What is the additional cost to repair the damage such as media coverage of the estimated downtime?
    -   What supporting systems are required on a normal day so that the business processes run efficiently?
    As the BCM lead or manager, when you respond to these assessment questions, it helps you to define the goals of creating a business impact analysis.


## Goal and method for creating the technical impact analysis

Technical impact analysis is performed by the IT owners to analyze the applications or systems that house the data. For example, if you are an IT owner of a financial organization, you can perform the technical impact analysis to determine the criticality and timelines for the applications and frequency to back up the data.

-   **Goal**

    The goals of performing a technical impact analysis are to determine the information:

    -   Criticality of the application.
    -   Timeline that the organization can survive for without the application.
    -   Frequency to back up the data
-   **Method to perform the technical impact analysis**

    As a business user, you can perform the business impact analysis by estimating the responses to the sample assessment questions:

    -   What is the impact on the business if the application is non-functional?
    -   How many employees are impacted?
    -   Is the application external facing?
    -   How many customers are impacted, if the application is external facing?
    -   What kind of data does the application process?
    -   How frequently does the data change?
    As the business user, when you respond to these assessment questions, it helps you to define the goals of the technical impact analysis.


## Using the business impact analysis workflow

If you are a user of the BCM application, you can use the business impact analysis workflow to perform the business impact analysis.

The sample use cases are considered for creating a business impact analysis with BCM:

-   Assess the recovery tier for the business processes or applications that are based on the pre-defined templates.
-   Identify the recovery point objective.
-   Identify the recovery time objective.
-   Identify the dependencies such as vendors, applications, facilities, and other foundational elements.

As a pre-requisite to the business impact analysis workflow, the BCM administrator of your organization sets up the BIA template in the BCM application. The template offers a survey-type user experience in the form of an assessment questionnaire.

If you are the BCM administrator, you can set up the questions that are relevant to your organization and scenario in the BIA template. For more information on setting up the BIA template with the BCM administrator role, see [Configure BIA templates with legacy assessment](../task/configure-bia-template-uib-ws.md).

If you are the BCM lead or BCM program manager, you can respond to the assessment questionnaire on the **Assessments** tab of the business impact analysis record. If you mainly use the business services and processes, your answers serve as key data points for the recovery time objective assessment and dependency assessment. Based on your responses, the criticality of the business process or service and recommended timelines are determined.

If you are the BCM lead or BCM program manager who handles the IT systems, data, and applications, your answers serve as key data points for the recovery point objective assessment. Based on the responses received to the questionnaire, the application calculates the criticality of the business process or service and the recommended timelines.

## Outcome of the impact analysis in BCM

After receiving responses to the questionnaire, the BCM application calculates the results of the business impact analysis. The results are displayed in the **Results** section on the **Details** tab in the business impact analysis record as shown in the example.

![Results section of a business impact analysis.](../image/results-section-of-bia.png)

The BCM application displays the key results in the business impact analysis record:

-   **Recovery tier**

    The BCM application determines the criticality of the process. It is known as the recovery tier. For example, a recover tier can be non-essential or critical for your business.

-   **Recovery time objective**

    The BCM application helps you to determine the time that the organization can survive without the business process that is the recovery time objective \(RTO\).

-   **Adjusted RTO**

    The business impact analysis owner can adjust the recovery time objective value for practical reasons. The adjusted value is displayed in the **Adjusted RTO** field in the **Results** section. If you are the business impact analysis owner and you have adjusted the RTO value with a reason during the assessment, the reason for the adjustment is displayed in the **Reason for adjusted RTO** field.

-   **Dependencies**

    The BCM application helps you to determine the supporting systems or dependencies that are required on a normal day so that the business processes run efficiently. For example, you can have the dependencies for your business:

    -   People
    -   Facility
    -   Application
    -   Vendors

For more information on the recovery time objective, recovery point objective, and recovery tiers, see [RTO, RPO, and recovery tiers](rto-rpo-recovery-tiers.md).

