---
title: Copy patterns from one instance to another
description: To copy patterns from one instance to another, create an update set containing new or modified patterns with their related items in your development instance. Then, import the update set into your production instance.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Copy patterns from one instance to another

To copy patterns from one instance to another, create an update set containing new or modified patterns with their related items in your development instance. Then, import the update set into your production instance.

## Before you begin

Role required: pd\_admin

## About this task

Typically, you maintain two ServiceNow instances in your organization: for production and for development. Create or modify patterns, test them, and verify results in the development instance. When you are satisfied with the discovery results, export relevant patterns from the development instance to create an update set.

Update sets is a ServiceNow feature for transferring customizations from one instance to another. Each update set is stored in the Update Set \[sys\_update\_set\] table. Specific customizations associated with the update set are the entries in the Customer Update \[sys\_update\_xml\] table, and they appear as a related list on the update set record. The method of creating update sets for patterns is different from creating update sets for other types of customizations.

**Warning:** Always follow this procedure to create update sets for patterns. Do not use the standard platform procedure for creating update sets.

Depending on the extent of the changes, you can use the following pattern export methods:

-   **Export patterns**

    This option creates a new, customized version of the pattern and its related items necessary for the patterns to function properly. It then links them to the update set. The related items include:

    -   Extension sections
    -   Tracked files
    -   Related CI types
    -   Classification records
    -   Associated scripts

        **Note:** Update sets do not include changes in script includes used in patterns.

-   **Export patterns with CMDB items**

    This option creates a new, customized version of the pattern and its related items from the previous option, including any associated CMDB items. It then links all of these to the update set. The CMDB items include:

    -   Main CI type
    -   Entry point types
    -   Lookup tables
    -   Identifiers
    -   Hosting and reconciliation rules

The update set is an XML file with the following name convention: sys\_remote\_update\_set&lt;random alphanumeric string&gt;.xml.

## Procedure

1.  In the development instance, perform these steps to export patterns:

    1.  Navigate to **Pattern Designer** &gt; **Discovery Patterns**.

    2.  Select application or infrastructure patterns that you want to export.

        **Note:** You cannot export shared libraries.

    3.  At the bottom of the window, click the **Actions on selected rows** button.

        **Note:** You cannot use more than 20 patterns at a time for the **Export patterns with CMDB items** method.

    4.  Click **Export patterns** or **Export patterns with CMDB items**.

    5.  When the system finishes exporting patterns, it creates the update set.

    6.  To view the list of items included in the update set, click **View Logs** in the success message.

    7.  Click **Close**.

        The update set file in XML format is automatically downloaded on the computer.

    8.  Save the update set file locally for future use.

2.  In the production instance, perform these steps to import the customized patterns:

    1.  Elevate privileges to the security\_admin role.

    2.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    3.  Select the link **Import Update Set from XML**.

    4.  Select **Choose File** and select an XML file.

    5.  Select **Upload**.

        The customization is now available as a retrieved update set with state Loaded.

3.  [Preview the imported update set](https://www.servicenow.com/docs/access?context=t_PreviewARemoteUpdateSet&version=australia&pubname=australia-application-development&ft:locale=en-US).

    The system scans and validates the update set and displays its contents on the **Customer Updates** tab.

4.  [Commit the update set](https://www.servicenow.com/docs/access?context=t_CommitAnUpdateSet&version=australia&pubname=australia-application-development&ft:locale=en-US).

5.  Click **Close** in the success message.

    The production instance contains all new or modified patterns with related items from the update set.

6.  Upload the updated set of patterns and related items onto the MID Server:

    1.  Navigate to **Discovery** &gt; **MID Servers**.

    2.  Alternatively, navigate to **Service Mapping** &gt; **MID Servers**.

    3.  Click **Pattern Sync to Mid**.

7.  If the discovery fails or the result is not as expected, restart the MID Server to make sure that the MID Server runs the latest set of patterns.


**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Finalize a pattern](t_FinalizePatternPatDef.md)

**Next topic:**[Choose the pattern version](t_ChoosePatternVersionPatDef.md)

**Related topics**  


[System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US)

