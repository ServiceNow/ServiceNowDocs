---
title: Redirection to the right case type
description: Create a proactive case from an incident in the Proactive Service Experience Workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/proactive-service-exp-workflows/product-support-for-technology/generate-proactive-cases.html
release: zurich
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Auto-creation of cases, Use, Proactive Service Experience Workflows]
---

# Redirection to the right case type

Create a proactive case from an incident in the Proactive Service Experience Workflows.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  In Service Operations Workspace, navigate to **List** &gt; **Incidents** &gt; **All**.

3.  Select the incident from the list.

4.  In the **Overview** tab, expand the **Impact** section.

5.  Select a **Cases** tile.

6.  Select the **Generate Proactive Cases** button.

7.  Set the property sn\_csm\_case\_types.service\_definition\_select \[sys\_properties table\] to true, to automatically create the case.

    If the sn\_csm\_case\_types.service\_definition\_select \[sys\_properties table\] property is set to false, cases aren’t created automatically.

8.  Select the appropriate service definition from the list.

    **Note:** The fibre broadband service definition as been shipped as a part of the demo data.

    For more information about service definition, see [Service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-service-definitions.md).

9.  Select the **Recommended Services**.

    The **Recommended Services** shows the service definitions that are linked to the **Impacted Services/CIs**.

    For more information about how to create record producer, see [Record Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/service-catalog/c_RecordProducer.md).

10. Select **Create proactive cases**.


**Parent Topic:**[Auto-creation of cases and updates from incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/proactive-service-exp-workflows/product-support-for-technology/psew-auto-creation-case.md)

