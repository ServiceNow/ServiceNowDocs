---
title: Create a request from an incident
description: If a user needs catalog items such as an application or a laptop, create a request from the incident. Linking the request to the incident helps you track associated requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/create-request-from-incident.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Create a request from an incident

If a user needs catalog items such as an application or a laptop, create a request from the incident. Linking the request to the incident helps you track associated requests.

## Before you begin

Role required: itil or sn\_incident\_write

The Best Practice - Incident Resolution Workflow plugin \(com.snc.bestpractice.incident\) must be active to create a request from an incident.

To associate a parent incident with the request created for a record producer, the following script must be added to the script block of the record producer:

```
var incRPUtil = new LinkRecordProducerToIncident();
incRPUtil.linkRecordProducerToParentIncident(RP.getParameterValue('sysparm_req_parent'), current);

```

**Note:** If you set the **Use the sc\_layout driven cart macros \(default true\)** \(**glide.sc.use\_cart\_layouts**\) property to **false** and create a request from an incident, the request is not associated with the incident.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Select the required open incident.

3.  Select the Additional actions icon \[Omitted image "AdditionalActions.png"\] Alt text: and select **Create Request**.

    The Catalogs home page is displayed with all active catalogs that you can access.

    **Note:** If there is only one active catalog, then that catalog page is displayed with available categories.

4.  Select the required catalog and navigate through its categories and items.

5.  Check out the required catalog item, order guide, or record producer.

    For information on checkout models, see [Service Catalog checkout models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_EnableATwoStepCheckout.md).

    For a catalog item or order guide, a request is created and displayed under the **Requests** tab of the incident. For a record producer, the corresponding task is created and displayed under the **Problems** tab of the incident.

    **Note:**

    -   The associated incident is specified in the annotation message throughout the request process.
    -   For both one-step and two-step checkout, the caller of the incident is automatically set as the **Requested For** user for the request. If the two-step checkout is enabled, the fulfiller can change the **Requested For**.
    -   You can't add items to the wish list or save a record producer in this flow.

