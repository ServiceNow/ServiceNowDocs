---
title: Configure visit requirements
description: Configure requirements that visitors must fulfill for their visit to your organization.
locale: en-US
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2026-03-15"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Configure visit requirements

Configure requirements that visitors must fulfill for their visit to your organization.

## About this task

Visit requirements let you control what information visitors must provide before they check in. You can set different rules based on the location, visitor type, and other conditions.

As an admin, you create visit requirements to define the check-in steps visitors go through.

Each requirement can include the following types of additional information:

-   Extra questions to collect information from the visitor
-   Policies or documents the visitor must read and agree to
-   Files the visitor must upload, such as a photo

You can also set conditions so that only certain visits trigger a requirement. For example, you might require a photo ID only for visitors arriving at a highly secure campus.

## Before you begin

Role required: sn\_wsd\_visitor.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Visitor Management** &gt; **Administration** &gt; **Visit requirements**.

2.  On the Visit requirements list, select **New**.

3.  On the form, fill in the fields.

<table id="table_ekn_czm_p3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the requirement.

</td></tr><tr><td>

Is initial requirement

</td><td>

Option to display the requirement on the visit creation page. If this option is selected, the requirement is displayed on the visit creation page to the host and receptionist.

Initial requirements are displayed first in the Workplace Services Kiosk self-registration flow. For more information about self-registration, see [Self-register as a visitor](../../workplace-services-kiosk/task/visitor-self-register.md).

Initial requirements are used by the Workplace Concierge agentic workflow to create visits. For more information, see [Workplace Concierge agentic workflow](../../now-assist-wsd/concept/workplace-concierge-ai-agent.md).

If this option is not selected, the requirements appear later in the visit creation process based the conditions set in the **Apply if** section.

For example, a visitor name and email are initial requirements, while a visitor license plate or VIP status can be considered non-initial requirements.

</td></tr><tr><td>

Order

</td><td>

Order of the requirement in the pre-check tasks.

</td></tr><tr><td>

Active

</td><td>

Option to set the record to active.

</td></tr></tbody>
</table>4.  In the **Apply if** field, add conditions for when the requirement is applicable.

    The **Apply if** field is only available if **Is initial requirement** is not selected.

    For more information about conditions, see Condition builder.

    To include workplace locations within a parent location, you must add conditions to dot-walk from the nested locations to the parent location.

    To include all floors, areas, and spaces in Building A, add the following conditions.

    -   `Workplace Location is Building A` OR
    -   `Workplace Location.Floor.Building is Building A` OR
    -   `Workplace Location.Area.Building is Building A` OR
    -   `Workplace Location.Space.Building is Building A`
5.  Save the record.

    The visit requirement record is created.

6.  On the Additional information related list, select **New**.

    You can also select **New** on the Document to acknowledge or Document to upload related list.

7.  On the form, fill in the fields.

    For a description of the field values, see [Additional requirement form](../reference/additional-req-form.md).

8.  On the Acknowledgment tab, in the Policy field, select a policy record.

    The acknowledgment tab is displayed if the **Requirement type** is `Document to acknowledge`.

    For more information about creating policies, see [Create a visitor policy](create-visitor-policy.md).

9.  On the Field mapping tab, select a **Target table** and **Target field** to map the additional information.

    For example, **Company** information can be mapped to the **Organization** field of the Visitor \[sn\_wsd\_visitor\_visitor\] table.

10. Select **Submit**.


## What to do next

Create more records for additional information based on your preference. You can view the created records in the related lists of the Visit requirement record.

**Parent Topic:**[Configuring Workplace Visitor Management](../concept/configure-visitor-mgmt.md)

**Related topics**  


[Install Workplace Visitor Management](install-workplace-visitor-mgmt.md)

[Create a visitor policy](create-visitor-policy.md)

[Create a record producer for visitor management](create-rec-prodcr-visit-mgmt.md)

[Configure a visitor type](configure-visitor-type.md)

[Create a visitor badge template](create-visitor-badge-template.md)

[Configuring Workplace Visitor Management for Workplace Services Kiosk](../concept/config-visitor-for-kiosk.md)

[Quick start test for Workplace Visitor Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-wsd-visitor-mgmt.md)

