---
title: Configure how an automatic event is created
description: Configure the ServiceNow AI Platform to automatically create events in MISP.Configure the event trigger conditions in the ServiceNow AI Platform so that you can automatically trigger an event in MISP when the conditions are met.Map the MISP event fields in the ServiceNow AI Platform so that security incident information is available when MISP events are created.Map the Security Incident Response observable types to the MISP attribute types because the MISP attribute types and the SIR observables may be different.Synchronize the MITRE-ATT&amp;CK information with MISP attributes for better security incident and threat analysis.Add MISP tags to the created MISP events.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Configure how an automatic event is created

Configure the ServiceNow AI Platform to automatically create events in MISP.

## Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) that are required for using the MISP bi-directional features.
-   Role required: sn\_si.admin, sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **MISP Integration** &gt; **Automatic Event Creation Profiles**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_tzj_2ls_lqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the automatic event creation profile.

</td></tr><tr><td>

Description

</td><td>

Brief description about the profile. A more detailed description is shared through the attributes in the next stage of the event's creation.

</td></tr><tr><td>

Order

</td><td>

Order of the profile when triggering conditions are met. The default is 100. Leave this setting at the default.If you create multiple profiles, this value provides a run-time execution priority when two or more profiles share triggering conditions. The profile with the lowest number has the highest priority.

</td></tr><tr><td>

Source

</td><td>

MISP source for the event creation.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the profile is active or inactive. The option is cleared by default to indicate that the profile is turned off.This profile is not active until you complete all the profile configuration steps and click **Finish**.

</td></tr></tbody>
</table>4.  Click **Continue**.


**Parent Topic:**[MISP administration](../concept/misp-administration.md)

**Related topics**  


[Getting started with MISP integration for Security Operations](../reference/get-started-with-misp-integration-for-security-operations.md)

[Install and configure the MISP integration for Security Operations](install-and-configure-misp.md)

[Review the MISP integration settings](review-the-misp-integration-settings.md)

[Configure MISP sighting searches](configure-sightings-search.md)

[MISP event data](../concept/misp-event-data.md)

[Associated MISP events](../reference/associated-misp-events.md)

[MISP user information](../reference/misp-user-information.md)

[Domain separation and MISP](../reference/domain-separation-and-misp.md)

[Troubleshooting MISP integration](../reference/troubleshooting-misp-integration.md)

## Configure event trigger conditions

Configure the event trigger conditions in the ServiceNow AI Platform so that you can automatically trigger an event in MISP when the conditions are met.

### Before you begin

Role required: sn\_sec\_misp.write

### Procedure

1.  On the Trigger Conditions form, fill in the details that can trigger an event.

    You can build a compound logic by providing the trigger conditions that are based on security incident fields or observable fields. You can also create events in MISP if observables don't have a corresponding event in MISP. You can choose to build a compound logic by using a combination of the three trigger conditions - Trigger based on security incident fields, Trigger based on observable fields, and Create MISP event, if an observable doesn't have corresponding events in MISP. If you select multiple triggers, you can join them by using the AND condition. Consider creating a profile with new conditions if you must use the OR condition.

<table id="table_bkc_wps_lqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger based on security incident fields

</td><td>

MISP event that you can create if all the security incident trigger conditions are met.

</td></tr><tr><td>

Security Incident Trigger Conditions

</td><td>

Filters in the first row that you can set by using the lists and fields of the conditions builder. To add more conditions, click AND or OR. If AND is selected, all conditions must be matched. If OR is selected, either condition can be matched.To set a second filter condition, click **New Criteria**.

</td></tr><tr><td>

Trigger based on observable fields

</td><td>

MISP event that you can create if all the observable trigger conditions are met.

</td></tr><tr><td>

Observable Trigger Conditions

</td><td>

Filters in the first row that you can set by using the lists and fields of the conditions builder. To add more conditions, click AND or OR. If AND is selected, all conditions must be matched. If OR is selected, either condition can be matched.To set a second filter condition, click **New Criteria**.

</td></tr><tr><td>

Create MISP event if observable doesn't have corresponding events in MISP

</td><td>

MISP event that you can create if an observable doesn't have corresponding events in MISP.

</td></tr></tbody>
</table>    The following example shows the event trigger conditions as you set up the MISP event creation profile.

    ![Configure conditions that are based on an event that is created in MISP.](../image/misp-event-trigger-conditions.png "Event trigger conditions")

2.  Click **Continue**.


## Map the MISP event fields

Map the MISP event fields in the ServiceNow AI Platform so that security incident information is available when MISP events are created.

### Before you begin

Role required: sn\_sec\_misp.write

### Procedure

1.  On the form, fill in the fields.

<table id="table_lk1_5ss_lqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event Info

</td><td>

Event information that is automatically created from the ServiceNow AI Platform Security Incident Response.The **Event Info** field supports substitution variables by using $⁠\{SIR FIELD LABEL\}$. During an event creation, these variables are replaced with the actual security incident field values. The $\{URL\}$ substitution variable is replaced with the URL of the security incident.

</td></tr><tr><td>

Distribution

</td><td>

Option that controls who can view this event after the event is published. This option also controls whether the event is synchronized to other servers. The distribution is inherited by the attributes, and the most restrictive setting wins. The distribution options are as follows: -   Your organization only: Enables only members of your organization to view this event. The event can be pulled to another instance by one of your organization members where only your organization can have the access to view it. Events with this setting are not synchronized.
-   This community only: Enables users that are part of your MISP community to view the event, including your own organization, organizations on this MISP server, and organizations that run MISP servers that synchronize with this server. Any other organizations that connect to your linked servers are restricted from viewing the event.
-   Connected communities: Enables users that are part of your MISP community to view the event including all organizations on this MISP server, all organizations on the MISP servers that synchronize with this server, and the hosting organizations of servers that connect to any server that is two hops away. Any other organizations that are connected to the linked servers that are two hops away are restricted from viewing the event.
-   All communities: Shares the event with all MISP communities.


