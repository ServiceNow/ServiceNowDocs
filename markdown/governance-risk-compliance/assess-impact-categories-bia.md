---
title: Assess impact categories and dependencies of a process
description: Assess the different components of a business impact analysis \(BIA\). First by assessing and determining the impact categories of a business process. Second, by identifying any underlying dependencies that the business process requires across different dependency types.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Structured workflows for BIA, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Assess impact categories and dependencies of a process

Assess the different components of a business impact analysis \(BIA\). First by assessing and determining the impact categories of a business process. Second, by identifying any underlying dependencies that the business process requires across different dependency types.

## Before you begin

Role required: sn\_bcm.program\_manager or sn\_bcm.planner

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

    By default the records in the **In Draft** state of the Business Impact Analysis list opens.

3.  To create a business impact analysis \(BIA\) record, click **New**.

4.  To update an existing BIA, click the link to the record in the **Name** column.

    You can view different cards that give the information on the impact assessment result, its progress, and the dependencies of the business process on business application, hardware, software, or vendors.

    ![Impact assessment and dependency view of BIA](../image/BIAImpactAssessmentDependencyView.png "BIA impact assessment and dependency views")

    -   **Impact Assessment Result**

        This card provides the assessment results of the recovery tier level and the recovery time objective for the item that is assessed.

        -   **Recovery Point Objective** \(RPO\): Metric that evaluates the data loss during the business disruption duration that can exceed the tolerance level. RPO results appear in the Impact Assessment Result card only when the primary element assessed in the BIA requires data backup. Otherwise the card shows only the Recovery Time Objective \(RTO\) and recovery tier results.
        -   **Recovery Time Objective**: Metric that calculates how quickly the business must recover an element or an item after a disruption. RTO is measured in terms of how long your business can survive following a disaster before operations are restored to normalcy. If the RTO is four hours and the item recovered is beyond four hours, then your business could suffer quite some loss.
        -   **Recovery Tier**: Organizations differ in defining recovery tiers depending on the item and the time by which it should be recovered on the state of a crisis. A recovery time objective of **Immediately**, **1 hour**, or **4 hours** is impending and falls within the **Mission Critical** recovery tier level. On the other hand, an RTO of two weeks to one month can be graded as a **Non-Essential** recovery tier, which may not incur considerable loss to the business.
        **Note:** You can configure the mapping of recovery tiers to RTOs as per your requirement.

        ![Impact assessment result.](../image/ImpactAssessmentResult.png "Impact assessment result")

    -   **Impact Assessment Progress**

        This component indicates the categories of impact that you have assessed and completed in relation to the categories that are assessment pending. As you complete the assessment for each category of impact, you can see the progress of the **Impact Assessment Progress** ribbon component. The color-coded ribbon component prompts you to complete the assessment for the pending impact categories.

        ![Impact assessment progress component.](../image/ImpactAssessmentProgressRibbon.png "Impact assessment progress component")

    -   **Dependent Assessment Progress**

        Identifies the dependency of the business process on different asset classes or types for its functioning. The assessment identifies the relationship between the business process and the business application, software, workplaces, or vendors. Or, the asset types that the process uses. The progress of the dependency assessment pie chart advances as you complete assessing the business applications, software or hardware, and vendors that the business process depends on.

        ![Dependency assessment progress pie chart.](../image/DependencyAssessmentProgress.png "Dependency assessment progress pie chart")

    -   **BIA SLA**

        The business impact analysis also requires a specific time by which the assessment of a business process must be completed. By default, the SLA timer is set to 30 days and it marks the time since the BIA is drafted, which is **In Draft** state, until the time it is complete, which is **Approved** state.

5.  To assess the different types of business impact categories on the business process, click the **RTO Impact Assessment** tab.

    All impact categories are configurable. A business process draws a set of impact categories, by default, from the template that you have used for the business impact analysis. For more information, see: [Review an impact category and assess its downtime](review-impact-category-bia.md).

6.  To answer questions on the data value of the asset in terms of its impact on the business and its data change frequency, click **RPO Impact Assessment** tab.

    For more information, see [Assess RPO impact of technology assets on the business](RPO-asset-impact-assessment.md).

7.  To review the dependency groups and identify the items within each group that your business process depends on, click the **Dependency Assessment** tab.

    You can prioritize your business continuity and recovery plans based on the criticality of the assets that your business process utilizes. For more information, see: [Identify dependent items to prioritize recovery plans](identify-dependent-items-bia.md).

    -   **Order of impact categories**

        The order in which the impact categories appear in the **RTO Impact Assessment**, **RPO Impact Assessment**, and **Dependency Assessment** tabs depend on the order in which the impact categories are created in the template that is used in the BIA.

        The order of impact rating in the RTO impact assessment grid and the order of the questions in the RPO impact assessment grid are defined by the impact rating scale and the impact analysis questions in the BIA, respectively. However, any user who can access the BIA can change the order of the RPO impact grid, RTO impact categories, and dependency groups.

    -   **Columns in dependency group grid**

        If you had set up column configurations for an element of a dependency group and enabled your grid configuration as active, then you can view those columns in the dependency grid for the corresponding dependency group in which element definition matches with the grid configuration element definition. Otherwise, you can view the grid that is rendered based on the configured view; that is either IT asset or non-IT asset view based on the required data backup value of the dependency group.

        ![Grid columns for dependency assessment.](../image/GridConfigBCMWS.png "Grid columns for dependency assessment")

        ![Grid configuration setup.](../image/GridConfigBCMSetup.png "Grid configuration setup")

        For ad hoc reporting of variables created for dependency: Add the columns in Dependency report source \[sn\_bia\_dependency\_report\_source\] table to match the variables that you defined in Element variable where the **Enable reporting** option is set to **true**. A scheduled job that runs weekly retrieves the dependencies \(sn\_bia\_dependency\), where the impact analysis is in approved state, updated in the last seven days, and has not expired, and the corresponding element and updates the data in the reporting table. To display the columns that you require you must set up the [element variable](setup-bcm-element-variable.md) and [grid configuration](setup-bcm-grid-config.md). For more information, see, [Grid configuration for column display](../concept/grid-config-dependency-assessment.md).

8.  To change the order of appearance of the impact categories in RTO, RPO, and dependency groups in dependency assessment, navigate to **Business Continuity** &gt; **Business Impact Analysis** &gt; **Impact Category Results**.

    1.  Click the impact analysis record.

    2.  To change the order of the impact categories for RTO and RPO, click the Impact Category Results related list and change the order in the **Order** column.

    3.  To change the order of dependency groups, click the Impact Dependency Groups related list and change the order.


