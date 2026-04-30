---
title: View technology risks in timeline - Legacy
description: View the internal and external life-cycle phases of all technologies or the product models that are used in your organization in the Technology Portfolio Management timeline. You can identify the stages at which the technology is, in terms of the risk factor by their color code.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# View technology risks in timeline - Legacy

View the internal and external life-cycle phases of all technologies or the product models that are used in your organization in the Technology Portfolio Management timeline. You can identify the stages at which the technology is, in terms of the risk factor by their color code.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy Technology Portfolio Management module is moved to the Enterprise Architecture Workspace. To learn more, see [Gantt view of TPM and TRM lifecycle timelines](../concept/eaw-concept/eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md).

To view your data in the TPM timeline view:

-   Create an [inventory of business applications](manage-business-appln.md).
-   Relate the [business application with an application service](relate-business-application-to-business-service.md).
-   Associate the [application service with the software models](associate-business-service-to-software-model.md).
-   Associate the [application service with the hardware models](associate-application-service-hardware-model.md).

The Enterprise Architect \(EA\) can use the timeline view to track the versions and life cycles of technologies, and the number of applications running on those technologies. EA can assess risks on a business application due to its end of life, and create demands and projects as needed.

The lines in the TPM screen indicate the life cycles of the product models. The lines are color coded, which indicates the stages of risk the software model is in, at that quarter or year.

**Note:** In the context of Enterprise Architecture, business services are referred to as application services. Application services are created based on the service \[cmdb\_ci\_service\] table.

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Technology Lifecycles**.

2.  Select a view grouped By Business Application, By Product Classification, By Software Model, or Application Backlog.

3.  By default, the **Quarterly** button is enabled to show the timeline for the four quarters of a year.

    See [views in TPM timeline](../concept/tpm-timeline-views.md).

    Click the **Monthly** button to toggle and view the timeline across all the months in a year. The monthly view helps you to track the risk stage of an application for any specific month in a year.

4.  Click the production icon \(\) to view the production instances that are liable to risks in the current quarter or month.

5.  The lifecycle data sources of software models can be displayed in either of the following two ways:

    -   To display the lifecycle data sources of a particular software model, click the expand icon \(\) of the software model.
    -   To display the lifecycle data sources of all software models related to a business application, click show all lifecycle data sources icon \(\). Use the icon to toggle between show and hide the data sources.
    You can view the timelines of life-cycle data sources in By Business Application, By Product Classification, By Software Model views, and Application Backlog view. All available sources for a software model are queried and retrieved from the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table. The Choices \[sys\_choice\_list\] table lists all the sources of the software models corresponding to the Software Product Lifecycle \[sam\_sw\_product\_lifecycle\] table.

    The sources of software life-cycle data can be internal and can also come from multiple external sources. The life-cycle phase information of the internal data with one external publisher data, with the least sequence number from the Choices \[sys\_choice\] table, is collated and displayed for each of the software models in the timeline. The other external publisher data sources, if present, are not shown in the timeline. Moreover, the overlapping of internal and the external publisher information in the software model timeline can make the phases indistinguishable between the two sources.

    Showing all lifecycle data sources helps in displaying all the publisher data sources for the product model as separate timelines instead of one with the least sequence number. The life-cycle information for each of the sources, whether internal or external, are shown separately. In the presence of more than one external publisher source, the sources displayed are in alphabetical order. As the life-cycle phase information is not merged or collated, the phase details for each source are comprehensible on the timeline.

6.  Click the legend icon \(\) to understand the indications of the markings on the timeline, and the color-coded lines.

    The gradation in color denotes risks, gradually phasing out from one stage to the phasing in of the next stage. You can view the legend for projects only when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

7.  Click **Create** list to [create a demand](create-an-idea.md) or a project.

    **Note:**

    Project in the list appears only when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

8.  To view and edit the application services, hardware and software models, projects, and create demands associated with the business application, click to expand a business application in the **Application** column.

    See [Perform application-related tasks from timeline](application-details-timeline.md).

    **Note:**

    You can create a project for a business application only when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

9.  Point to the risk bubble in the **Risk** column to view the risk of each business application.

    You can also view the underlying technology risk status of a business application in the By Business Application view.

    Risk information is retrieved from the business application risk table.

    Risk is calculated for all business applications that are active. A business application that consumes an application service is said to be active, and the relationship between the two is established in the CI Relationships \[cmdb\_rel\_ci\] table. The engine evaluates the risk of each application service \(of production type only\). It also evaluates the risks of all the application services consumed by a business application collectively from the Application Service Risk \[sn\_apm\_tpm\_business\_service\_risk\] table. If the risk of any one of the application services is at a higher level, then the overall risk is high.

    Formerly business application risks were calculated dynamically while loading the TPM timeline. To reduce the load to the risk engine, the engine now calculates the risk of each business application and stores the information in a Business Application Risk \[sn\_apm\_tpm\_business\_application\_risk\] table.

    Run the [Load TPM Risk Parameters and compute Application Service Risks scheduled job](run-scheduled-job-to-calculate-risks.md) daily to obtain the risk status of the application services on which the business applications run.

10. Click the risk bubble of a software model to view the scores at the risk parameter level.

    You can configure the scripts of the preconfigured risk parameters to evaluate your own risk values, which are stored in the Risk Parameter Score \[sn\_apm\_tpm\_risk\_param\_score\] table.

11. Click the risk bubble of a hardware model to view the breakdown of its risks.

12. Use the pagination option to populate the first 15 business applications, along with their related application services and software models.

    As a maintenance user, you can configure it to load up to 20 or 25 business applications in the Application column.

    1.  Navigate to **System Properties** &gt; **All Properties**.

    2.  Click **sn\_apm.noOfBusinessAppsPerTPMPage** to update the value.

    3.  Click **Update**.

13. Click the life-cycle phase icon \(\) on the hardware or software timeline to view the life-cycle information of the hardware or software model in a pop-up.

    The vertical line on the timeline indicates the current quarter that you are in. See [Software product lifecycle data on the timeline](../concept/lifecycle-data-timeline.md).


-   **[Multiple views in TPM - Legacy](../concept/tpm-timeline-views.md)**  
Multiple views within a TPM timeline screen facilitate users to view the risks of business applications in the way they want. Views can be a simple list of applications, categorizing the applications by products based on their functions, or by the underlying technology of the applications.
-   **[Use timeline to execute your application strategy - Legacy](application-details-timeline.md)**  
**Application** column of the By Business Application view lists all the business applications that are used in your organization. If you toggle to the By Product Classification view, you can view all the technologies in the **Category** column. In the By Software Model view, you can view all the software models for each full version.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

