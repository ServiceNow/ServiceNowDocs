---
title: Create a request from an incident
description: When you work on an incident and determine that the user needs one or more catalog items, such as an application or a new laptop, you can create a request from the incident. It helps you in tracking the requests associated with an incident and vice versa.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Create a request from an incident

When you work on an incident and determine that the user needs one or more catalog items, such as an application or a new laptop, you can create a request from the incident. It helps you in tracking the requests associated with an incident and vice versa.

## Before you begin

Role required: itil or sn\_incident\_write

The Best Practice - Incident Resolution Workflow plugin \(com.snc.bestpractice.incident\) should be active for creating a request from an incident. To associate a parent incident with the request created for a record producer, the catalog\_admin should add the following script in the script block of the record incident.

To associate a parent incident with the request created for a record producer, the administrator should add the following script in the script block of the record producer:

```
var incRPUtil = new LinkRecordProducerToIncident();
incRPUtil.linkRecordProducerToParentIncident(RP.getParameterValue('sysparm_req_parent'), current);

```

**Note:** If you set the **Use the sc\_layout driven cart macros \(default true\)** \(**glide.sc.use\_cart\_layouts**\) property to **false** and create a request from an incident, the request is not associated with the incident.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Select the required open incident.

3.  Click the additional actions menu icon ![Additional actions menu icon.](../image/AdditionalActions.png) and select **Create Request**.

    The Catalogs home page is displayed with all active catalogs that you can access.

    **Note:** If there is only one active catalog, then that catalog page is displayed with available categories.

4.  Select the required catalog and navigate through its categories and items.

5.  Check out the required catalog item, order guide, or record producer.

    For information on checkout models, see [Service Catalog checkout models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_EnableATwoStepCheckout.md).

    For a catalog item or order guide, a request is created and displayed under the **Requests** tab of the incident. For a record producer, the corresponding task is created and displayed under the **Problems** tab of the incident.

    **Note:**

    -   The associated incident is specified in the annotation message throughout the request process.
    -   Both for the one-step and two-step checkout, the caller of the incident is automatically set as the **Requested For** user for the request. If the two-step checkout is enabled, the fulfiller can change the **Requested For**.
    -   You cannot add items to the wish list, or save a record producer in this flow.

