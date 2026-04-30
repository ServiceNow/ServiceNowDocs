---
title: Enable dynamic creation for reference fields
description: When dynamic creation is enabled, entering a nonexistent value in a reference field creates a new record on the referenced table instead of returning an error.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add a reference field, Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable dynamic creation for reference fields

When dynamic creation is enabled, entering a nonexistent value in a reference field creates a new record on the referenced table instead of returning an error.

## Before you begin

Role required: personalize\_dictionary

## About this task

By default, a user must enter a value in a reference field that matches an existing record in the table that the reference field refers to. For example, the **Caller** field in an Incident must have a value that is an existing user. You can enable dynamic creation to create a new record on the referenced table when a user enter a nonexistent value in a reference field instead of returning an error.

## Procedure

1.  Right-click the field label in the form and select **Configure Dictionary**.

2.  Populate the following fields \(you may need to configure the Dictionary form\):

    -   **dynamic\_creation**: Select the check box.
    -   **dynamic\_creation\_script**: Enter a script that dynamically creates the record.
3.  Click **Update**.

    Examples:

    You could use the following `dynamic_creation_script` to create a record on the referenced table.

    ```
    current.name = value;
    current.insert();
    ```

    **Note:** The parent object can be used to access anything from the parent record.

    You could create a script include named MyUserReferenceCreator with the following contents:

    ```
    var MyUserReferenceCreator = Class.create();
    MyUserReferenceCreator.prototype = {
        initialize: function() {
        },
     
        create: function(current, value) {
            current.name=value;
            return current.insert();
        },
     
        type: 'MyUserReferenceCreator'
    }
    ```

    When the script include is created, the following `dynamic_creation_script` generates a new location for an invalid reference field value:

    ```
    new MyUserReferenceCreator().create(current, value);
    ```


**Related topics**  


[Configuring the form layout](../../form-administration/concept/configure-form-layout.md#)

