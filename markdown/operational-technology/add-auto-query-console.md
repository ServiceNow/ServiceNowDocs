---
title: Create an Auto Query
description: Create an Auto Query that you can run on demand for different Discovery Console for OT Assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/add-auto-query-console.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Auto Query page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Create an Auto Query

Create an Auto Query that you can run on demand for different Discovery Console for OT Assets.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Assets &gt; Auto Query**.

2.  Select the add icon \[Omitted image "add-icon-msi.jpg"\] Alt text:.

3.  For the Identification section, use the automatically provided name or create your own name.

    **Note:** If you use an IP address that is already in the system as the new Asset identification, you receive an error message.

    \[Omitted image "duplicate-error-message.png"\] Alt text: Error message

    Be sure to use an IP address that is not in the system already.

4.  Select **Next**.

5.  In the Assets section, choose from Assets and Targets.

    The Assets to Query section lists the following choices:

    -   Existing Assets
    -   New Assets Only
    -   Incremental
    -   Asset Discovery
    -   Asset Discovery &amp; Query
    The default Asset selection is **Existing Assets**.

    When **Existing Assets** is selected for a query, the query uses the asset's IP address and Network Zone as its unique identifier. This allows the asset's IP address to exist across multiple Network Zones.

    \[Omitted image "existing-assets.png"\] Alt text: Existing Assets

6.  From the Targeted Sensors list choose from the following:

    **Targets** refers to Sensors and Collectors.

    -   All Sensors
    -   Specific Sensors
    -   Auto Targeting
    The default Targets selection is **All Sensors**. **All Sensors** uses all available Sensors and Collectors for the query. **Specific Sensors** uses only the selected Sensor and Collectors for the query. **Auto Targeting** tries to intelligently assign targets to Sensors and Collectors based on the query. It is designed to help manage complex deployments.

7.  Select **Next**

8.  In the Filters section, select the filters as needed.

    These filters help with the query selections. Filters include the following categories.

    **Note:** Some options in this section are only visible when the Assets selection is set to Existing Assets or Incremental. When the selection is Asset Discovery or Asset Discovery &amp; Query, a few options are disabled.

    -   **Sites**

        Site rules override global behavior when the Site filter is selected. If no site rules matches the Asset, the query skips the Asset.

        **Note:** The Console automatically generates a default site. This is in case no Sites have been previously created. You can select the Console-generated site when using the Sites filter to select specific sites.

        \[Omitted image "console-generated-site.png"\] Alt text: Console-generated Site

    -   Ports
    -   Ethernet Vendors
    -   Brands
    -   Inbound Protocols
    -   Outbound Protocols
    -   Network
    -   Ignore Networks

        **Note:** The Ignore Networks filter allows you to select an IP range or individual IP addresses to ignore during the query.

        \[Omitted image "ignore-ip-range-or-addresses.png"\] Alt text: Add networks to ignore

    -   Hostnames

        The Hostnames filter uses the hostname of the Asset and Targets the Asset based on the specified hostname information. To use this filter, select **No Filter** \(default selection\) or one of these options:

        -   **Empty/Null**: Queries Assets where the Hostname field is empty or null.
        -   **Exact**: Matches Assets whose Hostname equals any of the values you add. There is a field to type in a Hostname. All hostnames are included in this query unless you add at least one value.
        -   **Contains**: Matches Assets whose Hostname contains any of the substrings you add. There is a field for adding a value. All hostnames are included in this query unless you add at least one value.
        \[Omitted image "hostnames-selection.png"\] Alt text: Hostnames filter

9.  Choose a filter and then select **Next**.

10. In the Query Types section, select the applicable query types as needed.

    -   A Simplified query is a small list of easy-to-understand queries that should cover most possible scenarios. Most users start with this type of query.

        \[Omitted image "simplified-query-type.png"\] Alt text: Simplified query types

        **Note:** The simplified **Auto Query** type **Full Page Extraction** updates the query to perform a full extraction of your Target landing page. That means, this type of query includes both the screenshot and the HTML information.

    -   Advanced query: presents the list of all available auto queries. As some of these queries can be riskier, require more technically complicated to understand, or specific to certain devices; these queries are recommended only for advanced users.
    \[Omitted image "adv-query-types2.png"\] Alt text: Advanced Query types

11. You can set up the Auto Query scan to include all open ports.

    To do this, select both or either the **UDP Port Enumeration** and/or **TCP Port Enumeration** \(highlighted in the previous image\) from the Advanced Query Types. Each scan determines all open ports for their two respective protocols.

    **Note:** For these query types to be available, ensure your ScanScripts.json driver is up to date; if not, upload the latest version of this driver. For information about Query drivers, see [Edit the Query Driver on Metadata tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/edit-query-driver-on-metadata.md).

12. Select **Next**

13. In the Classification section, select from the following.

    \[Omitted image "brand-based-on-ocr.png"\] Alt text: Classifications

    -   **Brand based on MAC address**: Assigns brand based on MAC address range match.
    -   **Brand based on OCR words**: Attempts to assign brands based on strings extracted by the OC. Fuzzy word search is supported.
    -   **Console Hostname Look up**: Attempts to determine an Asset's hostname based on its IP address.
    -   **Location**: Sets a label and the location field with Site name.
    -   **Unknown**: Marks the Asset brand and category Unknown.
14. Select **Next**.

15. In the Confirmation section, set the schedule, recursion, and duration.

    \[Omitted image "auto-query-confirmation2.png"\] Alt text: Confirm and schedule

16. Select **Next**.

17. Select the **Create Auto Query** button.


## Result

The query is added to the Auto Query page.

