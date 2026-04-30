---
title: Cross-scope privileges for Localization Workspace
description: After you create custom translation artifacts, set cross-scope privileges so that your artifacts can be accessed from Localization Workspace.
locale: en-US
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Cross-scope privileges for Localization Workspace

After you create custom translation artifacts, set cross-scope privileges so that your artifacts can be accessed from Localization Workspace.

## Before you begin

-   Ensure that your custom artifact has a processor script which includes a method named getTranslatableContent.
-   Confirm the name of the table where your custom artifact's records are stored. Also confirm the table's application scope. You can find this information in the artifact's record in \[sn\_lf\_config\]. Detailed table information can also be found in \[sys\_db\_object\].
-   Set your application scope to Localization Workspace.
-   Role required: admin. The localization\_admin can't complete this procedure.

## About this task

Your custom artifacts are located in different application scopes, so you must provide access to them from the Localization Workspace application scope. Completing this configuration makes your artifacts visible and selectable in translation requests.

For each artifact, set two entries in Cross scope privileges \[sys\_scope\_privilege\]:

1.  A record for the artifact's table.
2.  A record for the artifact's processor script.

The source scope for these records should be Localization Workspace.

Artifacts that are available by default don't need manual configuration of cross-scope privilege. For more information, see [Types of Localizable content in Localization Workspace](../reference/lw-localizable-content.md).

## Procedure

1.  Ensure that you are in the Localization Workspace application scope, and navigate to **All** &gt; **System Applications** &gt; **Application Cross-Scope Access**.

2.  On the **Cross scope privileges** \[sys\_scope\_privilege\] list, select **New**.

    The Source Scope and Application fields are automatically set to Localization Workspace on the form.

3.  On the form, fill in the fields to create a record for your artifact's table.

    |Field|Description|
    |-----|-----------|
    |Target Scope|Enter the name of the application scope associated to your artifact table.|
    |Target Name|Enter the name of the table where your artifact is stored \(such as \[kb\_knowledge\]\).|
    |Target Type|Select `Table` from the list.|
    |Operation|Select `Read`.|
    |Status|Select `Allowed`.|

4.  Select **Submit** to complete the record for the artifact's table.

5.  Create another record for your artifact's Processor script by selecting **New** on **Cross scope privileges** \[sys\_scope\_privilege\].

6.  On the form, fill in the fields to create a record for your artifact's processor script.

    |Field|Description|
    |-----|-----------|
    |Target Scope|Enter the name of the application scope associated to your artifact.|
    |Target Name|Enter the name of the processor script.|
    |Target Type|Select `Script Include`.|
    |Operation|Select `Execute API`.|
    |Status|Select `Allowed`.|

7.  Select `Submit` to complete the record for the artifact's Processor script.


## What to do next

You may also need to set Restricted Caller Access privileges to make restricted resources available to Localization Workspace. For more information see [Restricted Caller Access for Localization Workspace](lw-restricted-caller-access.md).

**Parent Topic:**[Configuring Localization Workspace](../concept/configuring-localization-workspace.md)

**Related topics**  


[Types of Localizable content in Localization Workspace](../reference/lw-localizable-content.md)

[Create and configure a custom artifact](../../localization-framework/task/create-configure-custom-artifact.md)

[Create a processor script](../../localization-framework/task/create-processor-script.md)

