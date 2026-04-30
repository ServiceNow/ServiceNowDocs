---
title: Configure Tagging Rules in TISC
description: Use tagging rules to automatically assign tags and taxonomies to RSS feeds. Tagging rules evaluate incoming feed data based on defined criteria and apply the appropriate tags and taxonomies when a match is found.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-02-21"
reading_time_minutes: 6
breadcrumb: [About Rules Engine in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configure Tagging Rules in TISC

Use tagging rules to automatically assign tags and taxonomies to RSS feeds. Tagging rules evaluate incoming feed data based on defined criteria and apply the appropriate tags and taxonomies when a match is found.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

Tagging rules are available from the **Administration** module and these tagging rules are supported for RSS feeds only.

Each tagging rule consists of matching criteria that TISC evaluates against incoming feed items, and a set of tags and taxonomies that TISC applies when all criteria are satisfied. When multiple tagging rules apply, all tags and taxonomies will be aggregated accordingly.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Rules Engine** &gt; **Tagging Rules**.

    The Tagging Rules list view displays all the existing tagging rules with the following fields.

<table id="table_ovc_lcd_j3c"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display name of the tagging rule.

</td></tr><tr><td>

Table

</td><td>

The table name for the tagging rule is **RSS Feed** by default, and it is read-only.

</td></tr><tr><td>

Description

</td><td>

A brief summary of the rule's purpose.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the rule is enabled or disabled. Only active rules are evaluated during feed processing.**Note:** This appears in the list view and is tagged to the tagging rule name in the form view, indicating whether it is enabled or disabled.

</td></tr><tr><td>

Method to Match

</td><td>

The keywords to match against the selected fields. Matching is case-insensitive by default.When defining a tagging rule, you must specify the keywords that the application will use to match against the fields you have selected. The matching process is case-insensitive by default, ensuring that matches are found regardless of letter casing.

There are two available matching options for evaluating feed items:

-   **Keywords**: Allows you to specify one or more keywords that the system will search for within the selected fields. By default, the option is Keywords.
-   **Regex**: Enables you to define regular expressions for more complex matching criteria within the feed data.

Choose the most appropriate matching method based on the complexity of your tagging requirements.

</td></tr></tbody>
</table>    **Note:** The following are the two base system tagging rules provisioned in the application for the RSS feeds. By default these two tagging rules are disabled, select **Enable** to enable the rules and proceed to next step.

    |Field|Description|Table|Method to Match|
    |-----|-----------|-----|---------------|
    |Sample Tagging Rule|This is a sample tagging rule.|sn\_sec\_tisc\_rss\_feed|Keywords|
    |Tag RSS Feeds with Zero Day mentions|This tagging rule is used to automatically associate the Vulnerability Intelligence: ZERODAY taxonomy with RSS feed records based on matching keywords found in the RSS feeds.|sn\_sec\_tisc\_rss\_feed|Keywords|

3.  Select **New** to create a tagging rule, or select an existing rule name to edit it.

    The Create New Tagging Rule form view opens. The form is divided into the following sections.

4.  In the **Details** section, fill in the basic configuration fields.

<table id="table_pvc_lcd_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique, descriptive name that identifies the tagging rule.

</td></tr><tr><td>

Description

</td><td>

Optional text that documents the purpose or scope of the rule.

</td></tr><tr><td>

Table

</td><td>

The table name for the tagging rule is RSS Feed by default.**Note:** As tagging rules are supported only for RSS feeds, the table name is read-only.

</td></tr><tr><td>

Fields

</td><td>

Select the fields that the tagging rule will match on. For example, you can choose fields such as **Description**, **Notes**, or **Title** of an RSS record.The available fields are displayed in a multi-select list that includes columns from the RSS table. Select one or more fields based on your requirements.

This matching is evaluated using the defined condition across the selected fields. The rule is considered a match when a keyword is found in any of the selected field. For example, if **Notes** and **Description** are selected, then the rule triggers when a match is detected in either of the selected field.

Select one or more keywords to match against the selected fields. Separate multiple keywords with commas. Each keyword is evaluated independently during matching.

**Note:**

-   The application checks whether any specified keyword is present in the values of the selected fields such as the content of the **Notes** or **Description** fields of an RSS record. If a match is found, the configured TISC tags and taxonomies and taxonomy values are automatically applied to the record.
-   The matching criteria support the following field types: **String**, **HTML**, **URL**, and **JSON**.


</td></tr></tbody>
</table>5.  Select the required Trigger Type.

    Use the **Trigger type** options to define when the rule runs. These options determine when the **TISC tags** and **taxonomy** values are associated with an RSS record.

    |Field|Description|
    |-----|-----------|
    |Run on insert|Select this check box to run the rule when a new RSS feed record is inserted.|
    |Run on update|Select this check box to run the rule when an existing RSS feed record is updated.|

    **Note:** **Activity stream**: This section displays the changed history of the record. Auditing is enabled to track the updates to these fields for execution, review, and troubleshooting.

6.  In the **Match criteria** section, define the conditions that a feed item must satisfy for the rule to apply.

<table id="table_qvc_lcd_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Method to Match

</td><td>

Matching is case-insensitive by default.The available matching options are:

-   Keyword\(s\)
-   Regex
Select the required option. The following section describes each matching option in detail. Refer to the descriptions as needed when configuring rules.

To configure the case sensitivity, update the `sn_sec_tisc.case_sensitivity_for_tagging_rules` system property as needed.

</td></tr><tr><td>

Keyword\(s\)

</td><td>

Select one or more keywords to match against the selected fields. Separate multiple keywords with a comma.

</td></tr><tr><td>

Regex

</td><td>

Select this option to add the condition using a regular expression \(Regex\). When selected, the **Regex** field is displayed allowing you to enter a regular expression to match against the specified fields. For example, .\*cve-\[0-9\].\*

</td></tr><tr><td>

Trim padded spaces for keywords

</td><td>

Select this check box to trim the leading and trailing spaces from keywords.When selected, the application automatically removes spaces entered before or after each keyword. For example, if extra spaces are included around a keyword, those spaces are ignored during matching.

If this check box is not selected, spaces are preserved and treated as part of the keyword. This allows you to control how precisely the match is evaluated.

**Note:** Only one regular expression can be provided.

</td></tr></tbody>
</table>7.  In the **Add TISC Tags &amp; Taxonomies** section, select the tags and taxonomies to apply when the rule criteria are met.

    |Field|Description|
    |-----|-----------|
    |Tags|Select one or more TISC tags to apply when the rule condition is met.|
    |Taxonomies|Select one or more taxonomy values to apply when the rule condition is met. Select a taxonomy and specify the corresponding taxonomy values to apply when a match occurs.|

8.  Select **Save** to save the tagging rule.

9.  Select **Enable** enable the tagging rule.

    **Note:** Once you enable the rule, the tagging rules form view will be in the read-only mode. You need to disable the tagging rule to edit the form view. The tagging rule execution is asynchronous.

10. Select **Duplicate** to copy an existing rule.

    A confirmation message is displayed indicating that the current tagging rule has been duplicated and a new rule has been created with a unique name.

    **Note:** When you copy an existing rule, the application creates a duplicate entry that retains all the field values from the original rule. The copied rule is created in a **disabled** state by default, allowing you to review or modify it before enabling the rule.


**To view the result of the execution**:

-   The application evaluates the RSS feed record against the rule conditions.
-   If a match is found:
    -   Configured tags and taxonomies values are automatically associated with the RSS feed record.
    -   A work note entry in the activity stream is added to record the action. The work note on the activity stream includes the following details:
        -   Tagging rule name
        -   Applied tags
        -   Applied taxonomy values

            ![TISC Tagging Rules - Activity Stream](../image/tisc-tag-rule-activity-stream.png)


If multiple rules are triggered, each rule appears as a separate row. When multiple tags and taxonomies values are applied by a single rule, they are listed as comma-separated values with tags and taxonomies separately applied by each tagging rule. When multiple tagging rules utilize the same tags or taxonomies values, the application ensures that duplicate tags and taxonomies are automatically managed. This prevents the same tag or taxonomy from being applied more than once to an RSS Feed record.

