---
title: Set up the Incident Management form
description: Configure the Incident form to see the impact of an incident and then restore affected services. The CSDM framework enables you to view rich context for incidents: the CIs involved in the incident and the service offerings, business applications, and business services that the incident affects.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Applying CSDM guidelines to Incident Management, Configure, Incident Management, IT Service Management]
---

# Set up the Incident Management form

Configure the Incident form to see the impact of an incident and then restore affected services. The CSDM framework enables you to view rich context for incidents: the CIs involved in the incident and the service offerings, business applications, and business services that the incident affects.

## Before you begin

Role required: admin

## About this task

Incident Management leverages the CSDM data structure to display information that assists in solving the incident.

[Go to the 1:00:00 mark on this video](https://www.youtube.com/watch?v=EbuHgr10P98&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=57) to learn about setting up the Incident form to include the related lists that leverage the CSDM framework.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Administration** &gt; **Incident Properties**.

2.  In the Incident Related List Properties section, enable the following properties and then select **Save**.

    -   **Populate Impacted Services based on Affected CIs**. This property enables display and update of the **Impacted Services/CIs** related list when you perform the **Refresh Impacted Services** action.
    -   **Populate the Business Application related list for incidents**
    -   **Populate the Service Offering related list for incidents**
    The properties are fully described in [Incident Management properties](../reference/incident-management-properties.md).

3.  Ensure that the **Principle Class** option is selected for the CI or CI class as described in [Create a CI class](https://www.servicenow.com/docs/access?context=t_CreateCIType&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) and [Update the list of classes in the Principal Class filter](https://www.servicenow.com/docs/access?context=update-principal-class-filter&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

4.  Navigate to **All** &gt; **Incident** &gt; **Open** and fill in the following fields:

<table id="table_qyz_qjm_pwb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Service

</td><td>

The business service or technical service associated with the incident. The value that you specify narrows the list of available CIs that appear for selection in the **Configuration Item** field.

 **Note:** Narrowing the list of available CIs isn't a feature of the base system. To narrow the list, you must specify values for **Service** and **Service Offering**.

</td></tr><tr><td>

Service Offering

</td><td>

The business service offering \(product\) or technical service offering associated with the incident. The value that you specify narrows the list of available CIs that appear for selection in the **Configuration Item** field.

 **Note:** Narrowing the list of available CIs isn't a feature of the base system. To narrow the list, you must specify values for **Service** and **Service Offering**.

</td></tr><tr><td>

Configuration Item

</td><td>

The CI or the affected service. \(Hardware, application, and cloud \[physical CIs\] or application service \[logical CIs\]\)

 You can then use the CI to identify details for incident routing. For example, you can use the CI data like Support Group and provide information about the service impact by using dependency relationships.

</td></tr></tbody>
</table>    ![Incident form with numbered fields.](../image/incident-form-use-case.png)

5.  Review the information.

    -   The CIs that may have caused the incident appear in the **Affected CIs** related list \[task\_ci\].
    -   The services and service offerings that are related to the populated CI appear in the **Impacted Services/CIs** related list \[task\_cmdb\_ci\_service\].
    -   The services and CIs impacted by the incident appear in the **Impacted Services/CIs** related list \[task\_cmdb\_ci\_service\].

**Parent Topic:**[Applying CSDM guidelines to Incident Management](../concept/itsm-incident-use-case-product-view.md)

