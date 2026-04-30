---
title: Viewing insights of your portfolio
description: You can view the insights for your business portfolio, information portfolio, application portfolio, and technology portfolio.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-04-29"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Viewing insights of your portfolio

You can view the insights for your business portfolio, information portfolio, application portfolio, and technology portfolio.

You can see the details such as the following:

-   Desired and scripted audits
-   Hardware models
-   Software products that are facing high and moderate technology risks
-   Pending certification instances that are open and not 100% complete

The last refreshed time shows when the results were refreshed in your browser. You can manually refresh the results by using the refresh icon \(![Refresh icon](../image/icon-refresh.png)\). You can navigate to the full list by selecting the **View list** button. You can see the details of a record by selecting it.

![Insights view](../image/insights-section.png "Insights view")

-   **Application Portfolio**

    Track information for your business applications. The cards displayed in this section are:

    -   **Past due certification tasks for business applications**: Displays the number of application certification tasks that are past due. This card isn’t displayed if there are no certification tasks or there are no certification tasks that are past due. The data for this card is calculated from the CMDB Data Management Task \(cmdb\_data\_management\_task\_list\) table.
    -   **Candidate business applications for retirement**: Displays the number of business applications that are fit for retirement, based on their indicator scores.
    -   **Candidate business applications for migration**: Displays the number of business applications that are fit for migration, based on their indicator scores.
    -   **Candidate business applications for investment**: Displays the number of business applications that are fit for further investment, based on their indicator scores.
    -   **Business applications w/o cost data**: Displays the number of business applications that lack any cost data associated with them.
    **Note:** To learn about application indicator scores, see [Configure indicators](eaw-concept/eaw-configure-indicators.md).

-   **Business Portfolio**

    Get insights on your business capabilities, business applications and manage them effectively to fulfill the goals of your organization.

-   **Information Portfolio**

    Track the details of the information objects that are related to the business applications and integrations in your enterprise.

-   **Technology Portfolio**

    Track the technology lifecycle risk for business applications, application services, servers, software products, and hardware models.

    -   **Track technology risks**

        Use this filter to see the risks for the next 1 month, 3 months, 6 months, 12 months, and 18 months. By default, the 1-month filter is applied.

    -   **Show only production instances**

        Use this toggle button to see only productions instances that are having technology lifecycle risks. By default, this filter is off.

    -   **View all technology lifecycle risks**

        Select this link to see the list of all technology lifecycle risks sorted by earliest lifecycle date, which means the earliest date when a technology lifecycle risk is to happen. You can also export the Technology lifecycle risks information to Excel, CSV, JSON, or PDF as required.

        The data in the Technology lifecycle risks table is fetched from the TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\] table.

<table id="table_ick_wpf_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Earliest lifecycle date

</td><td>

The minimum of End of support or End of extended support or End of life dates

</td></tr><tr><td>

Business application

</td><td>

Name of the business application

</td></tr><tr><td>

Application service

</td><td>

Service associated to the business application

</td></tr><tr><td>

Type

</td><td>

Element type. Choices are:-   Software
-   Hardware


</td></tr><tr><td>

Software product

</td><td>

Name of the software product

</td></tr><tr><td>

Hardware model

</td><td>

Model number for the hardware product

</td></tr><tr><td>

Server

</td><td>

Name of the server that is associated with the software product or hardware model.

</td></tr><tr><td>

End of support date

</td><td>

The end of support date for the software product or hardware model

</td></tr><tr><td>

End of extended support date

</td><td>

The end of extended support date for the software product or hardware model

</td></tr><tr><td>

End of life date

</td><td>

The end of life date for the software product or hardware model

</td></tr><tr><td>

Used for

</td><td>

The application service being used for. For example, production or staging.

</td></tr><tr><td>

TPM technology lifecycle

</td><td>

The link to the TPM technology lifecycles of the hardware model or software product.

</td></tr></tbody>
</table>
**Parent Topic:**[Enterprise Architecture Workspace](ea-workspace.md)

