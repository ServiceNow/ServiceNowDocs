---
title: Configure Add Related Party Activity
description: Customize the Details, Automation, and UI Layout tabs to define the Add Related Parties activity's data inputs, scheduling behavior, and visual presentation within the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customize-add-related-party-activity.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Add Related Parties Activity, Activities, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure Add Related Party Activity

Customize the Details, Automation, and UI Layout tabs to define the Add Related Parties activity's data inputs, scheduling behavior, and visual presentation within the playbook.

After adding the Add Related Parties activity to your playbook canvas, customize it using the Details, Automation, and UI Layout tabs in the side panel. Refer to the following sections for information to complete the activity setup.

**Note:** Select Save and Continue before navigating between tabs to save your changes. Fields might display a "Missing required fields" validation message until the tab configuration is saved.

## Details tab

Use the Details tab to configure the activity's label, description, and scheduling conditions that determine when and how it runs within the playbook. The following table lists the configurable fields and sections within the tab. Complete the fields in the order listed before moving on to the next tab.

|Configuration|Description|
|-------------|-----------|
|Label|Display name for the activity as it appears in the playbook canvas.|
|Description|Brief description of the activity's purpose.|
|Activity definition|Predefined record that fetches the associated Automation and UI Layout configurations for the activity.|
|Schedule|Configuration that determines when the activity begins processing; either when running the stage, or after specified preceding activities complete.|
|Display order|Setting that determines when the activity appears relative to others during runtime by assigned number.|
|Start with delay|Optional condition that postpones the activity start until specific criteria are met.|
|Restart rules|Optional conditions that determine when the activity can be restarted once the specific criteria are met.|

## Automation tab

Use the Automation tab to configure the fields that determine the activity's data inputs, including which related party records are loaded and how they relate to the parent record. The following table lists the configurable fields and sections within the tab. Complete the fields in the order listed before moving on to the next tab.

**Note:** The use case column references an example scenario of configuring the Add Related Parties activity for a loan application to illustrate how each field may be configured in practice.

|Configuration|Description|Use Case|
|-------------|-----------|--------|
|Related Party SysIDs|Optional configuration that accepts comma-separated sys\_ids to prepopulate records already linked to the parent record. These records are preloaded into the activity UI when it renders.|If a co-applicant was previously added to a case, pass in their sys\_id to preload their record into the activity.|
|Related Party Table|Reference to the table whose schema is used to dynamically generate the add and edit form.|If adding co-applicants to a loan application, the related party table would be the Applicant table.|
|Relationship Type|Setting that defines the relationship the related party table has with the parent record. Select Direct Relationship if the related party table contains a reference field pointing directly to the parent record. This is typically the most common configuration. Select Indirect Relationship if no direct reference exists and the related party record is created without a parent reference field.|If the Applicant table contains a Case reference field, select Direct Relationship. If adding a Consumer who will later be linked to a Household through a separate table, select Indirect Relationship.|
|Parent field|Reference field in the related party table that points to the parent record. Required for Direct Relationship configurations. Ensure the value entered is the database column name rather than the field's display label.|If the Applicant table references the Case table through a field with the database column name "case," enter "case" in this field.|
|Card Body Fields|Fields selected from the related party table to display on each party card in the activity UI. Select the field to open a field selector and choose the columns to populate.|For a co-applicant scenario, relevant fields might include First name, Family name, Email, and Home phone.|
|Related Party View|Optional configuration that defines the form view for the related party table. If empty, the table's default view is used.|If a custom view has been created for the Applicant table that includes only relevant fields, enter that view name here.|

## UI layout tab

Use the UI Layout tab to configure the visual presentation and labeling of the activity card as it renders in the playbook. Fields within the tab are organized in the following sections, and correspond to a specific label displayed on the activity card. Complete the fields in the order listed before moving on to the next tab.

**Note:** The use case column references an example scenario of configuring the Add Related Parties activity for a loan application to illustrate how each field may be configured in practice.

<table id="table_zdz_mgy_m3c"><thead><tr><th>

Configuration

</th><th>

Use Case

</th></tr></thead><tbody><tr><td>

Activity header configurations: Tagline

</td><td>

In a loan application scenario, the Tagline label may be configured as "Applicant Information" to provide context at the top of the activity card.

</td></tr><tr><td>

Related party configurations:

-   Related party title
-   Add button label
-   Party record label
-   Card tagline icon name
-   Card tagline icon field

</td><td>

For a co-applicant scenario, the Related Party configurations may be named as followed. These fields are optional but recommended for clarity:

-   Related party title: "Co-Applicants"
-   Add button label: "Add Co-Applicant"
-   Party record label: "Co-Applicant"
-   Card tagline icon name: "user-outline"
-   Card tagline icon field: "relationship\_type"

</td></tr><tr><td>

Show avatar:

-   Avatar image source field
-   Avatar icon name

</td><td>

If Show Avatar is enabled, the Avatar Image Source Field may be configured with the file path to a local photo in order to source the profile image for each co-applicant card. The Avatar Icon Name may be set to "user" to represent each co-applicant with a person icon.

</td></tr><tr><td>

Card heading field

</td><td>

Configuring the Card Heading Field as "first\_name" displays the applicant's name on the card and derives the associated initials.

</td></tr><tr><td>

Show additional options:

-   Empty state configurations
-   Unsaved changes pop-up configurations
-   Delete confirmation pop-up configurations
-   Parent record configurations
-   Experience record configurations

</td><td>

For a co-applicant scenario, the Show Additional Options fields may be configured as follows to help prompt agents:

-   If no co-applicants have been added, the Empty State Header may be configured as "No co-applicants added" to provide a clear message when no records exist.
-   If an agent attempts to remove a co-applicant, the Delete Confirmation Header may be configured as "Remove Co-Applicant?" to ensure they are aware of the action before permanently removing a record.

</td></tr></tbody>
</table>## Listed inputs and outputs for Add Related Party activity

The following tables provide an overview of general inputs and outputs that drive the Add Related Party activity's behavior and data flow for downstream processing. Use the fields as a reference when troubleshooting data flow within your playbook or configuring later workflow activities.

|Input Field|Description|
|-----------|-----------|
|associated\_table|Parent table: Table containing the parent record.|
|associated\_record|Parent record: Specific parent record instance associated with the related parties|
|child\_table|Related party table: Table schema used to dynamically generate the add/edit form fields|
|related\_party\_relationship\_type|Related party relationship type: Defines whether the relationship is direct \(single reference field\) or indirect \(through a many-to-many table\)|
|parent\_reference\_field|Parent field: Reference field name in the related party table schema that points to the parent record|

|Output Field|Use Case|
|------------|--------|
|Related Party Output|Array of user-entered related party data returned in JSON format, stored in the Experience status record \(flow data\) for downstream processing, verification, or database record creation|
|Related Party Configurations|JSON object containing table and field configuration|

## Next steps

The Add Related Parties activity does not automatically transfer records to the database. To store the data collected during the activity, you must configure a custom playbook activity to transfer and store the collected records. For further steps, contact your administrator.

