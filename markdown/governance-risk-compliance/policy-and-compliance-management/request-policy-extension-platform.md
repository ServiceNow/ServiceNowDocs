---
title: Request an extension
description: Request an extension for the policy exception that you created.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage policy exceptions and extensions, Using the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Request an extension

Request an extension for the policy exception that you created.

## Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **My Policy Exceptions**.

2.  Open the policy exception for which you want to request extension.

    As a requester you can request extensions to a policy exception that is in Approved state more than once. Configure the **Number of extensions allowed for a policy exception** property to request policy extension multiple times.

    1.  To set up the property, navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Properties**

    2.  Enter the number in the **Number of extensions allowed for a policy exception** property.

        If you enter 20, then you can request 20 extensions for each policy exception.

        **Note:** If an extension request is rejected by the approver, then you can request another extension until the **Valid to** date is reached.

3.  Click the **Request Extension** button.

4.  On the pop-up, fill in the **Extension date**, **Extension reason**, and **Justification** fields.

    |Field|Descriptions|
    |-----|------------|
    |Extension date|Requested extension date, which is later than the **Valid to** date.|
    |Extension reason|Reason for extension.|
    |Justification|Statement of explanation for the request extension. Justification is also displayed in the **Additional comments** field of the **Comments** tab.|

5.  Click **Request**.

    You can see the policy extension details in the [Schedule tab of the Policy exception form](request-policy-exception.md#policy-ext-det) after the requester has requested for an extension and the extension has been approved by the approver.


**Parent Topic:**[Manage policy exceptions and extensions](../concept/manage-policy-exceptions.md)

