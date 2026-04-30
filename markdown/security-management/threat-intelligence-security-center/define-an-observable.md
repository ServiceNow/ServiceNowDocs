---
title: Define an Observable
description: Observables can be retrieved from scheduled feed ingestion or from the import assistant. However, you can create observables, as needed.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define an Observable

Observables can be retrieved from scheduled feed ingestion or from the import assistant. However, you can create observables, as needed.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Select **New**.

3.  Select the **Observable Type**.

    **Note:** When you create records for observables, indicators, entities, or objects, a source record is created and a prompt message appears that the new object record is created. You are then redirected to the aggregated record.

4.  On the form, fill in the fields.

    **Note:** When you create a new observable or view existing observables, the **Attachments** pane appears by default on the form view. You can select the Attachments icon on the right-contextual menu or go to **Preferences** &gt; **Workspaces** and disable **Show the sidebar**. For more information, see [Configure Next Experience Workspace preferences](https://servicenow.com/docs/bundle/washingtondc-platform-user-interface/page/get-started/servicenow-overview/task/next-experience-workspace-preferences.html).

<table id="table_hmw_qzm_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value

</td><td>

Value \(for example, IP address or hash\) associated with the observable.

</td></tr><tr><td>

Description

</td><td>

Description of the observable record.

</td></tr><tr><td>

Author

</td><td>

Name of the author.

</td></tr><tr><td>

Type

</td><td>

Observable classification type such as an IP address, domain name, artifact, directory, file, or hash.By default, this appears when you select the new record.

</td></tr><tr><td>

Status

</td><td>

Active or inactive status of the observable.

</td></tr><tr><td>

Attack Phases

</td><td>

Attack phase in a kill chain such as LM, MITRE ATT&amp;CK.

</td></tr><tr><td>

TLP

</td><td>

Unique value that indicates the data sensitivity setting per TLP.

</td></tr><tr><td>

Reputation

</td><td>

Malicious reputation of the observable.

</td></tr><tr><td>

Status

</td><td>

Status of the observable if active or inactive.

</td></tr><tr><td>

Threat Score

</td><td>

Threat score for that observable.

</td></tr><tr><td>

Expiration Time

</td><td>

Expiration time of the observable record.

</td></tr><tr><td>

Source

</td><td>

Threat source from which this record is created.

</td></tr><tr><td>

Confidence

</td><td>

Confidence for this observable record.The confidence property identifies the confidence that the creator has in the correctness of their data. The confidence value must be a number in the range of 0-100.

</td></tr><tr><td>

Prevent System Updates

</td><td>

Setting this flag to true prevents the system from overriding values of fields on the record.

</td></tr><tr><td>

Is False Positive

</td><td>

Boolean flag that indicates if the observable is identified as a false positive.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Resolves To|List of references to one or more IP addresses or domain names that the domain name resolves to.|
    |Is FQDN|Fully qualified domain name \(FQDN\) is the complete address of an internet host or computer. It provides its exact location within the domain name system \(DNS\) by specifying the hostname, domain name, and top-level domain \(TLD\).|

    |Field|Description|
    |-----|-----------|
    |Threat Level|Threat level of the observable record.|
    |First Seen|Time that this observable record was first seen performing malicious activities.|
    |Threat Severity|Threat severity of the observable record.|
    |Last Seen|Time that this observable record was last seen performing malicious activities.|
    |Usage Categories|Categories that the observable falls under, such as botnet or phishing.|
    |Attack Phases|Attack phase in a kill chain such as LM, MITRE ATT&amp;CK.|
    |Additional Context|Any additional context.|
    |Sources|Threat source from which this record is created.|

    **Important:** **Source Reported Score**: This field contains the aggregated value of threat scores reported by the sources from which the observable is ingested. To see this field on the observable record form, you must add it manually, as it isn't available by default.

    |Field|Description|
    |-----|-----------|
    |Resolves To|List of references to one or more IP addresses or domain names that the domain name resolves to.|
    |Is FQDN|Fully qualified domain name \(FQDN\) is the complete address of an internet host or computer. It provides its exact location within the domain name system \(DNS\) by specifying the hostname, domain name, and top-level domain \(TLD\).|

    **Note:** **Resolves To** and **Is FQDN** attributes are only applicable to the **Domain Name** type of observables.

<table id="table_bq3_ykh_ryb"><thead><tr><th>

Attribute Name

</th><th>

Attribute Types

</th></tr></thead><tbody><tr><td>

Artifact

</td><td>

-   Decryption Key
-   Encryption Algorithm
-   MD5 Hash
-   MIME Type
-   SHA1 Hash
-   SHA256 Hash
-   SHA512 Hash
-   URL


</td></tr><tr><td>

AS Number

</td><td>

-   Name
-   RIR


</td></tr><tr><td>

Directory

</td><td>

-   Directory Creation Time
-   Directory Last Accessed Time
-   Directory Last Modified Time
-   Encoded Path


</td></tr><tr><td>

Domain Name

</td><td>

-   Is FQDN
-   Resolves To


</td></tr><tr><td>

Email Address

</td><td>

-   Display name
-   Email Body
-   Email Recipients Bcc
-   Email Recipients Cc
-   Email Recipients To
-   Email Sender
-   Email Subject
-   Sent Date


</td></tr><tr><td>

File

</td><td>

-   Additional Information
-   Encoded File Name
-   File Created Time
-   File Last Accessed Time
-   File Last Modified Time
-   File Name Magic Number
-   MD5 Hash
-   MIME Type
-   SHA1 Hash
-   SHA256 Hash
-   SHA512 Hash


</td></tr><tr><td>

IPv4 Address

</td><td>

-   AS Number
-   MAC Address


</td></tr><tr><td>

IPv4 CIDR

</td><td>

-   AS Number
-   MAC Address


</td></tr><tr><td>

IPv6 Address

</td><td>

-   AS Number
-   MAC Address


</td></tr><tr><td>

IPv6 CIDR

</td><td>

-   AS Number
-   MAC Address


</td></tr><tr><td>

Network

</td><td>

-   Destination Bytes
-   Count Destination Packets Count
-   Destination Port
-   End Time
-   HTTP Message Body Length
-   HTTP Request Header
-   HTTP Request Method
-   HTTP Request Value
-   HTTP Request Version
-   ICMP Code Byte
-   ICMP Type Byte
-   Is Network Active
-   Is Socket Blocking
-   Is Socket Listening
-   Network Protocols
-   Socket Address Family
-   Socket Descriptor
-   Socket Handle
-   Socket Options
-   Socket Type Source Bytes Count
-   Source Packets Count
-   Source Port
-   Start Time
-   TCP Destination Flags
-   TCP Source Flags


</td></tr><tr><td>

Process

</td><td>

-   ASLR Enabled
-   Command Line
-   Current Working Directory \(CWD\)
-   DEP Enabled
-   Environment Variables
-   Is Hidden
-   Owner SID
-   Process ID
-   Priority
-   Process Created Time
-   Service Descriptions
-   Service Display Name
-   Service Group Name
-   Service Name
-   Service Start Type
-   Service Status Service Type
-   Startup Info
-   Windows Integrity Level
-   Window Title


</td></tr><tr><td>

Software

</td><td>

-   Common Platform Enumeration \(CPE\)
-   Supported Languages
-   Software Identification \(SWID\)
-   Vendor Version


</td></tr><tr><td>

User Account

</td><td>

-   Account Created Time
-   Account Expiry Time
-   Account Login
-   Account Type
-   Additional Information
-   Can Escalate Privileges
-   Credentials Last Changed Time
-   Display Name
-   First Login Time
-   Is Account Disabled
-   Is Privileged
-   Is Service Account
-   Last Login Time
-   User ID


</td></tr><tr><td>

Windows Registry Key

</td><td>

-   Key Modified
-   Time Registry Value
-   Subkeys Count


</td></tr><tr><td>

X.509 Certificate

</td><td>

-   Additional Information
-   Authority Key Identifier
-   Basic Constraints
-   Certificate Policies
-   CRL Distribution Points
-   Extended Key Usage
-   Inhibit Any Policy
-   Issuer
-   Issuer Alternative Name
-   Is Self Signed
-   Key Usage
-   Name Constraints
-   Policy Constraints
-   Policy Mappings
-   Private Key Usage Valid From
-   Private Key Usage Valid until
-   Signature Algorithm
-   Subject
-   Subject Alternative Name
-   Subject Directory Attributes
-   Subject Key Identifier
-   Subject Public Key Algorithm
-   Subject Public Key Exponent
-   Subject Public Key Modulus
-   Valid From
-   Valid Until
-   Version


</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Notes|Any additional notes for an observable record.|

5.  Select **Save**.

    After you save, a prompt message appears indicating that a new observable record is created. Select **Continue** to edit the record and create new relationships.

6.  To delete any observable record, select **Delete** to delete the aggregated record.

    When you select this action, it removes all the related records, except the original source data, and triggers reaggregation.

    **Note:** A confirmation message appears to verify that you want to delete the aggregated record. To also delete the source records and prevent reaggregation, select the **Delete Source Records** check box. This action removes all the associated source records.

7.  Select **Continue**.

    **Important:** After you create a new observable record, the **Prevent System Updates** check box appears.

    Select this check box to prevent any updates from the system after the observable, indicator, or STIX objects records are created.

    |Field|Description|
    |-----|-----------|
    |Tags|
    |Select Tags|Tags that are associated with an observable.|
    |Add Tags|New tags.|
    |Taxonomies|
    |Select Taxonomy|Taxonomy that is associated with an observable.|
    |Add Taxonomy Values|Taxonomy values that are associated with an observable.|

    |Field|Description|
    |-----|-----------|
    |Source records details for an observable appear, if any.|


## What to do next

The following table lists the related records related to the observables:

<table id="table_svf_lcn_2yb"><thead><tr><th>

Related List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Observable

</td><td>

List of observables related to this observable.**Note:** This section also contains the potential relationships between two observables. For more information, see [Confirm observable-observable potential relationship](define-observable-observable-potential-relationship.md)and see [Define observable-observable relationships](define-observable-observable.md) for the confirmed relationships between the two observables.

</td></tr><tr><td>

Indicators

</td><td>

List of indicators related to this observable.

</td></tr><tr><td>

Attack Patterns

</td><td>

List of attack patterns that are related to this observable.

</td></tr><tr><td>

Campaigns

</td><td>

Campaigns that are related to this observable.

</td></tr><tr><td>

Infrastructure

</td><td>

Infrastructure such as systems, software services, and any associated physical or virtual resources that are related to this observable.

</td></tr><tr><td>

Intrusion Sets

</td><td>

Intrusion sets such as a set of adversarial behaviors and resources with common properties that are related to this observable.

</td></tr><tr><td>

Malware

</td><td>

Malware source records that are related to this observable.

</td></tr><tr><td>

Threat Actors

</td><td>

Threat actors that are related to this observable.

</td></tr><tr><td>

Threat Events

</td><td>

Threat events that are related to this observable.

</td></tr><tr><td>

Vulnerabilities

</td><td>

If the observable is an IP address, this list shows any resources \(configuration items\) that have a matching IP address that are related to this observable.

</td></tr></tbody>
</table>**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  From the **Related Records** section, you can confirm the relationships between two observables using the **Potential Relationships** section available on the **Observables** form view. For more information, see [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
3.  You can add observables to cases. For more information, see [Add to Case](add-to-case.md).
4.  You can also run enrichment actions to observables. For more information, see [Run Enrichment Actions within a case](run-enrichment-results.md).

**Parent Topic:**[Observables](../concept/observables.md)

