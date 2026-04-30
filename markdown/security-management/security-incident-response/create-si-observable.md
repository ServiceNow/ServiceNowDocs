---
title: Create a security incident observable
description: You can create and view an observable within a security incident and take appropriate action. Having observables available in the security incident is scalable and reduces response time.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a security incident observable

You can create and view an observable within a security incident and take appropriate action. Having observables available in the security incident is scalable and reduces response time.

## Before you begin

Role required:

-   sn\_ti\_observable.write \(write\)
-   sn\_ti\_observable.read \(read\)
-   sn\_ti\_observable.admin \(delete\)

## Procedure

1.  Navigate to **Security Incident**.

2.  Choose an incident.

3.  Click **Security Incident Observables** related list tab.

4.  Click **New**.

5.  Fill in the fields on the form, as appropriate.

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
-   Default value: Unknown. For more information, see [Threat Lookup Finding Calculators](../../threat-intelligence/concept/threat-lookup-finding-calculators.md).

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

Using the settings in two properties and a script include definition, you can load [Load more IoC data](../../threat-intelligence/task/t_LoadAdditionalIoCData.md) in this field.

</td></tr><tr><td>

Notes

</td><td>

Enter any additional notes about the observable.

</td></tr></tbody>
</table>6.  Right-click in the form header and click **Save**.

    You can now click any of the following related lists to view additional information.

    |Related List|Description|
    |------------|-----------|
    |Related Indicators|Lists indicators that have been identified by the threat source.|
    |Associated Tasks|Lists changes associated with the observable.|
    |Child Observables|Lists related observables that have been identified by the threat source.|
    |Matching Resources for IP|If the observable is an IP address, this list shows any resources \(configuration items\) that have a matching IP address.|
    |Observable Sources|Lists the sources of this observable, along with the confidence level of the source.|
    |Security Annotations|Lists security annotations added to this observable.|

7.  Returning to the security incident the following information is available.

    **Note:** When you add an observable to the security incident, the system checks for any other configuration items or users associated with it. The **Related Configuration Items** and **Related Users** related list tabs are updated accordingly.

    ![Security incident observables example](../image/SI_Observable.png)

<table id="table_bmj_3ky_gv"><thead><tr><th>

Column

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Observable

</td><td>

The value \(for example, IP address or hash\) associated with the observable.

</td></tr><tr><td>

Observable Type

</td><td>

The specific type of observable.

</td></tr><tr><td>

Context

</td><td>

Selected by the user. Choices are:-   IP - Source or Destination

**Note:** If Threat Intelligence and Palo Alto Networks - Firewall are activated, changing or adding a value to this field causes the [Get Log Data Flow](../../secops-integration-sir/secops-integration-palo-alto-firewall/task/get-threat-log-data.md#) [Security Operations Palo Alto Networks - Get Log Data](../../secops-integration-sir/secops-integration-palo-alto-firewall/task/get-threat-log-data.md#) workflow to execute. The workflow retrieves enriched threat log data from the firewall and attaches it to the security incident. The information is also parsed and displayed in the [Firewall Logs](t_ManuallyCreateSecurityIncident.md) section under the **Enrichment Data** tab.

-   URL - Referrer

**Note:** When the user clicks a link in a phishing email, a referrer is the URL of the final jump before the malware URL is accessed.

</td></tr><tr><td>

Incident Count

</td><td>

The number of incidents that this observable appears in. This value is automatically updated when the observable is added to another incident manually or through a workflow.

</td></tr><tr><td>

Updated

</td><td>

Data and time the list was last updated.

</td></tr></tbody>
</table>    **Note:** If the Threat Intelligence plugin is installed, you can also view the observable in the **Observables** list in the **IoC Repository**.


**Related topics**  


[Edit a security incident observable list](edit-si-observable.md)

[Add multiple security incident observables](add-multiple-si-observables.md)

