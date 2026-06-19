---
title: Configure domain separation for Vendor Management Workspace
description: Configure domain separation for Vendor Management Workspace to collect vendor scores and analyze the data for a specific domain. Configure domains for vendor score metric models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/vendor-management-workspace/config-domain-sep-vendor-management-configurable-workspace.html
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Domain separation and Vendor Management Workspace, Reference, Vendor Management Workspace, IT Service Management]
---

# Configure domain separation for Vendor Management Workspace

Configure domain separation for Vendor Management Workspace to collect vendor scores and analyze the data for a specific domain. Configure domains for vendor score metric models.

## Before you begin

Role required: pa\_data\_collector or admin

## Procedure

1.  Configure a domain to collect vendor score performance analytics data for that domain.

    1.  Navigate to **Performance Analytics** &gt; **Data Collector** &gt; **Domain Configurations**.
    2.  Create a domain configuration for Vendor Management Workspace
        1.  Click **New**.
        2.  In the **Name** field, enter a name for the configuration.
        3.  In the **Configuration type** menu, select **Conditions**.
        4.  In the Aggregate options section, select the **Collect children**check box to collect scores from all child domains.
    3.  Right-click the form header and click **Save**.
    4.  Add the following performance analytics jobs to the related list:

        **Note:** If you do not have the Jobs related list, you must configure the form to display the related list.

        -   VMW Scheduled Data Collection
        -   VMW Weight Collection
        -   VMW Daily Data Collection
        -   VMW Vendor Score Collection
    5.  Click **Update**.
    For more information on creating or scheduling a data collection job, refer to Create or schedule a data collection job

    **Note:** The Performance Analytics application:

    -   Runs the job and collects the score as the **Run as** user.
    -   Collects the scores only for the domain in which the logged-in user runs the job. The scores are not visible to vendor admins or vendor managers who are not part of that domain in Vendor Manager Workspace.
    -   Automatically adds database queries that limit results from the domain to the indicator source queries when the application runs a job for a domain configuration.
2.  Configure a domain to assign a vendor score metric model to a domain.

    1.  Navigate to **Vendor Manager Workspace** &gt; **Vendor Score Metric Models**
    2.  Do any of the following:
<table id="choicetable_uxc_zhx_5jb"><thead><tr><th align="left" id="d41183e200">

To

</th><th align="left" id="d41183e203">

Do this

</th></tr></thead><tbody><tr><td id="d41183e209">

**Configure the Vendor Score Metric Model list**

</td><td>

1.  Click the personalize icon.
2.  Move **Domain** from the **Available** to the **Selected** column.
3.  Click **OK**.


</td></tr><tr><td id="d41183e242">

**Configure a Vendor Score Metric Model form**

</td><td>

1.  From the list, select a vendor score metric model.
2.  Right-click the context menu icon and select **Configure &gt; Form Layout**. Make sure you are in the Vendor Manager Workspace section.
3.  Move **Domain** from the **Available** to the **Selected** column.
4.  Click **Save**.


</td></tr></tbody>
</table>
**Parent Topic:**[Domain separation and Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/vendor-management-workspace/domain-sep-vendor-management-workspace.md)

