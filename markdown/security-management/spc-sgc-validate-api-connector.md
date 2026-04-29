---
title: Validate your API connector
description: Test the connection for your API connector. You must pass both checks before you can publish your connector. You must review your input and mapping to be sure that it is accurate before publishing your connector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating your own API connector, Use the workspace, Security Posture Control, Security Operations]
---

# Validate your API connector

Test the connection for your API connector. You must pass both checks before you can publish your connector. You must review your input and mapping to be sure that it is accurate before publishing your connector.

## Before you begin

Roles required:

-   sn\_sec\_spc\_core.developer
-   sn\_spc\_cxf.admin - required for advanced scripting

## Procedure

1.  Select **Validate**.

    A modal is displayed that tracks the progress for the two validation steps. Your connector, at a minimum, must pass this check before you can publish your connector. If you fail one or both of the validation checks, the **Publish connector** UI action isn’t activated.

    **Note:** Passing this validation so the **Publish connector** UI action is activated doesn’t necessarily mean your mapping is accurate. Review your mapping, address any errors and warnings, and resolve any issues. A passing validation check means that you can successfully connect to the endpoint you specified with the credentials and basic parameters that you have provided. You must review your mapping for accuracy.

2.  Select the icons in the stepper to return and edit your entries.

3.  Select **Save and continue** to move to the next step.

    **Note:** If you edit information in the stepper, your template, input fields, and mapping response fields might change.

4.  When you’re satisfied with your template, select **Publish connector**.

    **Note:** After you publish your API connector, custom attributes can’t be edited or deleted. You can edit the other fields.

5.  In the modal that is displayed, copy the information for scope, table, label, and value.

    Keep this information handy and note that a new record is displayed.

6.  Select **Create discovery source**.

7.  Fill in the fields with the information that you copied.

8.  Select **Submit and close the window**.


