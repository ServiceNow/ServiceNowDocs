---
title: Create or edit a certification template
description: To create a certification template, follow these instructions.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Certification templates, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or edit a certification template

To create a certification template, follow these instructions.

## Before you begin

Activate the Certification Core plugin to enable the Compliance functionality. See [Compliance Activation](../concept/c_ActivatingCompliance.md) for details.

## Procedure

1.  Ensure that you have an appropriate filter that defines the records the template evaluates.

    The template applies its conditions to these records.

2.  Use the CI Class Manager to navigate to the Certification Template form:

    1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

    2.  Select **Hierarchy** to display the CI Classes list.

        Select the class for which to create a certification template.

    3.  In the class navigation bar, expand **Health** and then select **Compliance**.

3.  Select **Certification Template**.

4.  Or, navigate using one of these paths:

    -   **All** &gt; **Compliance** &gt; **Architecture Compliance** &gt; **Templates**
    -   **All** &gt; **Compliance** &gt; **Desired State** &gt; **Templates**
    -   **All** &gt; **Compliance** &gt; **Templates**
    -   **All** &gt; **Audit Definitions** &gt; **Templates**
5.  Select **New** or select a certification template to edit.

    The following fields are completed automatically:

    -   **Number**: Each new template has a unique number. All versions of the same template use the same number.
    -   **Active**: All new templates are set to Active.
    -   **Version**: The version of a new template is set to 1.
    -   **Audit type**: The system sets the default type to Architecture Compliance, Desired State, or Compliance, depending on the application in which the template was created. You can select a different type when you create the template, but the field becomes read-only when you submit the record. The system uses audit types to filter record lists for appropriate data and determine which conditions are visible on the template form.
6.  Complete the following mandatory fields.

    -   **Name**: Enter a descriptive name for this template. The name helps identify the purpose.
    -   **Filter**: Select the filter that identifies the records to be certified. You can select either active or inactive filter versions. By default, the system presents only active versions for selection. If you start enteringthe name of a filter, the auto-complete feature displays all versions for selection. For architecture compliance and desired state templates, only filters that use a table extended from Configuration Item \[cmdb\_ci\] appear on the choice list. All filters appear on the choice list for a compliance template. After you select a filter, the template condition builder appears. The template operates on the table specified in the filter.
7.  Enter a description for this template.

8.  Define certification conditions using the condition builders.

    All conditions are AND conditions. The audit type of the template determines which conditions are available.

    -   **Certification Attribute Conditions**: \[All audit types\] Select configuration item attributes or specifications to certify, such as CPU count, memory, or disk space. Available fields in the attribute condition builder depend on the table from the filter. Typical ServiceNow conditions for attributes are available, including the between operator for setting numerical conditions with high and low boundary values. This operator was added specifically for desired state conditions.

        The **Show Related Fields** item supports dot-walking, enabling you to include referenced fields in a certification attribute condition. Select **Show Related Fields** or **Remove Related Fields** to add or remove referenced fields \(in the form of &lt;field&gt; =&gt; &lt;field&gt;\). Select a referenced field to drill down to the next level of referenced fields.

        See [Dot walking](https://www.servicenow.com/docs/access?context=c_DotWalking&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    -   **Certification CI Relationship Conditions**: \[Desired State audit types\] Define the CI relationships to certify, such as Runs on or Depends on.
    -   **Certification User Relationship Conditions**: \[Desired State audit types\] Select the desired user relationship for this configuration item. The relationship provided in the base system is Log reviewed by.
    -   **Certification Group Relationship Conditions**: \[Desired State audit types\] Select the desired group relationship for this configuration item. The relationship provided in the base system is Backed up by.
    -   **Certification Related List Conditions**: \[All audit types\] Select field values from tables that reference the template table, or user-defined related lists ,which are created via custom relationships in the sys\_relationship table. To create a condition that evaluates all servers in the Server \[cmdb\_ci\_server\] table for the presence of Microsoft Word 2007, as referenced in the Software Installation \[cmdb\_sam\_sw\_install\] table. The resulting condition is \[Software Installation-&gt;Installed on\] \[Display name\] \[is\] \[Microsoft Word 2007\].

        Check **All** to include all records in the condition requirements of the related list. If there are no records in the related list, then:

        -   If **All** is checked, the condition requirement is met.
        -   If **All** is cleared, the requirement is not met.
    **Note:** By default, the condition builders for relationships display only suggested relationships. To see all possible relationships, select the **Show all relationships** check box on the side of the form.

    1.  Select **Insert a new row** to insert a condition.

        You cannot insert an empty condition.

    2.  Select the green check mark icon to save a condition.

        Make sure to save the condition before performing any other operation. Updating the form does not save the condition.

    3.  To delete a condition, select the red **X** beside the condition.

        The system marks the condition as inactive.

    4.  To reactivate a condition, select the gray **X**.

        If another condition for the same field exists, the system prevents reactivation and warns you of the conflict.

9.  Select **Submit**.

    ServiceNow saves the template as version 1.

10. To create another version of the template, change the name, edit the conditions, or select a different filter.

    Updating the template description does not create a new version.

    **Note:** If you select a filter whose table is incompatible with the existing template conditions, the system displays a warning that the conditions cannot be applied. ![Error message reading,"Some template conditions are incompatible with the selected filter. Incompatible conditions will not be used for auditing."](../image/IncompatibleFilterWarning.png)

11. Select **Update**.

    The system saves a new version of the current template and makes it the Active version. The previous version is marked inactive.