</td></tr><tr><td>

Threat Level

</td><td>

Field that indicates the risk level of the event. You can categorize incidents into three different threat categories \(low, medium, high\). This field can also be left as undefined. The following are the options: -   Low: General mass malware
-   Medium: Advanced Persistent Threats \(APT\)
-   High: Sophisticated APTs and 0-day attacks


</td></tr><tr><td>

Analysis Status

</td><td>

Current stage of the analysis for the event, with the following possible options: -   Initial: The analysis is just beginning
-   Ongoing: The analysis is in progress
-   Completed: The analysis is complete


</td></tr></tbody>
</table>    The following example shows the form that you can use to create an event in MISP.



    ![Configure the form to create a new event in MISP.](../image/misp-event-field-mapping.png)

2.  Click **Continue**.


## Map or associate SIR observables as attributes to MISP events

Map the Security Incident Response observable types to the MISP attribute types because the MISP attribute types and the SIR observables may be different.

### Before you begin

Role required: sn\_sec\_misp.write

### About this task

The MISP integration for Security Operations provides a base system mapping that you use when you add SIR observables as attributes to a MISP event.

You can choose to modify the base system mapping to suit your environment. For example, you can map multiple SIR observables to only one MISP attribute type. If any observable types are not mapped, the **other** MISP attribute type is selected by default.

### Procedure

1.  On the Additional Options form, map the SIR observable and MISP attribute types.

2.  Map the Security Incident Response observable types to the MISP attribute types as described in the following table.

<table id="table_okz_5ws_lqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add all associated observables as attributes

</td><td>

Option that you enable to add available observables in a security incident to a MISP event as attributes.This option enables the mapping in the Observable Type to Attribute Type Mapping section.

</td></tr><tr><td>

Observable Type To Attribute Type Mapping

</td><td>

Option to map the SIR observable types to the MISP attribute types. For example, you can map the CVE Number in SIR to the vulnerability attribute in MISP.You can add a SIR observable type to only one MISP attribute type.

 The base system provides a mapping of the SIR observable types to the MISP attribute types.

 If any SIR observable types are not mapped to a MISP attribute type, then the observable is mapped to the **other** attribute type in MISP.

 To add a new mapping, click **Add Observable Type**, search for the SIR observable type, and then map to the corresponding MISP attribute type.

 Click the Remove Mapping icon ![Remove mapping.](../image/misp-remove-mapping.png) to remove the SIR and MISP attribute mapping association.

 **Note:** For more information on MISP attribute types, see the [MISP documentation](https://www.circl.lu/doc/misp/categories-and-types/#types).

</td></tr><tr><td>

Filter observables based on security tags

</td><td>

Option to filter the observables based on the selected security tags.**Security tags**: Add tags to filter the observables. For example, if you are adding a tag called 'Block from sharing' or 'TLP: White' then if one of the observables has any of these tags associated then these observables will not be added as an attribute to the MISP event during the MISP event creation.

</td></tr><tr><td>

Set attribute IDS flag when observable finding is malicious

</td><td>

Option that lets you know that if an observable is marked as malicious in SIR, then the corresponding attribute in MISP has the IDS flag enabled. If the IDS flag is not set, the attribute is considered as contextual information and is not used for automatic intrusion detection.

</td></tr></tbody>
</table>    The following example shows how to navigate to the additional options page. On this page, you can enable the SIR observables and MISP attribute types mapping, add new SIR observable types, such as the IPV6 network and IPV4 network, and map it to the MISP attribute type domain IP address.



    ![Map SIR observable and MISP attribute type.](../image/misp-attribute-mapping.gif)


## Synchronize MITRE-ATT&amp;CK information to MISP events

Synchronize the MITRE-ATT&amp;CK information with MISP attributes for better security incident and threat analysis.

### Before you begin

Role required: sn\_sec\_misp.write

### Procedure

1.  On the Additional Options form, review the options to synchronize the MITRE-ATT&amp;CK information with the MISP attributes.

<table id="table_l3g_c1t_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sync Security Incident MITRE-ATT&amp;CK™ techniques as local galaxies to MISP event

</td><td>

Option to synchronize the ServiceNow AI Platform SIR security incident MITRE-ATT&amp;CK™ techniques as local galaxies in the MISP event.**Note:** To add local galaxies, the user who has configured the integration should belong to the host organization of the corresponding MISP server.

</td></tr><tr><td>

Sync Security Incident MITRE-ATT&amp;CK™ techniques as global galaxies to MISP event

</td><td>

Option to synchronize the ServiceNow AI Platform SIR security incident MITRE-ATT&amp;CK™ techniques as global galaxies in the MISP event.

</td></tr></tbody>
</table>
### Result

You created a profile that enables you to automatically create events in MISP from the ServiceNow AI Platform. You can now view the events in the Associated MISP Events related list.

## Add MISP tags to events

Add MISP tags to the created MISP events.

### Before you begin

Role required: sn\_sec\_misp.write

### Procedure

1.  On the Additional Options form, navigate to **Select MISP tags to add to the event** section on the form view.

2.  Review the options to add tags to the created events.

    |Field|Description|
    |-----|-----------|
    |Add tags to the created MISP event|Option that allows you to automatically add MISP tags to the events that are created from ServiceNow.|
    |Tags \(Local\)|The selected tags will be added as local tags to the MISP event.|
    |Tags \(Global\)|The selected tags will be added as global tags to the MISP event.|

3.  Click **Save**.


### Result

Adding MISP tags helps in classification of the event.

