---
title: MITRE-ATT&amp;CK heat map and navigator
description: You can use the MITRE-ATT&amp;CK heat map and navigator for basic navigation and to visualize your overall technique detection coverage.Access the MITRE-ATT&amp;CK heat map and navigator so that you can visualize the matrix that enables you to use ATT&amp;CK.Custom views in the MITRE-ATT&amp;CK heat map and navigator help you to save and view your favorite filters the next time that you land on the heat map.Use the primary filters to filter techniques in the MITRE-ATT&amp;CK navigator. The information in the MITRE-ATT&amp;CK repository is available for selection.You can use a heat map with advanced filters to perform an analysis by correlating security incidents with MITRE-ATT&amp;CK information.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 18
breadcrumb: [Using MITRE-ATT&amp;CK to detect and analyze threats, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE-ATT&amp;CK heat map and navigator

You can use the MITRE-ATT&amp;CK heat map and navigator for basic navigation and to visualize your overall technique detection coverage.

## Overview of the MITRE-ATT&amp;CK heat map and navigator

You can use the navigator with the primary filters for basic navigation and observation of ATT&amp;CK matrices. The heat map highlights the spectrum of the detection coverage including the blind spots where your organization does not have any coverage. This is available after you map the [technique detection coverage.](../task/map-technique-coverage.md)

With the heat map and navigator, you can:

-   Quickly and efficiently identify your organization's detection capabilities and highlight gaps in the technique detection coverage.
-   Hunt for threats and perform correlation of threats using associated features.

**Parent Topic:**[Using MITRE-ATT&amp;CK to detect and analyze threats](mitre-att-ck-features.md)

**Related topics**  


[Associate MITRE-ATT&amp;CK information with security incidents](../task/associate-mitre-with-sir.md#)

[Associate MITRE-ATT&amp;CK information with observables](../task/associate-mitre-observables.md)

[Associate MITRE-ATT&amp;CK information with security case](../../threat-intelligence-case-management/task/associate-mitre-att-ck-information-with-security-case-management.md)

[Rollup MITRE-ATT&amp;CK information using Threat Lookup results](../task/rollup-threat-lookup-results.md)

[Rollup MITRE-ATT&amp;CK information from detection rules](../task/rollup-mitre-attack-information-detection-rules.md)

[Rollup MITRE-ATT&amp;CK information from child security incidents](../task/rollup-mitre-att-ck-information-from-child-security-incidents.md)

[Perform link analysis and threat hunting using MITRE-ATT&amp;CK specific filters](../task/link-analysis-threat-hunt-mitre.md)

[Using the MITRE-ATT&amp;CK dashboard](mitre-dashboards.md#)

## Access the MITRE-ATT&amp;CK heat map and navigator

Access the MITRE-ATT&amp;CK heat map and navigator so that you can visualize the matrix that enables you to use ATT&amp;CK.

### Before you begin

Role required: sn\_ti.read, sn\_ti.mitre\_analyst

### About this task

You can review the heat map, use the filters to correlate, and perform link analysis of MITRE-ATT&amp;CK information, the observables, and the security incidents in your organization.

### Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Repository** &gt; **Heatmap and Navigator**.

    The heat map and navigator open in a new tab.

2.  Select the source to populate the heat map.

    **Note:** Only the [collections](../task/setup-mitre-profile.md) and [matrices](../task/view-mitre-collection.md) that have been activated appear in the source list.

    In the following illustration, you see how to navigate to the heat map and navigator, and how to select the source, which is Enterprise ATT&amp;CK in this example.

    Navigate to and select the source to populate the heat map

3.  Use the search box to quickly find a particular tactic or technique by using its name or ID.

    The following illustration shows how to search for a tactic, technique, or any information that is contained in them. Use search to drill down quickly to a specific tactic or technique.

4.  Click **Filters** and select a filter from the [Primary](mitre-att-ck-heatmap-and-navigator.md#) or [Advanced](mitre-att-ck-heatmap-and-navigator.md#) filters.

5.  Click **Apply** and control the filters as follows:

    -   To save your filters, [create a custom view](mitre-att-ck-heatmap-and-navigator.md#). You can create and save three [custom views](mitre-att-ck-heatmap-and-navigator.md#).
    -   To remove the selected filters, click **Restore Default Filters** to load your default saved view.
    -   To clear all filters and your existing view, click **Clear all filters**.
    **Note:** The views that you save are specific for a user.

6.  Click **Hide Sub-Techniques** to remove all sub-techniques from the heatmap view.

    If a technique has sub-techniques, you can click the expand icon to view the sub-techniques.


## Using the custom views

Custom views in the MITRE-ATT&amp;CK heat map and navigator help you to save and view your favorite filters the next time that you land on the heat map.

**Note:** You can create and save three custom views for every MITRE-ATT&amp;CK collection per user.

### Create a view

Once you select the required filters from the [Primary](mitre-att-ck-heatmap-and-navigator.md#) or [Advanced](mitre-att-ck-heatmap-and-navigator.md#) filters, click the ellipsis \(…\) button on the Filters header and select **Create a new view**. Enter the custom view name and **Save View**.

### Default views

Click **Save this as a default view** to directly load the view the next time that you land on the heat map. You can set a default view for each of the collections.

**Note:** If you are upgrading the Threat Intelligence plugin from an older version, then your existing default view from the old version appears as a custom view.

Illustration shows how to create a custom view in the heatmap

### Update a view

You can make updates to an existing custom view by modifying the required [Primary](mitre-att-ck-heatmap-and-navigator.md#) or [Advanced](mitre-att-ck-heatmap-and-navigator.md#) filters. Select a custom view, update the filters as required, and then click the ellipsis \(…\) button on the Filters header and select **Update view** to save the filters.

This Ilustration shows how to update a custom view.

### Manage custom views

Use the checkboxes next to each custom view to apply the selected custom view filter.

Click the ellipsis \(…\) button next to each custom view name to control the custom views as follows:

-   Set a default view.
-   Remove a custom view as the default view. This doesn’t delete the custom view.
-   Rename the custom view.
-   Delete the custom view.

This illustration shows how to manage custom views.

### Export a saved view

To export the saved custom views to JSON files, click ellipsis \(…\) on the Filters header and select **Export saved views**. Click the download icon for the custom view you wish to download to your local computer.

This illustration shows how to export custom views.

### Import a view

You can import only JSON files. To import the custom views, click the ellipsis \(…\) button on the Filters header and select **Import view\(json\)**.

Review the following conditions when importing views:

-   You can only import JSON file format.
-   You can import only one view or file at a time.
-   You cannot import if you already have three custom views in your filters. Delete a custom view and import a view.
-   You cannot import a view with an existing custom view name. Rename a view before you import.

This illustration shows how to import a view.

## Navigator with primary filters

Use the primary filters to filter techniques in the MITRE-ATT&amp;CK navigator. The information in the MITRE-ATT&amp;CK repository is available for selection.

<table id="table_g35_5fc_xnb"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Adversary Group \(Threat Group\)

</td><td>

Sets of related intrusion activity that are tracked by a common name in the security community. Groups can mean various threat groups, activity groups, threat actors, intrusion sets, and campaigns. You can add multiple groups to the **Adversary Group \(Threat Group\)** filter.For example, you add APT1 and AT12 as both are threat groups that are attributed to China. While both groups might target different sources, they could use similar techniques.

</td></tr><tr><td>

Tool

</td><td>

Legitimate software that is used by threat actors to perform attacks. You can understand how threat actors execute campaigns if you know how and what tools are used by threat actors. Tools includes both software that is not found on an enterprise system and software that is available as part of an operating system that is already present in an environment such as Microsoft Windows utilities.For example, gsecdump is a publicly available credential dumper that the APTI1 adversary group uses to obtain password hashes and LSA secrets \(Local Security Authority\) from Microsoft Windows operating systems.

</td></tr><tr><td>

Malware

</td><td>

Commercial, custom closed source, or open-source software that is intended to be used for malicious purposes by adversaries.Examples are PlugX, CHOPSTICK, and so on

</td></tr><tr><td>

Platform

</td><td>

Tactics and techniques that represent MITRE-ATT&amp;CK in a particular platform.For example, MITRE-ATT&amp;CK supports these platforms in the Enterprise ATT&amp;CK matrix: Microsoft Windows, macOS, Linux, PRE, AWS, GCP, Azure, Azure AD, Office 365, SaaS, Network.

</td></tr><tr><td>

Data source

</td><td>

Data sources that you are collecting in your environment and using to detect MITRE-ATT&amp;CK techniques.Examples are DLL monitoring, and browser extensions.

</td></tr></tbody>
</table>The following illustration shows all the primary filters available in the MITRE-ATT&amp;CK navigator.

![Primary filters.](../image/mitre-primary-filters.png)

## Using a heat map with primary and advanced features

You can use a heat map with advanced filters to perform an analysis by correlating security incidents with MITRE-ATT&amp;CK information.

### View technique IDs

You can view the MITRE-ATT&amp;CK technique IDs with the technique names when you select the **Display technique IDs** filter.

View technique IDs on a heat map

### View relevant techniques by priority

To filter the techniques based on their relevant priority in the navigator, select **Filter by technique relevant priority** filter and select the **Relevant Priority** from the menu. You can assign multiple priorities for filtering. You can also point to the techniques in the heat map to know the priority of the technique.

The relevant priority information is based on the prioritization you have set in the [Techniques](../task/view-techniques.md) relevant priority field.

This illustration shows filtering by relevant priority.

### View technique detection coverage

To view the overall technique detection coverage in the heat map, select the **Display technique detection coverage** filter. The heat map highlights the visual spectrum of the detection coverage including the blind spots where you do not have any coverage. The base system scoring definition and the colors have been defined in the [technique detection coverage](../task/define-technique-coverage.md). The information has been auto-extracted from the overall technique detection coverage.

For example, areas of the heat map that are marked in red indicate a lack of detection. Areas that are marked in blue indicate the presence of full detection capabilities. Areas that are marked in orange, yellow, and light blue reflect partial detection capabilities.

-   The color visualization is based on the [technique definition and color coding](../task/define-technique-coverage.md) that you define.
-   The coverage visualization is based on the [technique detection coverage mapping](../task/map-technique-coverage.md) that you define.
-   If you modify the base system coverage definition, the Coverage Type icons do not display with the techniques in the heat map.

    **Note:** The heat map works as expected when you modify the same fields as the base system's-defined technique detection coverage and coverage colors.


In this illustration, you see the technique detection coverage for all the techniques and sub-techniques and the coverage type with their colors and icons.

Heat map technique detection coverage

### View technique mitigation coverage

To view the overall technique mitigation coverage in the heat map, select the Display technique mitigation coverage filter. The heat map highlights the visual spectrum of the mitigation coverage including areas that you do not have any coverage. The mitigation coverage, colors, and percentage ranges have been defined in the [Mitigation Coverage Definition](../task/define-the-mitigation-coverage.md). The information is extracted from the [Overall Technique Mitigation Coverage](../task/map-your-mitigation-coverage-to-a-technique.md).

For example, techniques highlighted in red indicate no mitigation coverage, orange indicates poor mitigate coverage, and blue indicate excellent mitigation coverage.

-   The color visualization is based on the [technique mitigation definition and color coding](../task/define-the-mitigation-coverage.md) that you define.
-   The coverage visualization is based on the [technique mitigation coverage mapping](../task/map-your-mitigation-coverage-to-a-technique.md) that you define.
-   If you modify the base system mitigation coverage definition, the Mitigation Coverage Type icons do not display with the techniques in the heat map.

    **Note:** The heat map works as expected when you modify the same fields as the base system's-defined technique mitigation coverage and coverage colors.


This illustration shows the technique mitigation coverage heatmap

### View detection and mitigation coverage

You can use the technique detection and technique mitigation coverage filters together to gain an insight into the relevance of the technique detection and mitigate coverage for your organization.

![This illustration shows how to use the detection and mitigation filter together.](../image/mitre-heatmap-detection-mitigation.gif)

This illustration shows how to use the detection and mitigation filter together.

### View threat group

To view the threat group to technique information on the heat map, select **Display threat group heat map**. You can measure the number of threat groups that are using a particular technique. The probability of an attack using a particular technique increases when you have a high number of attackers. The threat group ranges, and heat map colors have been defined in the [Threat Group-Technique Heat Map Definition](../task/threat-group-to-technique-heatmap-definition.md).

-   The color visualization for the heat map and text is based on the [threat group to technique heatmap definition](../task/threat-group-to-technique-heatmap-definition.md).
-   The threat group range visualization is based on the [threat group to technique mapping](../task/review-threat-group-and-techniques-mapping.md).
-   You cannot use the **Display threat group heat map** filter when the technique detection coverage or technique mitigation coverage are enabled. This illustration shows the threat group information on the heat map.

### View Security incidents associated with technique

To view the techniques that are frequently exploited in your organization and that have resulted in security incidents, click **Display security incident associated with technique**. You can view more information about each of the associated security incidents when you click the link that open in a new window for analysis. Security incidents associated with a technique.

-   Priority: Select **Security Incident Priority** to filter by the security incident priority.
-   Date range: Select the **Security Incident Date Range** to filter security issues by the date range.
-   False positives: Select **Filter false positives security incident** to remove false positive issues. Selecting this filter reduces the number of security incidents you see in the heat map.

When you use this filter with the **Display technique detection coverage** filter, it provides you with an insight into the relevance of the technique detection coverage for your organization until the selected date.

For example, when you turn on both filters, you can see that under the Defense Evasion tactic, the Masquerading technique has no coverage. When you look further, the Masquerading technique is related to the Masquerade Task or Service, which also has a security incident that is associated with it. This shows that there is a gap in the technique detection coverage for the Masquerading technique and you may want to revise the overall technique detection coverage.

### View detection rules

To view if you have the detection rules defined for a particular technique, click **Display detection rules**. You can also see each associated detection rule with their definition.

This information is based on the [detection rules mapping](../task/create-detection-rules.md) that you have defined. View associated detection rules.

### View CVEs associated with technique

To view the Common Vulnerabilities and Exposures \(CVE\) information that is associated with each of the techniques, click **Display CVEs associated with technique**. The CVE to technique information is based on the information available in the [CVE - Technique Mapping module](../task/manage-cve-and-technique-mapping.md). This provides you insight into known vulnerabilities and lets you know if adversaries can potentially exploit your organization.

**Important:** The heat map is enhanced to display only the relevant CVEs that is associated with the VITs

To view VITs associated with CVEs and techniques, select **Display VITs associated with CVE and techniques**. Additionally, to further filter techniques without VITs, select **Hide techniques without VITs**. The CVE and VIT information you view is fetched from the Vulnerability Response product in your environment. You can view the filtered list of CVEs and VITs in the heat map and navigate to each CVE or VIT for every technique from the heat map.

**Note:**

-   The **Display CVEs associated with technique** is available only when the Vulnerability Response product is installed in your environment.
-   The VIT and CVE information is calculated based on the scheduled job you set in the [MITRE-ATT&amp;CK properties](../task/configure-mitre-att-ck-properties.md). The base system schedule job is set for 24 hours.

When you use this filter with the **Display security incident associated with technique** filter, you can learn if the known vulnerabilities have caused security incidents in your organization.

You can view more information about each CVE to analyze if the CVE is relevant to your organization. To do so, view the vulnerability items. If vulnerability items are created, you can view more information about any associated CI information in the Vulnerability Response module. You can also review the severity and priority to make informed decisions. Review CVEs to make informed decisions.

### Analyze Security Incidents

To analyze security incidents and review the techniques that are used by an adversary for an attack, click **Analyze Security Incidents**. You can add multiple security incidents for analysis by using comma-separated strings.

This filter helps you to analyze a security incident. You can learn why the incident occurred, what techniques were exploited, if any known threat actors were involved, if the threat actors used a particular sequence for an attack, and so on. Because you can analyze multiple security incidents at the same time, you can correlate the information to see if they are related or if they are an isolated incident. If the security incidents are related and you observe a pattern, you can review their progress on the kill chain to stop the attack or to form a defense strategy for your organization.

When you use the **Analyze Security Incidents** filter with primary filters, such as an **Adversary Group**, you can correlate if known adversaries are involved. For example, when multiple security incidents are being analyzed, the techniques that are associated with the security incidents are present in the form of a kill chain. As you overlap the information with the adversary, you will notice an overlap between the techniques that are associated with the security incident and the techniques that are associated with the adversary. Only the overlapped technique information is shown if both filters are enabled.

Analyze security incidents

### Using overlay to analyze security incidents and adversary groups

Use the **Enable Overlay / Analyze** filter to view the adversary behaviour and analyze one or more of the security incidents and correlate the information to see if an attack is an isolated incident or a coordinated attack by a known adversary.

For example, you can now view the security incidents and the threat adversary kill chain behaviour in the same view. This view provides overlap information which informs you of the attack and the known adversary behaviour. This enables you to analyze if this is an isolated attack or a coordinated attack by a known adversary.

Enabling the overlay analyze filter ignores all the primary filters except the **Adversary group** filter, and ignores the advanced filter **Filter by technique relevant priority** while generating a view.

Once you enable the overlay analyze filter, use the color palette to assign colors for the following:

-   Analyze Security Incident
-   Adversary Group
-   Overlay

The following illustration shows that the adversary group APT18 is spread across multiple techniques and tactics in the kill chain. The analysis also shows that there are three techniques which overlay the adversary group and security incidents that you are tracking. This illustration shows the adversary and security incident overlay information.

