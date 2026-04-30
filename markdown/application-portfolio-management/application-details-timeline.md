---
title: Use timeline to execute your application strategy - Legacy
description: Application column of the By Business Application view lists all the business applications that are used in your organization. If you toggle to the By Product Classification view, you can view all the technologies in the Category column. In the By Software Model view, you can view all the software models for each full version.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Technology risks in timeline - Legacy, Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Use timeline to execute your application strategy - Legacy

**Application** column of the By Business Application view lists all the business applications that are used in your organization. If you toggle to the By Product Classification view, you can view all the technologies in the **Category** column. In the By Software Model view, you can view all the software models for each full version.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

By default, the TPM timeline view expands the first business application in the list to display its associated application services at the first level. It then displays the software and hardware models underlying the application service at the next level.

For the subsequent list of business applications, click to expand the arrow of the business application label to see the count and list of application services that are tied to the application. You can also view the underlying software and hardware models that are associated to the business application.

Application Services, Software Models, and Hardware Models headers are in bold font to distinguish them from the application service, software, and hardware model labels that are in hypertext.

## Procedure

1.  To navigate to the Business Application form and view the record details and update, click the business application label.

2.  To navigate to the Application Service form and update the record details, click the application service label.

3.  To navigate to the Software Model form directly from the TPM timeline, click the software model label.

    You can modify the lifecycle details of the software product \(product models of each full version\) in the form.

4.  To navigate to the Hardware form and to add or update the hardware lifecycle details in the Hardware Model Lifecycles related list, click the hardware label.

5.  To add a demand or project to a particular business application \(in the By Business Application view\) or to a software model \(in the By Software Model view\), point to the application or the software model and click the add new project or demand icon \(\) that appears next to the application or software model name.

    **Note:**

    You can create a project for a business application only when you activate PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

    In the New Demand form, you can see the business application name being auto-populated in the **Business Applications** field.

    You can add a demand to more than one business application. A demand \(that may or may not be initially attached to a business application\) can be attached to another business application as well.

    To add a demand to a business application, and view the demand in the timeline view of the TPM page:

    1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio Analysis** &gt; **Demands**.
    2.  Click open the demand.
    3.  Select the business application in the **Business Applications** choice list of the Demand form to which you want the demand to be added.
    4.  **Save** or **Update** the record.
    5.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Technology Portfolio Management \(TPM\)** &gt; **Technology Lifecycles** and refresh the timeline view of the TPM page.

        You can view the number of demands that are added to the business application. Click the arrow to expand and view the demand names.

        **Note:** The start and end date of the demand that is attached to a business application is plotted on the demand timeline. If only one date of the demand is present, either the start or end date, then that date is plotted as a point.


**Parent Topic:**[View technology risks in timeline - Legacy](view-technology-risks-in-timeline.md)

