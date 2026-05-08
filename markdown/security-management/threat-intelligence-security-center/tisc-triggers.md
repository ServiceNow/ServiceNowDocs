---
title: Webhook Triggers
description: Webhook triggers are used to filter the threat intelligence entities that needs to be tracked for any event changes such as Create, Update, and Delete.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Working with Webhooks, Administer, Threat Intelligence Security Center, Security Operations]
---

# Webhook Triggers

Webhook triggers are used to filter the threat intelligence entities that needs to be tracked for any event changes such as Create, Update, and Delete.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Webhooks Configurations** &gt; **Triggers**.

    The Webhooks Triggers page displays.

3.  Click **New**.

<table id="choicetable_cfv_dkn_zbc"><thead><tr><th align="left" id="d44902e97">

Field

</th><th align="left" id="d44902e100">

Description

</th></tr></thead><tbody><tr><td id="d44902e106">

**Name**

</td><td>

Enter a webhook trigger name.

</td></tr><tr><td id="d44902e115">

**Description**

</td><td>

Add the description of the webhook trigger.

</td></tr><tr><td id="d44902e124">

**Table**

</td><td>

Select the table for the webhook trigger.

</td></tr><tr><td id="d44902e133">

**Trigger Type**

</td><td>

Defines whether the configured webhook trigger is either create/update/delete event on the specified table.**Trigger Fields**: This is displayed when you select the **Trigger Type: Update**.

These are the list of fields on the record for which the update event needs to be tracked. If this is empty, then the event is considered for any field change on the record. For example, if the trigger fields are **Confidence** and **Reputation** for the **Observables** table, then this trigger is considered only when confidence or reputation fields are updated.

**Note:** The fields selected in the Exclusion Fields will not be available in the selection of Trigger Fields.

**Delete**: If the **Trigger Type: Delete** then the Exclusion Fields is not visible.

</td></tr><tr><td id="d44902e170">

**Exclusion Fields**

</td><td>

These are the set of fields which are excluded from the webhook trigger payload.

</td></tr><tr><td id="d44902e179">

**Filter Conditions**

</td><td>

Optional conditions that can be applied to filter the match records for any event trigger. For example, if threat severity is high and the Trigger Type is defined as Update on the Observable Table, then only those observables that are changed and where the threat severity is high are sent to the webhook URL.

</td></tr></tbody>
</table>4.  Click **Save**.

    By default, the trigger is created in the disabled state.

5.  Click **Enable** to enable the trigger and this trigger will be available for the webhooks to subscribe.

    **Note:** Click **Disable** to disable the enabled trigger and disabling will unsubscribe all the associated webhooks from this trigger.

6.  Click **View Sample Payload** to select the record.

    View the sample payload of that particular webhook trigger. Based on the selected table, those records from that specified table will be populated in the **Select Record** drop down list. Select the record to view the sample payload. The sample payload is shown in the JSON format. The fields in the payload are listed below.

7.  Select the type of record from the drop down list.

    The payload will be automatically changed based on the record selected.

    ```
    {
        "record": "Observable",
        "record_fields": {
            "additional_context": "This could be a potential malicious IP. ",
            "attack_phases": "Lockheed Martin: Command and Control",
            "author": "Anomali",
            "confidence": "50",
            "description": "This could be a potential malicious IP. ",
            "expiration_time": "2024-12-01T00:00:00.000Z",
            "first_observed": "2024-01-01T00:00:00.000Z",
            "first_seen": "2024-01-01T00:00:00.000Z",
            "id": "ipv4-addr--70526b0a436a02102164e0ea78b8f210",
            "is_defanged": "false",
            "is_false_positive": "false",
            "last_observed": "2024-01-01T00:00:00.000Z",
            "last_seen": "2024-01-01T00:00:00.000Z",
            "reputation": "suspicious",
            "source_count": "1",
            "status": "active",
            "sys_created_by": "SecCommon.System",
            "sys_created_on": "2024-06-04T00:00:00.000Z",
            "sys_id": "30526b0a436a02102164e0ea78b8f210",
            "sys_updated_by": "system",
            "sys_updated_on": "2024-06-15T00:00:00.000Z",
            "tags": "critical",
            "taxonomies": "MITRE: T121",
            "threat_level": "medium",
            "threat_score": "24",
            "threat_severity": "medium",
            "tlp": "CLEAR",
            "type": "ip_v4_address",
            "usage_categories": "APT",
            "value": "116.98.170.70"
        },
        "trigger": {
            "name": "Observable Update",
            "type": "UPDATE",
            "trigger_time": "2024-07-26T07:27:29.000Z",
            "trigger_fields": [
                {
                    "field_name": "confidence",
                    "previous_value": "30",
                    "current_value": "50"
                }
            ]
        }
    }
    
    ```

