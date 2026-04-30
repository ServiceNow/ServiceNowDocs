---
title: Configure Manager Instances
description: Implement the following steps to configure the Manager Instances in Multi-Instance Management.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cross-instance application trust configuration, Configure, Multi-instance Management, Get started, Administer]
---

# Configure Manager Instances

Implement the following steps to configure the Manager Instances in Multi-Instance Management.

## Before you begin

Role required: admin or sn\_mif.mif\_admin.

## Procedure

1.  Log onto the instance that will be managed.

2.  Go to **Multi-Instance Management** &gt; **Manager Instances**.

    The Manager Instances list shows up.

    **Note:** sn\_mif\_managed\_by\_instance is the table for defining the manager instances.

    The manager instance table provides a list of multi-instance applications and the manager instances associated with each for trust configuration, for example, Impact Health.

3.  Select **New** to designate a manager.

    The Manager Instances form shows up.

4.  On the Manager Instances form, fill up the following.

<table id="choicetable_sps_q3z_42c"><thead><tr><th align="left" id="d285506e94">

Entry

</th><th align="left" id="d285506e97">

Description

</th></tr></thead><tbody><tr><td id="d285506e103">

**Manager Instance**

</td><td>

Select a manager instance from the list of instance names using the lookup option.**Note:** Only production instances should be designated as the primary managers for both production and sub-production instances. Sub-production instances may manage other sub-production instances under specific, defined conditions.

</td></tr><tr><td id="d285506e114">

**Application**

</td><td>

Select the appropriate application from the application list using the lookup option.

</td></tr></tbody>
</table>5.  Select **Submit**.


**Parent Topic:**[Cross-instance application trust configuration](../concept/grant-access-v2.md)

