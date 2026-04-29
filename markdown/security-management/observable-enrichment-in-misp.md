---
title: Observable enrichment in MISP
description: By enriching observables with additional information from various MISP sources during incident response investigations, you can contain identified threats.Enable automatic observable enrichment in the ServiceNow AI Platform MISP when new observables are associated with the security incident.Select individual or multiple observables and perform a manual observable enrichment so that you can enrich observables with additional information from various MISP sources.Add or remove tags in MISP to classify events or attributes. You can use tagging globally to enable your classification or use tags locally when you don't want MISP events to be modified during your classification.Add or remove galaxies in MISP so that you can classify these objects as a cluster in MISP and attach them to MISP events or attributes.Add comments for the MISP attributes. The comments that you add are for informational purposes only and are not used for correlation of MISP data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Using MISP to investigate and analyze threats, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Observable enrichment in MISP

By enriching observables with additional information from various MISP sources during incident response investigations, you can contain identified threats.

**Parent Topic:**[Using MISP to investigate and analyze threats](using-misp-to-detect-and-analyze-threats.md)

## Enable automatic observable enrichment in MISP

Enable automatic observable enrichment in the ServiceNow AI Platform MISP when new observables are associated with the security incident.

### Before you begin

-   Enable the Security Incident Response system property for the **Enables or Disables the scheduled job, Lookup Security Incident Observables** option to trigger the observable enrichment capability in SIR.
-   Role required: sn\_si.analyst

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables that you want to enrich the observable data in MISP for.

3.  Review the work notes after new observables have been associated with the security incident.

    The following example shows that a work note posts when the [Security Operations Integration - Enrich Observable flow](../../security-operations-integrations/task/secops-integration-enrich-observ-wf.md) triggers.

    ![View the work notes of the Observable Enrichment status.](../image/flows-misp-worknotes-start.png)

4.  In the MISP Enrichment Results related list of the security incident, view the enrichment results after the flow execution completes.

    ![View the work notes of the Observable Enrichment status after the execution is completed.](../image/flows-misp-worknotes-end.png)

    **Note:** You must configure that the MISP Enrichment Results related list appears in the security incident related lists. For more information, see [related list configuration](../../security-incident-response/concept/sir-new-ui-setup-form-uiaction.md).

    The following example shows the enrichment results in the MISP.

    ![View the enrichment results in the MISP Enrichment Results tab.](../image/misp-enrichment-results-tab.png)

    The following table shows the MISP enrichment results.

<table id="table_d23_blt_cwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event

</td><td>

ID of the event. Click open to view the record in the ServiceNow AI Platform instance.

</td></tr><tr><td>

Org

</td><td>

Organization that has originally created the event.

</td></tr><tr><td>

Observable

</td><td>

Observable that is associated with the event.

</td></tr><tr><td>

Category

</td><td>