<table id="table_zlc_xgh_2cc"><thead><tr><th>

Parameter in Trigger Payload

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

record

</td><td>

String

</td><td>

Specifies the record type such as Observable or Indicator.

</td></tr><tr><td>

record\_fields

</td><td>

Object

</td><td>

Specifies the record fields snapshot when the event is generated. For list of supported fields, refer to the table in the below section.

</td></tr><tr><td>

trigger

</td><td>

Object

</td><td>

Specifies the matched trigger information.

</td></tr><tr><td>

trigger.name

</td><td>

String

</td><td>

Specifies the name of the trigger

</td></tr><tr><td>

trigger.type

</td><td>

String

</td><td>

Specifies the type of the trigger. Valid values are CREATE, UPDATE, DELETE.

</td></tr><tr><td>

trigger.trigger\_time

</td><td>

Date \(in ISO format with UTC timezone\)

</td><td>

Specifies the time of the event occurred on the record.

</td></tr><tr><td>

trigger\_fields

</td><td>

Array of Objects

</td><td>

This is available only for UPDATE trigger type. It specifies the list of trigger fields which got changed as part of the event occurred. The parameters inside **trigger\_fields** are: -   **field\_name**: provides the field name which got changed
-   **previous\_value**: provides the previous value of the field.
-   **current\_value**: provides the current value of the field.


