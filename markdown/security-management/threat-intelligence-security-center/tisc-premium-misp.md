---
title: Configure custom MISP API feed
description: The Malware Information Sharing Platform \(MISP\) API feed enables you to import events from the MISP server, along with their associated attributes and objects, into the TISC library.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-05"
reading_time_minutes: 3
breadcrumb: [View Custom Feed, View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure custom MISP API feed

The Malware Information Sharing Platform \(MISP\) API feed enables you to import events from the MISP server, along with their associated attributes and objects, into the TISC library.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.

2.  Select **Custom**.

    **Note:** By default, the MISP feed is disabled, you must edit the configuration to enable the feed.

    ![Premium feed - MISP.](../image/tisc-misp-premium-feed.png)

3.  Select the **Edit** button on the **MISP Feed** card.

4.  Drill down to the **Configuration Details** section.

5.  Update the **REST endpoint URL** field.

6.  Add the required authentication details for the MISP server \(if any\).

7.  Navigate to **Additional Settings** to configure the filters to fetch the data from MISP.

    ![MISP feed- additional settings](../image/tisc-misp-additional-settings.png)

    The **Additional Settings** tab is used to set up filters that determine which MISP events are ingested.

8.  Select **Edit Settings**.

    ![MISP edit additional settings.](../image/tisc-misp-additional-settings-edit.png)

9.  Select the required filters.

    **Note:** All the filters configured will be applied in conjunction while ingesting the events.

    The following section provides a detailed explanation of each available option. Review each option in the following table to understand how the filters can be applied to optimize which MISP events are ingested into the TISC library.

10. Select the required values from the following available filters.

<table id="table_flc_vxs_z2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Filters on events**

</td></tr><tr><td>

Include unpublished events

</td><td>

Select this check box if you want to include unpublished events.

</td></tr><tr><td>

Creator org name or ID

</td><td>

Enter a comma-separated list of organization names and/or IDs associated with the event.**Note:** If the organization name contains leading or trailing spaces, enclose the name in double quotes to ensure proper processing.

</td></tr><tr><td>

Tag name or ID

</td><td>

Enter a comma-separated list of tag names and/or tag IDs associated with the event.

</td></tr><tr><td>

Threat level

</td><td>

Select a threat level to filter incoming events. Leaving this field empty includes events of all threat levels.

</td></tr><tr><td>

Distribution level

</td><td>

Select a distribution level to limit events. Leaving this field empty includes events of all distribution levels.

</td></tr></tbody>
</table>    **Note:**

    Once you've defined the **Additional Settings** following the instructions above, you can duplicate the feed when creating another. For more information, see Step 13.

11. Select **Update** on the **Additional Settings** dialog box to save the modified additional settings.

12. Select **Enable** to enable the MISP feed for including the MISP events.

    The TISC application uses the date configured in the **Fetch data from** field as the baseline for retrieving events and associated attributes.

    The **Fetch data from** date determines which events and associated attributes are retrieved. TISC compares this date with specific timestamps based on the event status:

    -   **Published events**: Compared against the **Published timestamp**.
    -   **Unpublished events**: Compared against the **Last updated timestamp**.
    An event is retrieved only if its relevant timestamp is later than the configured **Fetch data from** date.

    Using the appropriate timestamp for each event status ensures accurate retrieval of both newly published events and recently updated unpublished events.

13. Select **Duplicate** to duplicate the feed.

    For more information, see [Duplicate threat intelligence feeds](tisc-duplicate-feeds.md).

    **Note:**

    -   Each MISP event imported into the TISC library, whether as a **Threat Report** or **Threat Event**, includes an associated **External Reference** record.
    -   This record is accessible via the **Related Records** tab and provides a direct URL link to the corresponding MISP event on the MISP server. This also enables a quick access to the original event data.
    -   For details on how MISP events, along with their associated attributes and objects, are mapped to TISC entities, refer to [KB2197697](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2197697).
    -   Entity types that aren’t included in the mapping described in the KB article aren't ingested into the TISC Library.

**Parent Topic:**[View Custom Feed](view-oob-custom-feeds.md)

