---
title: Configure instance user story integration
description: Formally track findings from a non-production environment using Stories in a production instance. To configure ServiceNow instance user story integration, perform the procedure.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [User story integration, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure instance user story integration

Formally track findings from a non-production environment using Stories in a production instance. To configure ServiceNow instance user story integration, perform the procedure.

## Before you begin

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\)

## Procedure

1.  Register your instances.

    See [Register your instance](register-your-instance.md).

2.  Set the **User Story Table**.

    The table selected becomes the target table in which you wish to insert a record. Task-based tables such as `rm_story` are a common choice. This table should exist on both the source instance and target instance.

3.  Customize the associated script to handle field updates dynamically based on the selected **User Story Table** and define **User Story Field Mapping** and the available fields.

    This allows scripting to be used to define a mapping from a finding in the lower environment to a story in the upper environment. For example, you can specify which values populate the **Short Description**, **Description**, or any other fields available on the selected table.

    By default, useful information is provided in the comments, along with a sample which can be used as a guide. Configure the script to suit your needs.

    The following variables are available when configuring source and destination instance processing scripts.

    -   **`isSource`**

        Set to `true` when executing on the source instance \(dev\).

    -   **`isDestination`**

        Set to `true` when executing on the destination instance \(prod\).

    -   **`payload`**

        A user-defined variable used to pass information between instances.

    -   **`grFinding`**

        The GlideRecord of the finding that is sending the request. Defined on the source instance only. Available fields are those of the `sn_se_finding` table.

    -   **`grTask`**

        The GlideRecord being created on the destination instance. Defined on the destination instance only. Available fields are those of the table selected in the **User Story Table** column.

    When `isSource` is `true`, the script executes only on the source instance. Use this block to load the `payload` object with variables from the finding record. The fields available are those within the `sn_se_finding` table.

    ```
    if (isSource) {
          // This logic is ONLY executed on the SOURCE instance.
          // Load the 'payload' object with variables from the finding record.
          // The fields which can be used are fields within the sn_se_finding table.
    
          payload.short_description = "Story generated from finding - " + grFinding.getDisplayValue();
          payload.description = "Definition: " + grFinding.definition.short_description;
          payload.description += "\nFinding details: " + grFinding.getValue('finding_details');
          payload.description += "\nFinding URL: " + gs.getProperty("glide.servlet.uri") + grFinding.getLink(false);
    }
    ```

    When `isDestination` is `true`, the script executes only on the target instance. Use this block to apply the `payload` object values to fields in the Story or Task table. Ensure that `grTask.insert()` is called so that the record is created. If you selected `rm_story`, the available fields are those of the `rm_story` table.

    ```
    if (isDestination) {
          // This logic is ONLY executed on the TARGET instance.
          // Set the field values in the Story/Task table using the payload object.
          // The fields which can be used are fields within the Story table.
          // If you selected rm_story, the fields you can set are those of the rm_story table.
    
          grTask.short_description = payload.short_description;
          grTask.description = payload.description;
          grTask.insert();
    }
    ```

    The following is a complete example showing both source and destination processing.

    ```
    // Available variables
    // isSource      - True when on source instance (dev)
    // isDestination - True when on destination instance (prod)
    // payload       - The user-defined variable used to pass information between instances
    // grFinding     - The GlideRecord of the finding sending the request (source only)
    // grTask        - The GlideRecord being created on the destination instance (destination only)
    
    // Source processing and payload preparation
    if (isSource) {
          payload.short_description = "Story generated from finding - " + grFinding.getDisplayValue();
          payload.description = "Definition: " + grFinding.definition.short_description;
          payload.description += "\nFinding details: " + grFinding.getValue('finding_details');
          payload.description += "\nFinding URL: " + gs.getProperty("glide.servlet.uri") + grFinding.getLink(false);
    }
    
    // Destination processing and payload use
    // Make sure to include grTask.insert() so that the record is created
    if (isDestination) {
          grTask.short_description = payload.short_description;
          grTask.description = payload.description;
          grTask.insert();
    }
    ```

4.  Once the instances are validated and mapping is complete, customers will now be able to select findings to push to the target instance.


