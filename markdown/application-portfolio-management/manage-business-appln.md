---
title: Add or edit a business application
description: Use the Business application form to add the applications that your organization uses based on their functions and the business processes they fulfill. In Enterprise Architecture, add any business application that is used to assess and track costs, usage, business value, functional fitment, and risks.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add or edit a business application

Use the Business application form to add the applications that your organization uses based on their functions and the business processes they fulfill. In Enterprise Architecture, add any business application that is used to assess and track costs, usage, business value, functional fitment, and risks.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy business applications module is moved to the Enterprise Architecture Workspace. To learn more, see [Add or edit a business application](eaw-task/eaw-create-business-app.md).

If you have an Enterprise Architecture user role \(sn\_apm.apm\_user\), use the Business Application Life-cycle Management services to request, add, or retire a business application.

**Note:** The Business Application form manages logical application information. Technology certifications and infrastructure components, such as servers, are maintained through related records including technology models, application services, and CMDB relationships.

Role required: sn\_apm.apm\_analyst

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **All Business Applications**.

2.  Select **New** to add a new application or select the name of an existing application that you want to edit.

3.  On the form, fill in the fields.

    For field information, see [Business Application Form](../reference/business-application-form.md).

4.  Select **Submit** or **Update**.

5.  To [relate a business application to an application service using the CI relationship editor](relate-business-application-to-business-service.md), select the Add CI relationship \(![CI relationship editor icon](../image/RelationshipEditorIcon.png)\) icon in the **Related Items** section.

    Business applications are related to application services, and application services are related to servers and infrastructure through the CMDB. To associate servers with a business application, relate the application to an application service and verify the application service is linked to the appropriate servers in the CMDB.

6.  To [view the roadmap of the business application](view-business-application-roadmap.md) and its related data, select **View Application Roadmap**.

    You have to activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin to view the business application roadmap.

7.  To get all the available and significant information of a business application, select [Application 360](applications-360-dashboard.md).

8.  To know the application cost in the last period, manage application cost as a percentage of total spend, determine its future trend, and provide a cost-effective business application, select **Application TCO**.

    For more information, see Application TCO.

    **Note:**

    The link to the Application TCO dashboard works when you use the preconfigured **Business Application Costing** cost model. The integration works when you activate the Enterprise Architecture plugin \(com.snc.apm\) and Financial Management for APM \(com.snc.financial\_management\_for\_apm\) plugin. By default, the Performance Analytics – Content Pack – Enterprise Architecture \(com.snc.pa.apm\) plugin gets activated as part of the Enterprise Architecture plugin \(com.snc.apm\) activation.

    For the Financial Management for APM \(com.snc.financial\_management\_for\_apm\) plugin, reach out to one of the Partner Store Apps. Your ServiceNow implementation partner could help you with the Partner Store App details.

9.  To raise a demand for the business application, select **Create Demand**.

    The Demand form that opens up populates the related business application in the **Business Applications** field.

10. To retrieve [software models associated to the business application](../concept/software-models-suggestions-application-service.md), select **Manage Technology Models**.

    It also retrieves the log of software models that the software models suggestion engine retrieved when the scheduled job was last executed.

    Operating system and technology certifications are derived from the Technology Reference Model \(TRM\). Use Manage Technology Models to associate approved software or operating system models with the business application. Certification status is determined by the lifecycle and compliance information defined in the TRM.

    Business applications are related to application services, and application services are related to the underlying servers and infrastructure through the CMDB. To associate servers with a business application, relate the business application to an application service.

11. To navigate to the timeline view of the business application and to view the timeline of all its associated epics, stories, enhancements, other stories, projects, and demands, select the additional actions icon \(![Additional actions icon](../image/AdditionalActionsIcon.gif)\) and configure UI actions to display the **View Application Backlog** button.

    Select the button to go to the Application backlog view of the timeline.

    For more information on this timeline view, see [Application Backlog view](../concept/tpm-by-app-unified-backlog.md).


## What to do next

To have a complete view of the business applications, select the [Application 360 dashboard](applications-360-dashboard.md).

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

