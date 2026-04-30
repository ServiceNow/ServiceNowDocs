---
title: View business capability details in capability map
description: Use the capability map to assess capabilities on dimensions such as people, process, and technologies and plan investments accordingly. View the current trend of your business applications and plan to potentiate them by creating goals, demands, and programs and track their progress in the map.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Use capability map for planning, Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# View business capability details in capability map

Use the capability map to assess capabilities on dimensions such as people, process, and technologies and plan investments accordingly. View the current trend of your business applications and plan to potentiate them by creating goals, demands, and programs and track their progress in the map.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy capability ratings module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing a business portfolio](../concept/manage-business-portfolio.md).

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Capability Ratings** &gt; **Capability Map**.

2.  Select the **Business Capability** view.

3.  Click each capability to view the sub-capabilities and their details.

    The left pane of the map displays the capabilities along with the following information:

    -   **Number of sub-capabilities**

        At each capability level, the total count of sub-capabilities and their subsequent level of sub-capabilities is listed within brackets next to the name of the capability. That is, at the parent capability level, the total number of child capabilities and their direct child capabilities is listed.

    -   **Number of applications linked to the capability**

        The applications icon \(![Applications icon](../image/ApplicationsIcon.png)\) displays the total count of applications that are related to that capability.

    -   **Capability score**

        The capability score for the business capability, rounded to two decimal places only, is displayed in a color-coded box next to the application count. The colors indicate:

        -   Major gap: red color, scores in the range of 1–4.
        -   Medium gap: orange color, scores in the range of 4–7.
        -   No gap: green color, scores in the range of 7–10.
        The capability is assessed for the selected fiscal period of the business capability and the score data is retrieved from the apm\_app\_score table.

        The overall score of parent capability is the average sum of the scores of all the direct child capabilities. That is:

        `Score of parent capability = Score of all child capabilities / total number of child capabilities`

        If the parent capability is not assessed and displays \(n/a\) instead of a score, then it means that all its child capabilities are not assessed. However, if one of the child capabilities is not assessed, then the parent capability score is calculated based on the scores of the other child capabilities that have been assessed.

    -   **Capability levels and assessment**

        The map displays capabilities up to six levels. The capability that is at the lowest level or the capability that does not have a child is called the **leaf** level. Only the leaf level capabilities are assessed on the dimensions of people, process, and technology. The capability in the hierarchy that does not have a parent is the level 0 or root capability.

    The right pane of the map displays the details of the capability selected on the left pane, and all the business applications that are related to that capability.

    -   **Details**

        With the **Business Capability** view, all the data of the selected capability are displayed in the **Details** tab.

        ![Capability based planning](../image/CapabilityBasedPlanning.png "Capability based planning")

        -   **Capability**: Displays the name of the business capability that is selected. Click the capability name to navigate to the Business Capability form and view the record details of the selected capability.
        -   **Capability Score**: Displays the capability score of the selected business capability and the individual indicator scores based on the dimensions of people, process, and technology.

            **Note:** If the business capability is at the leaf level, with no sub-capabilities, then the capability score is clickable. On clicking the link, the CI Scores form opens to display the score of the business capability configuration item for the fiscal period selected in the capability map.

            Similarly, the indicator scores of People, Process, and Technology are clickable if they are for the leaf capabilities only. Clicking each of these links opens the Indicator Scores form of the business capability configuration item for the relevant indicator and the fiscal period selected in the capability map.

        -   **Project**: Displays the total number of projects that the selected business capability is part of. The project attached to a sub-capability rolls up to its parent. Likewise, the projects of all the sub-capabilities in a hierarchy rolls up to the root, level 0, capability.

            Clicking the number of projects opens the Projects form with the project details for the business capability.

        -   **Demand**: Displays the total number of demands created for the selected business capability. The demand created for a sub-capability rolls up to its parent. Like manner, the demands attached to all the sub-capabilities in a hierarchy rolls up to its root, level 0, capability in the hierarchy.

            When you select a capability or a sub-capability in the left pane of the map, the total number of demands and projects created or added to the capability, sub-capability, or its technology is displayed on the right pane. Selecting a parent capability displays the consolidated total number of demands created either for the parent or for its child capabilities.

            Clicking the number of demands opens the Demands form showing the demand details for the business capability.

        -   **Total Project Investments**: Displays the total amount invested on the selected business capability in the selected fiscal period. Total project investments are the consolidated amount of investments made on the capability through one or more projects. You can create a project to achieve an objective of one or more business capabilities. Similarly, you can have a business capability tied to more than one project to achieve the goal of the business capability.

            **Note:** The Project and Total Project Investments details are available only when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

            If a project is created to achieve the goals of any two business capabilities, then the **Total planned cost** of the cost plans attached to the project is split equally between the two business capabilities. For example, if $100 is invested on project P1, which impacts business capabilities BC1 and BC2, then the invested amount of $100 is split as $50 each between BC1 and BC2, respectively.

            The investment made on a child capability rolls up to its parent. Likewise, the investments made on all the sub-capabilities in a hierarchy rolls up to the level 0 capability in the hierarchy.

    -   **Business Applications**

        Displays the names of the applications that are directly and indirectly related to the capability and their overall scores.

        Directly related applications are those applications that are directly related to the capability. Indirectly related applications are those applications that are related to another capability in that capability hierarchy. That is, the application is related to either any of the parents or any of the children in that hierarchy.

        Both the **Business Capability** and **Technology Risk** views have the option to display direct and indirect business applications. However, the details displayed regarding the applications slightly vary.

        **Business Capability** view: Displays the names of the business applications on the right pane, which are related to the selected business capability on the left pane, and the overall score of each individual application.

        ![Business application overall score view](../image/BusAppOverallScore.png "Business application overall score view")

        Click the business application hypertext to navigate to the Business Application form and view the record details.

        Click the information icon \(![Information icon](../image/iIcon.png)\) of an application to view the following details:

        ![Business application indicator score](../image/BusiAppIndicatorScore.png "Business application indicator score")

        -   **Project Investments**: Displays the total amount invested in the selected business application for the stipulated fiscal period. Project investments are the consolidated amount of investments made on a business application through one or many projects. You can create a project to fulfill an objective of one or more business applications. Similarly, you can have a business application tied to more than one project to achieve the goal of the business application.

            If a project impacts one or more business applications, then the **Total planned cost** of the cost plans attached to the project is split equally among the business applications. For example, if $100 is invested on project P1, which impacts business applications, BA1 and BA2, then the invested amount of $100 is split equally as $50 each between BA1 and BA2, respectively. Similarly, you can invest in one or more projects that can be tied to one business application \(BA1\). The invested amount is split equally among the applications tied to each of these projects. The resultant consolidated amount from different projects is the project investment of the business application \(BA1\).

            **Note:** The Project Investments and Projects are available only when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

            You cannot roll up cost in the case of business applications as it is an independent entity and is not hierarchical, whereas investment rollup is possible in business capabilities.

            Project investments cannot be made for both business capability and business application within a project. Total planned cost of a project is considered either for business capabilities if you are investing in business capabilities or for business applications if you are investing in business application, and not for both.

        -   **Production Instances**: Number of application services of the production type that the business application is related to.

            The data is retrieved from the CI Relationships \[cmdb\_rel\_ci\] table based on the consumes::consumed by relationship between the business application and the application service.

        -   **Demands** and **Projects**: The number of demands and projects created at the business application level.
        -   **Score indicators**: The number of indicators on which the business application is assessed. It also displays the individual score of each indicator.
        -   **Capabilities supported**: Scrolling down in the pop-up you can also view the number of capabilities the business application supports and the name of each of the capabilities.

            The association between the business capability and the business application is based on the provided by::provides relationship type in the CI relationships table.

        Use the pagination option to display business applications attached to the business capability that you select on the left pane. You can view a maximum number of 10 business application records related directly and indirectly to the capability. Click the left or right arrow to continue to view the previous or next set of records. The pagination option is available for all levels of a capability. The option is helpful to view the business applications of all the capabilities consolidated at the root level capability, especially when there are many applications attached to it.

    -   **Services**

        The tab displays the names of the services that are related to the selected parent business capability on the left pane. You can sort services in alphabetical or reverse order, search for a service, and view only a selected number of services using the pagination option.

        Click the service hypertext to navigate to the service record and edit the record. The business capability is related to the service by establishing Provided by::Provides CI relationship.


## What to do next

[View technology risk details in capability map](technology-risk-map.md)

**Parent Topic:**[Use capability map for planning](view-capability-based-planning.md)

**Related topics**  


[Create business capability and relate the capability with an application](create-a-business-capability.md)

