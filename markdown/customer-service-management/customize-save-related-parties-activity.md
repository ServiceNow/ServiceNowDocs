---
title: Configure Save Related Parties Activity
description: Customize the Details and Automation tabs to define the Save Related Parties activity's data inputs and scheduling behavior within the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customize-save-related-parties-activity.html
release: australia
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 6
breadcrumb: [Save Related Parties Activity, Activities, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure Save Related Parties Activity

Customize the Details and Automation tabs to define the Save Related Parties activity's data inputs and scheduling behavior within the playbook.

After adding the Save Related Parties activity to your playbook canvas, customize it using the Details and Automation tabs in the side panel. Refer to the following sections for information to complete the activity setup. The Save related parties activity is available only when Playbooks for Customer Service Management is installed with the demo data flag enabled.

**Note:** Select Save and Continue before navigating between tabs to save your changes. Fields might display a "Missing required fields" validation message until the tab configuration is saved.

## Details tab

Use the Details tab to configure the activity's label, description, and scheduling conditions that determine when and how it runs within the playbook. The following table lists the configurable fields and sections within the tab. Complete the fields in the order listed before moving on to the next tab.

|Configuration|Description|
|-------------|-----------|
|Label|Display name for the activity as it appears in the playbook canvas.|
|Description|Brief description of the activity's purpose.|
|Activity definition|Predefined record that fetches the associated Automation configurations for the activity.|
|Schedule|Configuration that determines when the activity begins processing; either when running the stage, or after specified preceding activities complete.|

## Automation tab

Use the Automation tab to configure the fields that determine the activity's data inputs, including which related party records are loaded and how they relate to the parent record. The following table lists the configurable fields and sections within the tab. Complete the fields in the order listed before moving on to the next tab.

**Note:** The use case column references an example scenario of configuring the Save Related Parties activity for a loan application to illustrate how each field may be configured in practice.

|Configuration|Description|Use Case|
|-------------|-----------|--------|
|Related Party JSON|JSON output from an upstream Add related party activity. Connect the Related Party Output from the preceding activity.|If a co-applicant was previously added to a case, pass in their sys\_id to preload their record into the activity.|
|Related Party Table|Reference to the table whose schema is used to dynamically generate the add and edit form.|If adding co-applicants to a loan application, the related party table would be the Applicant table.|
|Parent Record|Sys ID of the parent record that related parties are linked to. Used only for direct relationships.|If saving co-applicants linked directly to a case, pass in the case's sys ID.|
|Parent reference field|The reference field on the related party table that points to the parent record. Enter the database column name, not the display label. Required for direct relationships.|If the Applicant table references the Case table through a field with the column name "case," enter "case."|
|Relationship Type|Setting that defines the relationship the related party table has with the parent record. Select Direct Relationship if the related party table contains a reference field pointing directly to the parent record. This is typically the most common configuration. Select Indirect Relationship if no direct reference exists and the related party record is created without a parent reference field.|If the Applicant table contains a Case reference field, select Direct Relationship. If adding a Consumer who will later be linked to a Household through a separate table, select Indirect Relationship.|

## Listed inputs and outputs for Save Related Parties activity

The following tables provide an overview of general inputs and outputs that drive the Save Related Parties activity's behavior and data flow for downstream processing. Use the fields as a reference when troubleshooting data flow within your playbook or configuring later workflow activities.

|Input Field|Description|
|-----------|-----------|
|Related Party Table|Target table on which records will be inserted, updated, or deleted, such as csm\_household\_member.|
|Related Party JSON|JSON object of related parties to save, typically piped from the Related Party Output of an upstream Add related party activity. Each entry's operation \(insert/update/delete/skip\) is determined by its metadata flags.|
|Parent Record|Sys ID of the parent record \(e.g., case or household\) that related parties are linked to. Used only for direct relationships.|
|Parent Field|Reference field name on the related party table that points to the parent record \(e.g., household\). Used only for direct relationships.|
|Related Party Relationship Type|Defines whether the relationship is direct \(single reference field set automatically on each related party\) or indirect \(through a many-to-many table; the parent field is not set by this activity, and the link must be created separately\).|

|Output Field|Use Case|
|------------|--------|
|Success|True when at least one record was processed successfully, false when all operations failed.|
|Related Party Created Sys IDs|Comma-separated list of sys IDs for records inserted in this activity execution. Empty for batches containing only updates, deletes, or skips.|
|Error Details|Concatenated error messages from failed operations \(record-level\), separated by '; '. Empty when all operations succeed. Intended for diagnostic use; sanitize before surfacing to end users.|

## Use Cases and Sample Configurations

Use this activity when your playbook needs to separate capturing related party data from writing it to the database, such as when approval, validation, or other steps must run in between. Note that this is distinct from the Save Related Parties check box in the Add Related Parties activity, which writes data to the database immediately when the agent completes the activity.

Configure the relationship type based on your data model: use a direct relationship if the related party table has a reference field pointing to the parent record, and an indirect relationship if it does not.

**Use Case 1: Save a related party with a direct relationship:**

Use a direct relationship when the Save Related Parties activity should automatically populate the parent reference field when saving each record.

In this example, the Household Member table has a reference field pointing to the Household table. The Save Related Parties activity takes the JSON from the upstream Add related party activity and saves each record to the Household Member table, with the household field populated automatically.

Example field value configuration:

-   Related Party JSON- Output from upstream Add related party activity
-   Related Party Table- Household Member
-   Parent Record- Household record sys ID
-   Parent Reference Field– household
-   Relationship Type- Direct Relationship

**Use Case 2: Save a related party with an indirect relationship**

Use an indirect relationship when the related party table does not have a reference field pointing to the parent. In this case, two Save Related Parties activities are needed — the first creates the related party record, and the second links it to the parent.

\(First activity\) Save to the related party table:

The first activity saves the related party record to it's primary table. No parent reference is set here because the table has no direct link to the parent. In this example, a Consumer record is created first. The Consumer table does not reference the Household table, so the relationship type is set to Indirect.

Example field value configuration:

-   Related Party JSON- Output from upstream Add related party activity
-   Related Party Table- Consumer
-   Relationship Type- Indirect Relationship

\(Second activity\) Establish the relationship:

The second activity links the record from the first step to the parent by saving it to a table that does reference the parent directly. In this example, a Household Member record is created using the Consumer saved in the first activity. The Household Member table references the Household table directly, so this step uses a direct relationship.

Example field value configuration:

-   Related Party JSON- Output from upstream Add related party activity
-   Related Party Table- Household Member
-   Parent Record- Household record sys ID
-   Parent Reference Field– household
-   Relationship Type- Direct Relationship

**Note:** To add an existing consumer as a household member, use only the second activity configuration.

