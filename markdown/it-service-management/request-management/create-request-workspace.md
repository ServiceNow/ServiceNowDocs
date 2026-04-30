---
title: Create a catalog request in Agent Workspace
description: You can create a catalog request in Agent Workspace to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.
locale: en-US
release: xanadu
product: Request Management
classification: request-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Use, Request Management, IT Service Management]
---

# Create a catalog request in Agent Workspace

You can create a catalog request in Agent Workspace to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.

## Before you begin

Role required: itil

You can create a catalog request in Agent Workspace to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.

-   To associate a request with any parent table record, the corresponding mapping configuration should be available in the **Catalog Administration** &gt; **Request Parent Mapping** submodule.
-   To associate a record producer request with the parent table record, retrieve the **sysparm\_parent\_sys\_id** and **sysparm\_parent\_table** parameters from the URL using the RP.getParameterValue\(\) method in the **Script** field of the record producer.
-   For the **Create Request** UI actions in workspace on the Interaction \[interaction\] table, the field values should be as follows:
    -   **Workspace Client Script**:

        ```
        function onClick() {
            var result = g_form.submit('sysverb_ws_save');
            if (!result) {
                // failed form submission 
                return;
            }
            result.then(function () {
                var params = {};
                params.sysparm_parent_table = "interaction";
                params.sysparm_parent_sys_id = g_form.getUniqueValue();
                g_service_catalog.openCatalogItem('sc_cat_item', '-1', params);
            });
        }
        ```

-   For the **Create Request** UI actions in workspace on the Incident \[incident\] table, the field values should be as follows:
    -   **Condition**: `current.incident_state != global.IncidentState.CLOSED && gs.hasRole("itil")`
    -   **Workspace Client Script**:

        ```
        function onClick() {
            g_form.submit('sysverb_ws_update').then(function () {
                var params = {};
                params.sysparm_parent_table = "incident";
                params.sysparm_parent_sys_id = g_form.getUniqueValue();
                g_service_catalog.openCatalogItem('sc_cat_item', '-1', params);
            });
        }
        ```


## Procedure

1.  Initiate a catalog request using any of the following options.

<table id="choicetable_khj_fll_zdb"><thead><tr><th align="left" id="d360694e121">

Option

</th><th align="left" id="d360694e124">

Steps

</th></tr></thead><tbody><tr><td id="d360694e130">

**From an incident using the Create Request UI action**

</td><td>

1.  From the List panel, select an open incident.
2.  In the **Details** tab, from the **More UI Actions** menu, select **Create Request**. The Service Catalog categories page is displayed with available categories.
3.  Navigate to a catalog item, order guide, or record producer that you want to order.

**Note:** You can only order items from the catalogs that are accessible.

</td></tr><tr><td id="d360694e162">

**From an incident using Agent Assist**

</td><td>

1.  From the List panel, select an open incident.
2.  In the **Details** tab, click the **Toggle Sidebar**.
3.  From **Agent Assist** in the contextual sidebar, search for the catalog item, order guide, or record producer that you want to request.
4.  Click **Order**.


</td></tr><tr><td id="d360694e198">

**From an interaction record**

</td><td>

1.  Select **Add New** &gt; **Interaction**.
2.  From the **More UI Actions** menu, select **Create Request**. The Service Catalog categories page is displayed with available categories.
3.  Navigate to a catalog item or order guide that you want to order.

**Note:** You can only order items from the catalogs that are accessible.

</td></tr></tbody>
</table>2.  Click **Order Now**.

    The Order Confirmation window is displayed.

    **Note:** The value in the **Request for** field is set by default depending on where the request is created:

    -   If the request is created from an incident, the value is set to the person who called in the incident.
    -   If the request was started from an interaction, the value is set to the person with whom the interaction is happening.
3.  Specify the **Delivery Information** and **Special instructions**.

4.  Click **Checkout**.

    The request is created and associated with the parent incident.

5.  Click **Close**.

6.  To view the created request, click **View Details**.


**Parent Topic:**[Agent Workspace for Request Management](../concept/agent-workspace-request-mgmnt.md)

