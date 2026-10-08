---
title: Consumption rule evaluation
description: Consumption rules control which installations or users can consume a license. After you link a consumption rule to an entitlement, the license metric type determines how the system evaluates the rule during allocation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/consumption-rule-evaluation.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Consumption rule, software asset management consumption rule, device based metrics, user based metrics]
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Consumption rule evaluation

Consumption rules control which installations or users can consume a license. After you link a consumption rule to an entitlement, the license metric type determines how the system evaluates the rule during allocation.

Consumption rules restrict license consumption to specific organizational entities, such as a company, cost center, department, or country. You use consumption rules to allocate licenses to particular groups or locations within your organization. For example, a consumption rule could limit a license to users in the Finance department or devices in a specific company.

After you [create consumption rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-consumption-rule.md), you must [link them to entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/link-consumption-rules.md). When the system allocates a license, it evaluates each software installation against the linked consumption rule to determine whether that installation can consume a license from the entitlement.

The field that the system evaluates depends on the license metric allocation type configured on the entitlement. The system reads this field from the Software Installation \[cmdb\_sam\_sw\_install\] table.

|License metric allocation type|Field evaluated on the Software Installation record|
|------------------------------|---------------------------------------------------|
|Device-based \(for example, Per Core or Per Device\)|Installed on|
|User-based \(for example, Per User or User Subscription\)|Assigned to|

The license metric on the linked entitlement determines which field the system evaluates, regardless of the consumption rule values you set such as country, company, or cost center.

## Evaluation scenarios

-   **Per Device evaluation scenario**

    An entitlement uses the Per Device license metric and is linked to a consumption rule that specifies a company. When a software installation attempts to consume a license from this entitlement, the system checks the device's company. That device is the one referenced in the **Installed on** field of the Software Installation record.

    If the device's company matches the consumption rule's company, the installation can consume a license from the entitlement. If it doesn't match, the installation can't consume against that entitlement.

-   **Per User evaluation scenario**

    An entitlement uses the Per User license metric and is linked to a consumption rule that specifies a department. When a software installation attempts to consume a license from this entitlement, the system checks the user's department. That user is the one referenced in the **Assigned to** field of the Software Installation record.

    If the user's department matches the consumption rule's department, the installation can consume a license from the entitlement. If it doesn't match, the installation can't consume against that entitlement.


**Parent Topic:**[Exploring Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/explore-sam-workspace.md)

**Related topics**  


[Create consumption rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/create-consumption-rule.md)

[Link consumption rules to entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/link-consumption-rules.md)