Category of the attribute.View the list of categories in the [MISP documentation](https://www.circl.lu/doc/misp/categories-and-types/#categories).

</td></tr><tr><td>

Type

</td><td>

Type of the attribute.View the list of types in the [MISP documentation](https://www.circl.lu/doc/misp/categories-and-types/#types).

</td></tr><tr><td>

MISP Tags

</td><td>

List of tags that are associated with the MISP attribute.

</td></tr><tr><td>

MISP Galaxies

</td><td>

List of galaxies that are associated with the MISP attribute.

</td></tr><tr><td>

Comment

</td><td>

Contextual comment to further describe the attribute. These comments are not used for correlation and are purely informative.

</td></tr><tr><td>

IDS

</td><td>

Indicator of compromise, which allows it to be included in all the eligible exports.

</td></tr><tr><td>

Distribution

</td><td>

Distribution of the attribute after it is published. An attribute can have a different distribution level than the event. In either case, the lowest distribution level is used.

</td></tr><tr><td>

Hyperlink to the MISP event

</td><td>

Link to the MISP event, which is stored on the MISP server.

</td></tr><tr><td>

Integration vendor

</td><td>

Integration vendor who provides the data for enrichment.

</td></tr><tr><td>

Raw data

</td><td>

Raw data that is associated with the MISP attribute.

</td></tr></tbody>
</table>
## Perform a manual observable enrichment in MISP

Select individual or multiple observables and perform a manual observable enrichment so that you can enrich observables with additional information from various MISP sources.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Role required: sn\_si.analyst

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables that you want to perform the enrichment for.

3.  Click **Show All Related Lists** and the **Associated Observables** tab.

4.  Select the observable and from the Actions menu, click **Run Observable Enrichment**.

    You can select multiple observables for a sighting search.

    The Run Observable Enrichment dialog box appears.

5.  Select a MISP source and in the Selected column, select an implementation to enrich the selected observables.

6.  Click **Submit**.

    A work note shows that the [Security Operations Integration - Enrich Observable workflow](../../security-operations-integrations/task/secops-integration-enrich-observ-wf.md) has triggered. The associated implementation workflows execute to perform the enrichment. You can view the work notes in the security incident to view the status.

    The following example shows how to view the work notes for a manual observable enrichment.

    ![View work notes for manual observable enrichment.](../image/misp-enrichment-manual-worknotes.png "Work notes for manual observable enrichment")

    The enrichment message lists the created event. You can view the event in the ServiceNow AI Platform or in the MISP instance and view the details of the record in the MISP Enrichment Results tab.


## Add or remove tags to MISP attributes

Add or remove tags in MISP to classify events or attributes. You can use tagging globally to enable your classification or use tags locally when you don't want MISP events to be modified during your classification.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Verify that the attribute that you are editing belongs to the same organization as the MISP user.
-   Note that the tags and galaxies that are available to you are based on the MISP source and its distribution permissions.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables, attributes, or events that you want to add the tags for.

3.  Click **Show All Related Lists** and the MISP Enrichment Results related list.

4.  Click the preview icon ![Preview icon.](../image/misp-attribute-preview-open.png) next to a record, and then click **Open Record**.

    The following example shows how to review the **MISP Enrichment Results** and how to open a MISP enrichment record.

    Opening the MISP Enrichment Result record

5.  Review the MISP Enrichment Result record.

<table id="table_cww_w1j_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Observable

</td><td>

 

</td></tr><tr><td>

Event

</td><td>

Event ID that is assigned by the MISP server when the event was first created or imported into MISP.Preview the event or click the record to view the event data in the MISP Event Data page.

</td></tr><tr><td>

Org

</td><td>

Organization that created the MISP attribute.

</td></tr><tr><td>

Category

</td><td>

Category of the attribute that you add to the specific event in MISP. You can select an option such as an internal reference, network activity, financial fraud, and so on.

</td></tr><tr><td>

Type

</td><td>

Type of MISP attribute.

</td></tr><tr><td>

Integration vendor

</td><td>

Integration vendor that provides the data for the observable enrichment.

</td></tr><tr><td>

Created date \(in MISP\)

</td><td>

Date that the event was first created or imported into MISP.

</td></tr><tr><td>

IDS

</td><td>

Status of whether an observable is marked as malicious in SIR. The corresponding attribute in MISP is also marked as true.

</td></tr><tr><td>

Distribution

</td><td>

Distribution option controls, such as who can view this event after it is published. This option also controls whether the event is synchronized to other servers. The distribution is inherited by the attributes, and the most restrictive setting wins. The distribution options are as follows: -   Your organization only: Enables only members of your organization to view this event. The event can be pulled to another instance by one of your organization members where only your organization has the access to view it. Events with this setting are not synchronized.
-   This community only: Enables users that are part of your MISP community to view the event, including your own organization, organizations on this MISP server, and organizations that run MISP servers that synchronize with this server. Any other organizations that are connected to these linked servers are restricted from viewing the event.
-   Connected communities: Enables users that are part of your MISP community to view the event, including all organizations on this MISP server, all organizations on MISP servers that synchronize with this server, and the hosting organizations of servers that connect to any server that is two hops away. Any other organizations that are connected to the linked servers that are two hops away are restricted from viewing the event.
-   All communities: Shares the event with all MISP communities, which allows the event to be freely available.


</td></tr><tr><td>

Hyperlink to the MISP event

</td><td>

Link to the MISP event that is stored on the MISP server.

</td></tr><tr><td>

Raw data

</td><td>

Raw details for the observable enrichment data record.

</td></tr><tr><td>

Comment

</td><td>

Comments that you add for the attributes. These comments are for informational purposes only and not used for correlation.

</td></tr><tr><td>

Tags \(Local\)

</td><td>

Tags that are available on the host organization's MISP instance to enable tagging for synchronization and export filtering. MISP events are not modified when you use local tags. These tags are always stripped before being synchronized with other MISP instances and sharing communities.

</td></tr><tr><td>

Tags \(Global\)

</td><td>

Tags that are available globally to be shared and synchronized with other MISP instances and sharing communities. When you add global tags to MISP instances, you modify events.

</td></tr><tr><td>

Galaxies \(Local\)

</td><td>

Galaxies that are available on the host organization's MISP instance for synchronization and export filtering. MISP events are not modified when you use local galaxies. These galaxies are always stripped before being synchronized with other MISP instances and sharing communities.

</td></tr><tr><td>

Galaxies \(Global\)

</td><td>

Galaxies that are available globally to be shared and synchronized with other MISP instances and sharing communities. When you add global galaxies, MISP events are modified.

</td></tr></tbody>
</table>6.  To edit either a local or global tag, click the edit icon ![Edit icon.](../image/misp-edit-icon.png) in one of the following options:

7.  -   **Tags \(Local\)**
-   **Tags \(Global\)**
8.  In The MISP Attribute Tags dialog box, enter the name of the tag to search and to add it.

9.  Click **Update Tags to MISP Attribute**.

    The following example shows that by clicking the edit icon for the local tags, you can search and add the C3, Adware, C2, and Botnet 3101 tags, and update the MISP server with the tags. The confirmation message shows that all tags have been updated in MISP.

    Adding local tags in the MISP attribute.

    The tags update successfully in the MISP server.

10. To view the changes in the record, click **Reload Form** in the success message.


## Add or remove galaxies to a MISP event or attribute

Add or remove galaxies in MISP so that you can classify these objects as a cluster in MISP and attach them to MISP events or attributes.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   To add local galaxies, the user who has configured the integration should belong to the host organization of the corresponding MISP server.
-   Note that the tags and galaxies that are available to you are based on the MISP source and its distribution permissions.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Click the edit icon ![Edit icon.](../image/misp-edit-icon.png) in one of the following options.

2.  -   **Galaxies \(Local\)**
-   **Galaxies \(Global\)**
3.  In The MISP Event Galaxies dialog box, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Event ID|Event ID that is assigned by the MISP server when the event was first created or imported into MISP.|
    |Namespace|Namespace where the galaxy is stored. You can use namespaces to group similar galaxies.|
    |Galaxies|Galaxy where you store the cluster information.|
    |Clusters|Information about the clusters in the galaxy.|

4.  Click **Update Galaxies to MISP Attribute**.

    The following example shows that by clicking the edit icon for the local galaxies, you can select the deprecated namespace, select the Enterprise Attack - Attack Pattern galaxy, and add the cluster information. After the galaxy information is updated, you can view the success message.

    Adding galaxy information in MISP through the ServiceNow AI Platform

5.  To view the changes in the record, click **Reload Form** in the success message.


### Result

The galaxy information is successfully updated in the MISP server.

## Add comments to MISP attribute

Add comments for the MISP attributes. The comments that you add are for informational purposes only and are not used for correlation of MISP data.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Verify that the attribute that you are editing belongs to the same organization as the MISP user.
-   Role required: sn\_sec\_misp.write

### Procedure

1.  Click the edit icon ![Edit icon.](../image/misp-edit-icon.png) on the Comment field.

2.  Enter your comment in the Attribute Comment field.

3.  Click **Update Comment to MISP Attribute**.

    The following example shows that by clicking the edit icon next to the comment field, you can add a comment and then update the MISP attribute. After the comment is updated, you can view the success message.

    Adding galaxy information in MISP through the ServiceNow AI Platform.

4.  To view the changes in the record, click **Reload Form** in the success message.


### Result

The comment is successfully updated in the MISP server.

