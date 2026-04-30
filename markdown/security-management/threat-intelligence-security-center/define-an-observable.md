---
title: Define an Observable
description: Observables can be retrieved from scheduled feed ingestion or from the import assistant. However, you can create observables, as needed.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define an Observable

Observables can be retrieved from scheduled feed ingestion or from the import assistant. However, you can create observables, as needed.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Click **New**.

3.  Select the **Observable Type**.

    Create New Observable record form is displayed.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

4.  On the form, fill in the fields.

    **Note:** Whenever you either create a new observable or view the existing observables, the **Attachments** pane is by default displayed on the form view. You can either click the Attachments icon on the right-contextual menu or go to **Preferences** &gt; **Workspaces** and disable the **Show the sidebar**. For more information, see [Configure Next Experience Workspace preferences](https://servicenow.com/docs/bundle/washingtondc-platform-user-interface/page/get-started/servicenow-overview/task/next-experience-workspace-preferences.html).

<table id="table_hmw_qzm_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value

</td><td>

The value \(for example, IP address or hash\) associated with the observable.

</td></tr><tr><td>

Description

</td><td>

Description of the observable record.

</td></tr><tr><td>

Author

</td><td>

Enter the name.

</td></tr><tr><td>

Type

</td><td>

The observable classification type such as an IP address, domain name, artifact, directory, file, or hash.By default, this is displayed when you selected the new record.

</td></tr><tr><td>

Status

</td><td>

The active or inactive status of the observable.

</td></tr><tr><td>

Attack Phases

</td><td>

Represents attack phase in a kill chain such as LM, MITRE ATT&amp;CK.

</td></tr><tr><td>

TLP

</td><td>

Unique value that indicates the Data sensitivity setting per TLP.

</td></tr><tr><td>

Reputation

</td><td>

Specifies the malicious reputation of the observable.

</td></tr><tr><td>

Status

</td><td>

Enter the status of the observable if active or inactive.

</td></tr><tr><td>

Threat Score

</td><td>

Indicates the threat score for that observable.

</td></tr><tr><td>

Expiration Time

</td><td>

Specifies the expiration time of the observable record.

</td></tr><tr><td>

Source

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for this observable record.The confidence property identifies the confidence that the creator has in the correctness of their data. The confidence value MUST be a number in the range of 0-100.

</td></tr><tr><td>

Prevent System Updates

</td><td>

Setting this flag to true will prevent system from overriding values of fields on record.

</td></tr><tr><td>

Is False Positive

</td><td>

A boolean flag that indicates if observable is identified as false positive.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Resolves To|Specifies a list of references to one or more IP addresses or domain names that the domain name resolves to.|
    |Is FQDN|A fully qualified domain name\(FQDN\) is the complete address of an internet host or computer. It provides its exact location within the domain name system \(DNS\) by specifying the hostname, domain name and top-level domain \(TLD\).|

    |Field|Description|
    |-----|-----------|
    |Threat Level|Indicates the threat level of the observable record.|
    |First Seen|The time that this observable record was first seen performing malicious activities.|
    |Threat Severity|Indicates the threat severity of the observable record.|
    |Last Seen|The time that this observable record was last seen performing malicious activities.|
    |Usage Categories|Categories that the observable falls under, such as botnet or phishing.|
    |Attack Phases|Represents attack phase in a kill chain such as LM, MITRE ATT&amp;CK.|
    |Additional Context|Add any additional context.|
    |Sources|Specifies the threat source from which this record is created.|

    **Important:** **Source Reported Score**: This field contains the aggregated value of threat scores reported by the sources from which the observable is ingested. To see this field on the observable record form, you must add it manually, as it is not available by default.

    |Field|Description|
    |-----|-----------|
    |Resolves To|Specifies a list of references to one or more IP addresses or domain names that the domain name resolves to.|
    |Is FQDN|A fully qualified domain name\(FQDN\) is the complete address of an internet host or computer. It provides its exact location within the domain name system \(DNS\) by specifying the hostname, domain name and top-level domain \(TLD\).|

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
    |Notes|Add any additional notes for an observable record.|

5.  Click **Save**.

    After you save, a prompt message is displayed indicating that A new observable record is created. Click **Continue** to edit the record and create new relationships.

6.  Click **Continue**.

    **Important:** After you create a new observable record, **Prevent System Updates** check box is displayed.

    Select this check box to prevent any updates from the system after the observable or indicator or STIX objects records are created.

    |Field|Description|
    |-----|-----------|
    |Tags|
    |Select Tags|Select the tags that are associated with an observable.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select the Taxonomy that is associated with an observable.|
    |Add Taxonomy Values|Add the Taxonomy values that are associated with an observable.|

    |Field|Description|
    |-----|-----------|
    |The source records details for an observable are displayed, if any.|


## What to do next

Following table lists the related records related to the Observables:

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

List the campaigns that are related to this observable.

</td></tr><tr><td>

Infrastructure

</td><td>

List the Infrastructure such as systems, software services, and any associated physical or virtual resources that are related to this observable.

</td></tr><tr><td>

Intrusion Sets

</td><td>

List the intrusion sets such as a set of adversarial behaviors and resources with common properties that are related to this observable.

</td></tr><tr><td>

Malware

</td><td>

List the malware source records that are related to this observable.

</td></tr><tr><td>

Threat Actors

</td><td>

List the threat actors that are related to this observable.

</td></tr><tr><td>

Threat Events

</td><td>

List the threat events that are related to this observable.

</td></tr><tr><td>

Vulnerabilities

</td><td>

If the observable is an IP address, this list shows any resources \(configuration items\) that have a matching IP address that are related to this observable.

</td></tr></tbody>
</table>**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  Also, from the **Related Records** section, you can confirm the relationships between two Observables using the **Potential Relationships** section available on the **Observables** form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
3.  You can add observables to cases. For more information, see [Add to Case](add-to-case.md).
4.  You can also run enrichment actions to observables. For more information, see [Run Enrichment Actions within a case](run-enrichment-results.md).

**Parent Topic:**[Observables](../concept/observables.md)

