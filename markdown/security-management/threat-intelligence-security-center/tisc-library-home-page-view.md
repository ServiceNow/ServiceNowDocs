---
title: TISC Library Objects form view
description: The Threat Intelligence Security Center objects home page consists of the following features.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# TISC Library Objects form view

The Threat Intelligence Security Center objects home page consists of the following features.

Use or navigate to these following sections and learn more about each SDOs in detail.

![TISC Objects home page view](../image/tisc-home-page-view.png)

<table id="table_rdn_qc2_4yb"><thead><tr><th>

Order

</th><th>

Menu/Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

**Details** tab

</td><td>

Use this section to view or edit the SDOs in the form view.

</td></tr><tr><td>

2

</td><td>

**Source Records** tab

</td><td>

Source records contribute to an aggregated record as displayed in the form view. These source records are auto created from feeds or manually created by the user.

</td></tr><tr><td>

3

</td><td>

**Related Records** tab

</td><td>

Lists all the related records associated with the SDO.

</td></tr><tr><td>

4

</td><td>

**Relationship Graph** tab

</td><td>

Visual representation of the related objects.

</td></tr><tr><td>

5

</td><td>

**Internal Intelligence** tab

</td><td>

Lists the internal intelligence records of the associated objects.

</td></tr><tr><td>

6

</td><td>

**Enrichment Results** tab

</td><td>

Lists the enrichment integrations associated with the objects.

</td></tr><tr><td>

7

</td><td>

**Form banner**

</td><td>

This is read-only section, which contains the key fields such as Type, Confidence, Threat score, Number of Sightings, Status and Expiration time.

</td></tr><tr><td>

8

</td><td>

**Form banner UI actions**

</td><td>

These are the security control lists that are available for you to click if they are needed to be added to the allow list, removed from the allow list \(Deny list\), or add it to the watch list based on the observables. Click to:-   add to watch list
-   add to deny list
-   add to allow list

**Note:** The Form actions are applicable only to Observables.

</td></tr><tr><td>

9

</td><td>

**Form UI actions**

</td><td>

The available form UI actions are:1.  **Add to Case**: Add the objects to the case.
2.  **Run Observable Enrichment**: Run the enrichments to the selected objects.
3.  **Save**: Save the record.
4.  **Delete**: Delete the record.

</td></tr><tr><td>

10

</td><td>

**Right Contextual menu**

</td><td>

Provides easy access to the quick controls such as attachments, notes, and so on, based on the tasks associated with that object. This option is available across the remaining two tabs for the threat analyst to access whenever required.The contextual menu provides easy navigation to:

1.  **Attachments**: Attach any file that are related to the objects.

**Note:** Whenever you either create a new observable, indicators, or any objects or view the existing objects, the **Attachments** pane is by default displayed on the respective form view. You can either click the **Attachments** icon on the right-contextual menu or go to **Preferences** &gt; **Workspaces** and disable the **Show the sidebar**. For more information, see [Configure Next Experience Workspace preferences](https://servicenow.com/docs/bundle/washingtondc-platform-user-interface/page/get-started/servicenow-overview/task/next-experience-workspace-preferences.html).

2.  **Insights**: Add any additional information related to the observables or indicators which are associated with that object.

</td></tr><tr><td>

NA

</td><td>

**Search in Navigator**

</td><td>

Use this search function to search for various objects within the Threat Intel \(TI\) library. For example, you can search for all observables records within the TI library module.

</td></tr><tr><td>

NA

</td><td>

**Search in Threat Intel Library**

</td><td>

Use this search function to search for the source records across multiple sources based on your search criteria. The results will be displayed in a separate **Search Results** tab. For example, for an IP address 104.227.137.35, if you need to search the records, by entering 104.\* then searching will narrowed down the records and displays the records that contains the IP address starting with 104 in the separate **Search Results** tab. -   You can also modify the existing search keywords in the Search Criteria on the same Search Results page without going back to the Threat Library page.
-   Similarly, you can also search based on the name and description of any particular record.
-   Once the records are filtered and listed, you can click on the list view which will take you to the respective record in a new tab.

</td></tr></tbody>
</table>**Parent Topic:**[Threat Intelligence Security Center Library](threat-intelligence-security-center-library.md)

**Related topics**  


[Understanding the Data Model](../reference/understanding-the-data-model.md)

[TISC Library Repository](tisc-ioc.md)

[Access Vulnerability Downstream actions](downstream-actions-from-the-vulnerability-form-view.md)

[Deleting threat intelligence library records](../task/tisc-delete-lib-records.md)

[Export intelligence data](../task/tisc-export-observables.md)

[Confirm Potential Relationships from Related Records](../task/confirm-potential-relationships.md)

[Automated Correlation](automated-correlation-rules.md)

