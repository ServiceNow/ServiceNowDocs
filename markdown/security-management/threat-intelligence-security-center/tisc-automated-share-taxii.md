---
title: Automated Sharing of TAXII Collections
description: Automated TAXII Collections automatically add intelligence records to TAXII Server Collections for seamless distribution to trusted external partners.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring TAXII Outbound Server, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Automated Sharing of TAXII Collections

Automated TAXII Collections automatically add intelligence records to TAXII Server Collections for seamless distribution to trusted external partners.

## Before you begin

Role required:

-   System Administrator \(view, create or edit\)
-   sn\_sec\_tisc.admin \(view\)

## About this task

The automated flow action adds the record provided in the inputs to TAXII server collections configured in the selected template. For more information, see [Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md).

Add record to TAXII Server Collection via automated process:

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Automated Flows**.

3.  Select **Automatically add threat intelligence to a TAXII collection** action link to view the respective rule details in the flow designer.

4.  View the flow designer action for the following triggers:

    ```
     Observable Created or Updated where (Type is IP address (V4), or Type is IP address (V6), or Type is Domain Name; and TISC Tags contains Add to: Sample Collection, and Reputation is Malicious, and Threat Score greater than or is 60)  Actions Select multiple
    ```

5.  Go to **Actions**

<table id="choicetable_ybr_fxh_qfc"><thead><tr><th align="left" id="d309118e141">

Action

</th><th align="left" id="d309118e144">

Description

</th></tr></thead><tbody><tr><td id="d309118e150">

**Sharing Template\[Outbound Intel Sharing\]**

</td><td>

Select the sharing template.Template with a usage mode of both **Automated addition to TAXII Collections** can be selected for Automated Sharing.

 For more information see, [Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md).

</td></tr><tr><td id="d309118e178">

**Observable Record \[Observable\]**

</td><td>

Select the type of observable record to add records to TAXII server collections.

</td></tr><tr><td id="d309118e187">

**Indicator Record \[Indicator\]**

</td><td>

Select the type of indicators record to add records to TAXII server collections.

</td></tr><tr><td id="d309118e196">

**Object Record \[Object\]**

</td><td>

Select the type of objects record to add records to TAXII server collections.

</td></tr><tr><td id="d309118e206">

**Include Related Records**

</td><td>

Select this check box to add the related records of the selected observables, including indicators and objects to TAXII server collections.

</td></tr></tbody>
</table>6.  Select **Done**.


## What to do next

Activate the flow.

**Parent Topic:**[Exploring TAXII Outbound Server](../concept/tisc-taxii-outbound-server.md)

**Related topics**  


[Create TAXII Collection](../concept/tisc-create-taxii-collection.md)

[Viewing TAXII Collection Records](../concept/tisc-view-taxii-collection.md)

[Create TAXII Collection](../concept/tisc-create-taxii-collection.md)

[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

