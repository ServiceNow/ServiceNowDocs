---
title: Define an observable
description: Observables are retrieved from the vendor server as STIX data. However, you can create observables, as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Observables, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define an observable

Observables are retrieved from the vendor server as STIX data. However, you can create observables, as needed.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Observables**.

2.  Click **New**.

    ![Add an observable](../../threat-intelligence-case-management/image/add-observable.png)

3.  Fill in the fields on the form, as appropriate.

<table id="table_hsg_w5w_yt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select classification tag

</td><td>

If you set up and activated [security tags](../../security-operations-common/task/create-class-group-and-tags.md) to add metadata to the record, you can select one or more tags to specify the degree of sensitivity of the observable. If you did not set up or activate security tags, this drop-down list is not displayed.

</td></tr><tr><td>

Value

</td><td>

The value \(for example, IP address or hash\) associated with the observable.**Note:** If a threat scan on an IP address or hash, returned malware or some other failure, the IP address or hash value is automatically added to the Observable \[sn\_ti\_observable\] table. As such, it can be searched for from the Observables form.

</td></tr><tr><td>

Observable type

</td><td>

Select the observable classification, such as an IP address or file hash. These observable types are defined in the **Observable Types** module.

</td></tr><tr><td>

Incident count

</td><td>

The number of times the observable value has been encountered.

</td></tr><tr><td>

Is composition

</td><td>

This field displays only after the observable record has been saved.If the **Observable Type** is set to anything other that **Observable Composition**, and this new observable is a composition, select this check box.

 If the **Observable Type** is already set to **Observable Composition**, the check box is selected and read-only.

 An observable composition is an observable that contains child observables.

</td></tr><tr><td>

Finding

</td><td>

Select one of the following:-   **Malicious**: Indicates that the observable is harmful to the organization.
-   **Suspicious**: Indicates that the observable might be harmful to the organization.
-   **Clean**: Indicates that the observable is not harmful to the organization.
-   **Unknown**: Indicates that we are yet to determine the observable's finding.
-   Default value: Unknown. For more information, see [Threat Lookup Finding Calculators](../concept/threat-lookup-finding-calculators.md).

 **Note:** After an upgrade, existing observables are marked Malicious.

</td></tr><tr><td>

Operator

</td><td>

This field appears only when the **Is composition** check box is selected. Depending on your setting in this field, the observables and their children are considered when deciding whether an associated indicator is present. Set this field to **AND** if all the child observables must be present for an associated indicator to be considered present.

 Set it to **OR** if any of the child observables are present for an associated indicator to be considered present.

</td></tr><tr><td>

Must not be present

</td><td>

This field displays only after the observable record has been saved.If selected, this field signifies that the absence of the observable is the potential issue \(for example, a missing registry key\).

</td></tr><tr><td>

Location

</td><td>

Using the settings in two properties and a script include definition, you can load [Load more IoC data](t_LoadAdditionalIoCData.md) in this field.

</td></tr><tr><td>

Notes

</td><td>

Enter any additional notes about the observable.

</td></tr></tbody>
</table>4.  Right-click in the form header and click **Save**.

    You can now click any of the following related lists to view additional information.

    |Related List|Description|
    |------------|-----------|
    |Related Indicators|Lists indicators that have been identified by the threat source.|
    |Associated Tasks|Lists changes associated with the observable.|
    |Child Observables|Lists related observables that have been identified by the threat source.|
    |Matching Resources for IP|If the observable is an IP address, this list shows any resources \(configuration items\) that have a matching IP address.|
    |Observable Sources|Lists the sources of this observable, along with the confidence level of the source.|
    |Security Annotations|Lists security annotations added to this observable.|


**Parent Topic:**[Observables](../concept/c_Observables.md)

**Related topics**  


[Add a related IoC to an observable](t_AddIoCToObserv.md)

[Add associated tasks to an observable](t_AddAssociatedTasksToObservable.md)

[Add a related observable](t_AddRelatedObservable.md)

[Load more IoC data](t_LoadAdditionalIoCData.md)

[Identify observable sources](t_IdentifyObservbleSources.md)

[Perform lookups on observables](perform-lookups-on-observables.md)

[Perform threat enrichment on observables](perform-enrich-on-observs.md)