</td></tr></tbody>
</table>    |Table|Column Name|Column Label|
    |-----|-----------|------------|
    |Campaign|aliases|Aliases|
    |Campaign|description|Description|
    |Campaign|first\_seen|First Seen|
    |Campaign|last\_seen|Last Seen|
    |Campaign|name|Name|
    |Campaign|objective|Objective|
    |Indicator|additional\_context|Additional Context|
    |Indicator|attack\_phases|Attack Phases|
    |Indicator|author|Author|
    |Indicator|confidence|Confidence|
    |Indicator|description|Description|
    |Indicator|expiration\_time|Expiration Time|
    |Indicator|first\_detected|First Detected|
    |Indicator|first\_observed|First Observed|
    |Indicator|first\_seen|First Seen|
    |Indicator|id|ID|
    |Indicator|indicator\_types|Indicator Types|
    |Indicator|ioc\_classification|IOC Classification|
    |Indicator|last\_observed|Last Observed|
    |Indicator|last\_seen|Last Seen|
    |Indicator|name|Name|
    |Indicator|pattern|Pattern|
    |Indicator|pattern\_type|Pattern type|
    |Indicator|pattern\_version|Pattern Version|
    |Indicator|platforms|Platforms|
    |Indicator|revoked|Revoked|
    |Indicator|source\_count|No of Sources|
    |Indicator|spec\_version|Spec Version|
    |Indicator|status|Status|
    |Indicator|tags|TISC Tags|
    |Indicator|taxonomies|Taxonomies|
    |Indicator|threat\_level|Threat Level|
    |Indicator|threat\_severity|Threat Severity|
    |Indicator|tlp|TLP|
    |Indicator|usage\_categories|Usage Categories|
    |Indicator|valid\_from|Valid From|
    |Indicator|valid\_until|Valid Until|
    |Malware|aliases|Aliases|
    |Malware|attack\_phases|Attack Phases|
    |Malware|description|Description|
    |Malware|executable\_process\_architectures|Process Architectures|
    |Malware|first\_seen|First Seen|
    |Malware|implementation\_languages|Implementation Languages|
    |Malware|is\_family|Is Family|
    |Malware|last\_seen|Last Seen|
    |Malware|malware\_capabilities|Malware Capabilities|
    |Malware|malware\_types|Malware Types|
    |Malware|name|Name|
    |Object \(Common Object Fields\)|additional\_context|Additional Context|
    |Object \(Common Object Fields\)|confidence|Confidence|
    |Object \(Common Object Fields\)|expiration\_time|Expiration Time|
    |Object \(Common Object Fields\)|id|ID|
    |Object \(Common Object Fields\)|revoked|Revoked|
    |Object \(Common Object Fields\)|source\_count|No of Sources|
    |Object \(Common Object Fields\)|spec\_version|Spec Version|
    |Object \(Common Object Fields\)|status|Status|
    |Object \(Common Object Fields\)|tags|TISC Tags|
    |Object \(Common Object Fields\)|taxonomies|Taxonomies|
    |Object \(Common Object Fields\)|threat\_level|Threat Level|
    |Object \(Common Object Fields\)|threat\_severity|Threat Severity|
    |Object \(Common Object Fields\)|tlp|TLP|
    |Observable|additional\_context|Additional Context|
    |Observable|attack\_phases|Attack Phases|
    |Observable|author|Author|
    |Observable|confidence|Confidence|
    |Observable|description|Description|
    |Observable|expiration\_time|Expiration Time|
    |Observable|first\_observed|First Observed|
    |Observable|first\_seen|First Seen|
    |Observable|id|ID|
    |Observable|is\_defanged|Is Defanged|
    |Observable|is\_false\_positive|Is False Positive|
    |Observable|last\_observed|Last Observed|
    |Observable|last\_seen|Last Seen|
    |Observable|reputation|Reputation|
    |Observable|source\_count|No of Sources|
    |Observable|status|Status|
    |Observable|tags|TISC Tags|
    |Observable|taxonomies|Taxonomies|
    |Observable|threat\_level|Threat Level|
    |Observable|threat\_score|Threat Score|
    |Observable|threat\_severity|Threat Severity|
    |Observable|tlp|TLP|
    |Observable|type|Type|
    |Observable|usage\_categories|Usage Categories|
    |Observable|value|Value|
    |Threat Actor|aliases|Aliases|
    |Threat Actor|description|Description|
    |Threat Actor|first\_seen|First Seen|
    |Threat Actor|goals|Goals|
    |Threat Actor|last\_seen|Last Seen|
    |Threat Actor|name|Name|
    |Threat Actor|personal\_motivations|Personal Motivations|
    |Threat Actor|primary\_motivation|Primary Motivation|
    |Threat Actor|resource\_level|Resource Level|
    |Threat Actor|secondary\_motivations|Secondary Motivations|
    |Threat Actor|sophistication|Sophistication|
    |Threat Actor|threat\_actor\_roles|Threat Actor Roles|
    |Threat Actor|threat\_actor\_types|Threat Actor Types|
    |Threat Report|description|Description|
    |Threat Report|name|Name|
    |Threat Report|published|Published|
    |Threat Report|report\_types|Report Types|
    |Vulnerability|affected\_software|Affected Software|
    |Vulnerability|description|Description|
    |Vulnerability|exploitation\_status|Exploitation Status|
    |Vulnerability|exploit\_exists|Exploit Exists|
    |Vulnerability|name|Name|
    |Vulnerability|published|Published|
    |Vulnerability|record\_last\_modified|Record Last Modified|
    |Vulnerability|severity|Severity|

    Below is the list of system fields that are applicable which are in common for every entity, and these are supported in the Webhook Trigger Payload for Create and Update triggers.

    -   sys\_id \(Sys ID\)
    -   sys\_created\_on \(Created\)
    -   sys\_created\_by \(Created By\)
    -   sys\_updated\_on \(Updated\)
    -   sys\_updated\_by \(Updated By\)
    **Note:** For the Delete, only sys\_id \(Sys ID\) is sent to webhook endpoint URL as part of the payload and other system fields are not supported.

    |Table|Column Name|Column Label|
    |-----|-----------|------------|
    |Observable|type|Type|
    |Observable|value|Value|
    |Indicator|name|Name|
    |Indicator|pattern|Pattern|
    |Indicator|pattern\_type|Pattern type|
    |Indicator|valid\_from|Valid from|
    |Campaign|name|Name|
    |Malware|is\_family|Is family|
    |Malware|name|Name|
    |Threat Actor|name|Name|
    |Threat Report|name|Name|
    |Threat Report|published|Published|
    |Vulnerability|name|Name|
    |Vulnerability|severity|Severity|


**Parent Topic:**[Working with Webhooks](tisc-webhooks.md)

**Related topics**  


[System properties for Webhooks](tisc-sysprops-retry.md)

[Configure webhooks](setup-webhooks.md)

