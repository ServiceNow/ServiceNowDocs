---
title: Managing events in MISP
description: You can create events in MISP automatically or manually from the ServiceNow AI Platform. You can also edit the event data in MISP from the ServiceNow AI Platform.You can verify the automatically created events after you configure the event creation profile in your ServiceNow AI Platform instance.Manually create events in MISP from the ServiceNow AI Platform to capture contextually related information represented as attributes and objects.Add attributes to an event, such as the type, category, and other contextual information about the event.Add tags in ServiceNow AI Platform MISP to classify events or attributes. You can use tagging globally to enable your classification or use tags locally when you don't want MISP events to be modified during your classification.Add or remove galaxies in ServiceNow AI Platform MISP so that you can classify these objects as a cluster in the MISP instance and attach them to MISP events or attributes.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Using MISP to investigate and analyze threats, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Managing events in MISP

You can create events in MISP automatically or manually from the ServiceNow AI Platform. You can also edit the event data in MISP from the ServiceNow AI Platform.

**Parent Topic:**[Using MISP to investigate and analyze threats](using-misp-to-detect-and-analyze-threats.md)

## Verifying automatically created events in MISP

You can verify the automatically created events after you configure the event creation profile in your ServiceNow AI Platform instance.

### Automatic event creation profile

[Configuring the automatic event creation profile](../task/configure-automatic-event-creation-profile.md#) is done by the sn\_si.admin or the sn\_ti.admin user roles in the **MISP Integration** &gt; **Automatic Event Creation Profiles** module.

### Viewing the MISP event data

You can view the created events in the following ways:

-   View the work notes for the created events. You can view the event details in the ServiceNow AI Platform instance and also as it appears in the MISP server as shown in the following example.

    ![View the work notes for created events.](../image/misp-event-creation-worknotes.png "Work notes for created events")

-   Click the [Associated MISP Events](../reference/associated-misp-events.md) related list. Here, you can view the event in relation to the security incident and the MISP resources as shown in the following example.

    ![View the list of associated events](../image/misp-associated-event-list.png "List of associated events")

-   View the MISP event data in the form view to review the detailed information about the MISP events as shown in the following example.

    ![View the event data in the form view to see the detailed MISP event information.](../image/misp-event-data-form-view.png "Event data in the form view")


## Manually create an event in MISP

Manually create events in MISP from the ServiceNow AI Platform to capture contextually related information represented as attributes and objects.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables that you want to create an event for.

3.  Click **Create a new event in MISP**.

4.  In the Create a new event in MISP dialog box, fill in the details.

<table id="table_f1q_1td_mqb"><thead><tr><th colspan="2">

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Date

</td><td>

Creation date of the event in MISP.

</td></tr><tr><td colspan="2">

Event Info

</td><td>

Event information that is automatically created from the ServiceNow AI Platform Security Incident Response.

</td></tr><tr><td colspan="2">

Threat Level

</td><td>

Risk level of the event. You can categorize the incidents into three different threat categories \(low, medium, high\). This field can also be left as undefined. The following are the options:-   Low: General mass malware
-   Medium: Advanced Persistent Threats \(APT\)
-   High: Sophisticated APTs and 0-day attacks


</td></tr><tr><td colspan="2">

Source

</td><td>

MISP source for the event creation.

</td></tr><tr><td colspan="2">

Distribution

</td><td>

Option that controls who can view this event after the event is published. This option also controls whether the event is synchronized to other servers. The distribution is inherited by the attributes. The most restrictive setting wins. The distribution options are as follows:-   Your organization only: Enables only the members of your organization to view this event. The event can be pulled to another instance by one of your organization members where only your organization has the access to view it. Events with this setting are not synchronized.
-   This community only: Enables users that are part of your MISP community to view the event, including your own organization, organizations on this MISP server, and organizations that run MISP servers that synchronize with this server. Any other organizations that are connected to linked servers are restricted from viewing the event.
-   Connected communities: Enables users that are part of your MISP community to view the event, including all organizations on this MISP server, all organizations on MISP servers that synchronize with this server, and the hosting organizations of servers that connect to any server that is two hops away. Any other organizations that are connected to the linked servers that are two hops away from this server are restricted from viewing the event.
-   All communities: Shares the event with all MISP communities.


</td></tr><tr><td colspan="2">

Analysis

</td><td>

Current stage of the analysis for the event with the following possible options:-   Initial: The analysis is just beginning
-   Ongoing: The analysis is in progress
-   Completed: The analysis is complete


</td></tr><tr><td rowspan="6">

Advanced Options

</td><td>

Add SIR associated observables as attributes to MISP Event

</td><td>

Option to add available observables in a security incident to a MISP event as attributes.This option enables the **Set attribute IDS flag when observable finding is malicious** option.

</td></tr><tr><td>

Set attribute IDS flag when observable finding is malicious

</td><td>

Observable that is marked as malicious in SIR. The corresponding attribute in MISP is also marked as true.

</td></tr><tr><td>

Filter observables based on security tags

</td><td>

Option to filter the observables based on the selected security tags. This option provides the capability to distinguish and manage the MISP events in threat intelligence.**Security tags**: Add tags to filter the observables. For example, if you are adding a tag called 'Block from sharing' or 'TLP: White' then if one of the observables has any of these tags associated then these observables will not be added as an attribute to the MISP event during the MISP event creation.

</td></tr><tr><td>

Synch Security Incident MITRE ATT&amp;CK techniques as local galaxies to MISP event

</td><td>

Option to synchronize the ServiceNow AI Platform SIR security incident MITRE-ATT&amp;CK™ techniques as local galaxies in the MISP event.

</td></tr><tr><td>

Sync Security Incident MITRE ATT&amp;CK techniques as global galaxies to MISP event

</td><td>

Option to synchronize the ServiceNow AI Platform SIR security incident MITRE-ATT&amp;CK™ techniques as global galaxies in the MISP event.

</td></tr><tr><td>

Add tags to the MISP event

</td><td>

Option that allows you to add MISP tags to the events that are created from ServiceNow. This option displays the following options:-   **Local \(Tags\):**The selected tags will be added as local tags to the MISP event.
-   **Global \(Tags\):**The selected tags will be added as global tags to the MISP event.


</td></tr></tbody>
</table>5.  Click **Create New MISP Event**.

    The following example shows that by creating an event in MISP, you can view the results in the security incident. You also can view the work notes, the event in the ServiceNow AI Platform instance, and the event in the MISP server as shown in the following example.

    ![Manually create an event in MISP from the ServiceNow AI Platform.](../image/misp-manual-event-creation.gif "Manually create an event in MISP from the ServiceNow AI Platform")

    You can view the results in the following ways:

    -   A success message appears at the top of the security incident page. You can view the event details in the ServiceNow AI Platform instance and also as it appears in the MISP server.
    -   In the work notes, you can view the success message with more details. You can also view the event details in the ServiceNow AI Platform instance and also as it appears in the MISP server.
    -   In the [Associated MISP Events](../reference/associated-misp-events.md) related list, you can view the event in relation to the security incident and the MISP resources.

## Add attributes to a MISP event

Add attributes to an event, such as the type, category, and other contextual information about the event.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Verify that the event that you are adding or updating the attribute belongs to the same organization as the MISP user.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Navigate to **All** &gt; **MISP** &gt; **Associated MISP Events**.

    You can also navigate to the Associated MISP Event related list in any security incident.

2.  Click the MISP event that you want to add an attribute for.

3.  Click **Add Attribute to MISP Event**.

4.  In the Add Attribute to Event dialog box, fill in the details.

<table id="table_zhq_bbv_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value

</td><td>

Actual value of the attribute. Enter data about the value that is based on what is valid for the chosen attribute type. For example, for an attribute of type ip-src \(source IP address\), 11.11.11.11 is a valid value.**Note:** You can only select attributes or observables that share context with the event. The observables can't already have an attribute in MISP.

</td></tr><tr><td>

Category

</td><td>

Category of the attribute. The category describes the aspect of the malware for this attribute. An example would be the persistence mechanisms of the malware or network activity.

</td></tr><tr><td>

Type

</td><td>

Type that explains the category. For example, if an attacker uses an IP address for an attack, a source email address or a file sent through an attachment can all describe the payload delivery of a malware. These types of attributes have the category of payload deliver.

</td></tr><tr><td>

Distribution

</td><td>

Users who can view this attribute. The distribution is inherited by attributes. The most restrictive setting wins.

</td></tr><tr><td>

Use Attribute as an IDS signature

</td><td>

Observable that is marked as malicious in SIR. The corresponding attribute in MISP is also marked as true.

</td></tr><tr><td>

Comments

</td><td>

Comments that you add for the attributes.

</td></tr></tbody>
</table>    The following example shows that by navigating from the Associated MISP Events list, you can view the event record 5627 and add attributes to the event. The attributes include the value \(testdomain.com\), category as external analysis, type as domain. You can also enable IDS. The success message on the event record shows that the attribute is added to the event as shown in the following example.

    ![Adding attribute to a MISP event.](../image/misp-add-attribute-to-event.gif "Add attribute to a MISP event")

5.  Click **Add Attribute to MISP Event**.


### Result

You can view the added attribute in the Attributes section.

## Add tags to a MISP event

Add tags in ServiceNow AI Platform MISP to classify events or attributes. You can use tagging globally to enable your classification or use tags locally when you don't want MISP events to be modified during your classification.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Verify that the event you are editing belongs to the same organization as the MISP user.
-   Note that the tags and galaxies that are available to you are based on the MISP source and its distribution permissions.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the event that you want to add tags for.

3.  Click **Show All Related Lists** and the MISP Enrichment Results related list.

4.  Click the Event ID from the list of enrichment results.

    You can also navigate from the **MISP** &gt; **Associated MISP Events** module.

5.  Review the MISP Event record.

6.  To edit either a local or global tag, click the edit icon ![Edit icon.](../image/misp-edit-icon.png) in one of the following options:

7.  -   **Tags \(Local\)**
-   **Tags \(Global\)**
8.  In The MISP Event Tags dialog box, enter the tag name to search and add the tags.

9.  Click **Update Tags to MISP Event**.

    The following example shows that by clicking the edit icon for the local tags, you can search and add the C3, Adware, C2, and Botnet 3101 tags, and update the MISP server with the tags. The confirmation message shows that all the tags are updated in MISP.

    ![Updating tags to a MISP event.](../image/misp-add-tags-event.gif "Updating tags to MISP event")

10. Click **Reload Form** in the success message to view the changes in the record.


### Result

The tags are updated successfully in the MISP server.

## Update galaxies to a MISP event or attribute

Add or remove galaxies in ServiceNow AI Platform MISP so that you can classify these objects as a cluster in the MISP instance and attach them to MISP events or attributes.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) required for using the MISP bi-directional features.
-   To add local galaxies, the user who has configured the integration should belong to host organization of the corresponding MISP server.
-   The tags and galaxies available to you are based on the MISP source and its distribution permissions.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Click the edit icon ![Edit icon.](../image/misp-edit-icon.png) in one of the following options.

2.  -   **Galaxies \(Local\)**
-   **Galaxies \(Global\)**
3.  In The MISP Event Galaxies dialog, type and search to add the tags.

4.  Click **Update Galaxies to MISP Event**.

    The following example shows how to click the edit icon for the local galaxies, select the deprecated namespace, select the Enterprise Attack - Attack Pattern galaxy, and add cluster information. After the galaxy information is updated, you can view the success message.

    ![Updating galaxy information to MISP event.](../image/misp-add-galaxy-event.gif "Update galaxy information to MISP event")

    The galaxies are updated successfully in the MISP server.

5.  Click **Reload Form** in the success message to view the changes in the record.


