---
title: Add business application lifecycle data using bubble chart
description: Create or edit the life cycle of a business application to manage the business application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-add-business-application-lifecycle-data.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use bubble chart view, Working with application rationalization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add business application lifecycle data using bubble chart

Create or edit the life cycle of a business application to manage the business application.

## Before you begin

The application model \(field name: Model ID\) is required to create an application model lifecycle for a business application. The application model ID can either be entered manually or can be automatically created and added to the business application by executing or scheduling the **CSDM Product Model Assignment** script. For details on how to run the **CSDM Product Model Assignment** script, see [Generate application models - Legacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/run-job-gen-model-id-ba.md).

Role required: sn\_apm.apm\_analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Application Rationalization page by selecting the application rationalization icon \(\[Omitted image "icon-app-rationalization.png"\] Alt text: Application rationalization icon.\).

3.  Select **Bubble chart**.

4.  Select the bubble for the relevant application that you want to add business application life-cycle data for and perform the following.

<table id="choicetable_ebc_3mq_fhc"><thead><tr><th align="left" id="d90063e111">

Bubble type

</th><th align="left" id="d90063e114">

Action

</th></tr></thead><tbody><tr><td id="d90063e120">

**Single bubble**

</td><td>

1.  Select a single bubble.
2.  In the pop-up window, select the context menu icon \(\[Omitted image "eaw-icon-menu.png"\] Alt text: Context menu icon.\) and select **Add lifecycle data**.

\[Omitted image "bubble-chart-menu-add-lifecycle-data.png"\] Alt text: Add lifecycle data button highlighted.

</td></tr><tr><td id="d90063e158">

**Grouped bubble**

</td><td>

1.  Select a grouped bubble. The info pane appears, displaying the list of individual business applications that are part of the grouped bubble.
2.  Select the context menu icon next to \(\[Omitted image "eaw-icon-menu.png"\] Alt text: Context menu icon.\) and select **Add lifecycle data**.

\[Omitted image "bubble-chart-grouped-add-lifecycle.png"\] Alt text: Add lifecycle data button highlighted for a grouped bubble.

</td></tr></tbody>
</table>5.  On the Application model life-cycle details form, fill in the fields.

    For a description of the field values, see [Application model life-cycle details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-application-model-lifecycle-details-form.md).

6.  Select **Create**.


**Parent Topic:**[Use bubble chart view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-using-app-rat-bubble-chart-view.md)

**Related topics**  


[Analyze applications using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-analyze-applications-by-capability.md)

[Create a demand using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-create-a-demand-using-the-bubble-chart.md)

[Set the planned disposition of a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-set-planned-disposition-of-a-business-application.md)

