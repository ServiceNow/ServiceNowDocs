---
title: Define an attack mode/method
description: Attack modes and methods are imported with STIX data, but you can add new modes/methods, as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Attack modes and methods, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define an attack mode/method

Attack modes and methods are imported with STIX data, but you can add new modes/methods, as needed.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Attack Mode/Method**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_dsg_w5w_yt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select classification tag

</td><td>

If you set up and activated [classification tags](../../security-operations-common/task/create-class-group-and-tags.md) to add metadata to the record, you can select one or more tags to specify the degree of sensitivity of the attack mode/method. If you did not set up or activate classification tags, this drop-down list is not displayed.

</td></tr><tr><td>

Title

</td><td>

Enter a descriptive name for this attack mode/method.

</td></tr><tr><td>

Malware Type

</td><td>

Select the malware type for this attack mode/method. The available malware types are retrieved from the vendor server as STIX data.

</td></tr><tr><td>

Source

</td><td>

Select the threat data source for this attack mode/method. Some data sources are included with the base system. You can [create new data sources](../concept/c_GetStartedWithThreatIntel.md#) as needed.

</td></tr><tr><td>

Attack mechanism

</td><td>

Select the attack mechanism for this attack mode/method. Attack mechanisms represent the different techniques used to attack a system. The available attack mechanisms are retrieved from the vendor server as STIX data.

</td></tr><tr><td>

First Seen

</td><td>

This date is retrieved from the vendor server as STIX data.

</td></tr><tr><td>

Last Seen

</td><td>

This date is retrieved from the vendor server as STIX data.

</td></tr><tr><td>

Threat Actor Type

</td><td>

Select the threat actor type for this attack mode/method. Threat actor types characterize malicious actors \(or adversaries\) representing a cyber attack threat, including presumed intent and historically observed behavior. The available threat actor types are retrieved from the vendor server as STIX data.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the attack mode/method.

</td></tr><tr><td>

Handling

</td><td>

Enter instruction for how to handle this attack mode/method.

</td></tr><tr><td>

Intended effect

</td><td>

Enter the intended effect of this type of attack.

</td></tr></tbody>
</table>4.  Right-click in the form header and click **Save**.

    You can view any of the following related lists to view additional information.

    |Related List|Description|
    |------------|-----------|
    |Related Indicators|Lists related Indicators of Compromise \(IoC\) that have been identified by the threat source.|
    |Child Attack mode/method|Lists attack modes/methods that are children of the parent attack mode/method.|
    |Associated Tasks|Lists changes associated with the parent attack mode/method.|


**Parent Topic:**[Attack modes and methods](../concept/c_AttackModeMethod.md)

**Related topics**  


[Add an IoC to an attack mode/method](t_AddIoCToAttackMode.md)

[Add a related attack mode method](t_AddRelatedAttackMode.md)

[Add associated task to an attack mode/method](t_AddAssociatedTaskToAttackMode.md)

