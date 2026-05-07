---
title: Installed with field normalization
description: Several components are installed with Field Normalization.Manage field normalization and transformation.Create test records for normalizations and transformations. Only records opened by users with this role are available for testing normalization and transformation rules in Test mode.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Field Normalization, Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Installed with field normalization

Several components are installed with Field Normalization.

The following preferences \(**Field Normalization** &gt; **Administration** &gt; **Preferences**\) control features for normalization and transformation:

|Preference|Description|
|----------|-----------|
|Enable field normalization|This preference enables or disables the Field Normalization functionality, including transformations.|
|Enable field normalization auditing|This preference enables or disables auditing of field normalization tables.|
|Logging|Select the maximum level of logging detail desired. For example, select Error to log only errors and Information to log errors, warnings, and information.|
|Decoration URL|Enter the URL for the help/information link associated with the Field Normalization decoration. This link opens the page presented to users who do not have rights to see the normalization or transformation record. The default link opens a ServiceNow Wiki page with a general explanation of Field Normalization. The purpose of this page is to explain to normal users why a field value they entered was changed automatically.|
|Restrict decorations to roles|Use this preference to define the user roles that can view the reference icon \(decoration\) adjacent to a normalized field. This decoration displays transformation and normalization records to users with the normalizer role. For all other users, it opens the URL specified in the Decoration URL preference. If this preference does not specify any roles, then all roles can see the decoration.|

## Field Normalization business rules

The following business rules were created for this plugin:

-   Ensure Rules Application Job
-   Ensure Transform Application Job
-   Ensure Rules and Alias Jobs
-   Ensure Transform Application Job
-   Ensure Decoration Attribute
-   Cleanup on field or table change
-   Prevent duplicates in class hierarchy
-   Handle potential duplicates
-   Run job
-   Ensure Pending Value Collection Job
-   Ensure name changer job
-   Flush forms when activating

## Field Normalization script includes

|Name|Description|
|----|-----------|
|FieldNormalizationAjax|Provides AJAX services for the Field Normalization plugin.|
|FNEnsureJob|Ensures that a job record exists for a particular extant data job target.|
|FNExtantDataJobChoices|Generates a list of tables for use in document\_id field of the fn\_extant\_data\_normalization table.|
|FNExtantDataJobUtil|Determines whether an extant data job is allowed to run.|
|FNFields|Returns valid fields for normalization.|
|FNTransformChooserUtil|Provides support for the fn\_transform\_chooser UI page.|
|Position|Finds a position within a given string.|
|Round|Rounds numbers with various rounding modes and intervals.|

## Field Normalization UI pages

|Name|Description|
|----|-----------|
|aliases|Creates the slushbucket with pending values for choosing aliases for a normal value.|
|fn\_transform\_chooser|Displays available transforms. Invoked by the New button on the fn\_transform related list.|

## Field Normalization roles

|Role|Description|
|----|-----------|
|normalizer|Person authorized to manage field normalization and transformation.|
|normalization\_tester|Person authorized to create test records for normalizations and transformations. Only records opened by users with this role are available for testing normalization and transformation rules in Test mode.|

**Related topics**  


[Enable auditing for a table](https://www.servicenow.com/docs/access?context=t_EnableAuditingForATable&version=australia&pubname=australia-platform-security&ft:locale=en-US)

## Normalizer \[normalizer\]

Manage field normalization and transformation.

### Contains Roles

The Normalizer \[normalizer\] role contains the Normalization Tester \[normalization\_tester\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Normalization Tester \[normalization\_tester\]

Create test records for normalizations and transformations. Only records opened by users with this role are available for testing normalization and transformation rules in Test mode.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

